About a year or so back I added <category> elements to the MSDN RSS feeds, which seemed like an obvious addition, but it wasn&#8217;t until recently that I noticed that my own feeds (coming out of my .Text 0.95 based blogging engine) didn&#8217;t have categories specified in them at all. Not in <a href="http://blogs.duncanmackenzie.net/MainFeed.aspx" target="_blank" class="broken_link">the main feed</a> or in the <a href="http://blogs.duncanmackenzie.net/duncanma/rss.aspx" target="_blank" class="broken_link">per-blog feeds</a>&#8230; 

This seemed really odd to me, since much of the UI of the .Text posting page, editing page, and even the blog skins themselves is dedicated to the listing and selecting of categories. Obviously, categories are seen as important information about blog entries, so why not include them in the RSS feeds? Oh well, there is little point in wondering about these sorts of things, not when you have the source, so I added category elements to my main and individual feeds. I haven&#8217;t added them to the per-category feeds yet, or to the ATOM feeds, but I&#8217;ll get to those in the near future.

If you haven&#8217;t looked at the .Text source yourself, you might be wondering why adding these elements to one feed wouldn&#8217;t have added them to all of the feeds, because all RSS feeds are probably running through the same code path. While this is mostly true, they are running through the same ASP.NET handler and through the same feed generation code, the category-based feeds use a different stored procedure to retrieve their entries than the feeds that I have updated, and I had to make a change to the database query to return the list of categories along with each item. What I ended up doing, (and I&#8217;m not sure about the performance of this code but it is so highly cached that I&#8217;m not particularly worried about it for this use), was using a Function to retrieve the list of categories as a semi-colon deliminated string given a PostID (note that if you host multiple blogs on your .Text instance that this function should take both a BlogID **and** a PostID&#8230; I&#8217;ll have to update this for the multi-blog case).

<pre><br /> <span class="TSql_ReservedKeyword">CREATE</span> <span class="TSql_ReservedKeyword">FUNCTION</span> blog_GetCategoryTitles (@PostID <span class="TSql_DataType">int</span>) RETURNS <span class="TSql_DataType">nvarchar</span>(4000)<br /> <span class="TSql_ReservedKeyword">BEGIN</span><br /> <span class="TSql_ReservedKeyword">DECLARE</span> @CategoryList <span class="TSql_DataType">nvarchar</span>(4000)<br /> <span class="TSql_ReservedKeyword">SELECT</span> @CategoryList = <span class="TSql_Function">COALESCE</span><br />(@CategoryList + <span class="TSql_String">';'</span>, <span class="TSql_String">''</span>) +<br /> blog_LinkCategories.Title<br /> <span class="TSql_ReservedKeyword">FROM</span> blog_Content<br /> <span class="TSql_Function">LEFT</span> <span class="TSql_Operator">OUTER</span> <span class="TSql_Operator">JOIN</span> blog_Links <br /> <span class="TSql_ReservedKeyword">on</span> blog_Links.PostID = blog_Content.ID<br /> <span class="TSql_Function">LEFT</span> <span class="TSql_Operator">OUTER</span> <span class="TSql_Operator">JOIN</span> blog_LinkCategories<br /> <span class="TSql_ReservedKeyword">on</span> blog_Links.CategoryID = blog_LinkCategories.CategoryID<br /> <span class="TSql_ReservedKeyword">WHERE</span> blog_Content.ID=@PostID <span class="TSql_Operator">AND</span><br /> blog_Content.BlogID = blog_Links.BlogID <span class="TSql_Operator">AND</span><br /> blog_LinkCategories.Title != <span class="TSql_String">''</span><br /> <span class="TSql_ReservedKeyword">RETURN</span> @CategoryList<br /> <span class="TSql_ReservedKeyword">END</span><br /> </pre>

_thanks to <a href="http://www.sqlteam.com/item.asp?ItemID=2368" target="_blank">Garth&#8217;s 2001 article from SQLTeam.com for showing me COALESCE being used for this purpose&#8230;</a>_

and then modifying the queries that retrieved entries to also return blog_GetCategoryTitles(<PostID>), and then modify the RSS writer to output the categories if any were returned.

Interesting note, I figured the omission of category data from the feeds in .Text was a simple error and that it would have been added along the way to Community Server, but I noticed that the feeds on <a href="http://blogs.msdn.com/alexbarn/rss.aspx" target="_blank" class="broken_link">blogs.msdn.com</a> don&#8217;t appear to have category data either&#8230; is category information not considered useful in feeds?