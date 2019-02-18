I&#8217;m just playing around with an internal application, just a tool that hits our internal web services for article ratings (you know, the little box that says &#8220;7 out of 9&#8221; next to MSDN articles&#8230;) and displays the results in a grid. Well, there are a lot of things I&#8217;ve been hoping to add to the Windows Forms Data Grid, and while I&#8217;ve done quite a few of them (3 or 4 custom column types) I&#8217;ve never gotten around to adding the really cool stuff&#8230;. but by using someone else&#8217;s grid, I get all of that functionality for free. I&#8217;ve been a big Janus fan since before .NET&#8230; but I never used it in a real project before, since I had already purchased <a href="http://www.componentone.com/products.aspx?ProductCode=1&#038;ProductID=67" target="_blank">the excellent &#8220;TrueDB Grid&#8221; </a>for VB5/6 and &#8230; well&#8230; once you&#8217;ve paid for a grid that works well, there is little incentive to try out another one. Anyway, I grabbed the trial edition of <a href="http://www.janusys.com/janus/library/default.aspx?url=/janus/download/downloadcenter.aspx" target="_blank" class="broken_link">Janus&#8217;s .NET controls</a> and I have to say that I&#8217;m impressed&#8230; very nice stuff feature wise, and as graphically appealing as I have always thought from looking at their demos. 

<img src="http://www.duncanmackenzie.net/JanusGrid.png" border="0" />

I especially like the grouping features, which work a lot like Outlook&#8230; and the Field Chooser (shown in the picture above) which knows about all of the available fields from the data source and lets you pick and choose which ones to display in the grid. It doesn&#8217;t automatically appear though, but it was easy to add. I just created a context menu with a single item &#8220;Show Field Chooser&#8221; and a teeny bit of code in it (Me.ratingsGrid.ShowFieldChooser())

Anyway, I&#8217;m going to get back to coding, but I thought I&#8217;d post my thoughts on this&#8230;. 

I hope everyone carefully considers the **build vs buy** decision when they are looking at their UI requirements&#8230;. it is often a very cost-effective choice to pick up a control or two&#8230; and, on that note&#8230;. check out <a href="http://msdn.microsoft.com/vbasic/vbrkit/component/" target="_blank" class="broken_link">the VB Control Gallery</a> that appears to have grown out of the Visual Basic Resource Kit.