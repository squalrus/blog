[
						  
<font face="Trebuchet MS" color="teal">Darren&#8217;s</font>
				  
](http://dotnetweblogs.com/DNeimke){.broken_link} 
				  
 <font face="Trebuchet MS" color="teal">comments on</font>
				  
[
						  
 <font face="Trebuchet MS" color="teal">my previous post:</font>
				  
](http://dotnetweblogs.com/duncanma/Posts/4921.aspx){.broken_link} 

_I certainly don&#8217;t want to get into a debate over this but, shouldn&#8217;t the
  
question be: &#8220;what is it best to use?&#8221;. </p> 

I&#8217;m probably biased because I
  
never really programmed in any typed languages before .NET, but, to me at least,
  
being as explicit as possible is always a good thing. 

I know that Int32
  
will map to System.Int32 even in version 30 of the Framework. God knows what
  
Integer or int will map to by then.   
</em>  
<font face="Trebuchet MS" color="teal">Instead of replying<br /> back to him directly or in the comments, I thought I would try replying in<br /> another blog entry (there certainly are <a href="http://dotnetweblogs.com/DNeimke/posts/4910.aspx" class="broken_link">some issues </a>to be<br /> worked out regarding the best way to comment/discuss)..</font>

<font face="Trebuchet MS" color="teal">Good point Darren, thanks. The problem I<br /> see is that the question of &#8220;best&#8221;&nbsp;isn&#8217;t an easy one to answer. If you are<br /> writing your code to be dependent on the size of the underlying data type, then<br /> the desire to be explicit is certainly understandable, but when programming in<br /> C# or VB.NET you do not always need to be aware of this implementation detail.<br /> (that hurt to even type, I&#8217;m a big fan of always knowing about the details&#8230;<br /> but my point is that you shouldn&#8217;t <strong>have to know about them</strong> in<br /> this case). In fact, I think you should try to avoid being implementation<br /> dependent as a general rule.</font>

<font face="Trebuchet MS" color="teal">As I mentioned in my last post, if I&#8217;m<br /> working in&nbsp;a situation, such as a Win32 API call, where the exact size of<br /> the integer, the number of bits involved, is relevant then I use it. In all<br /> other situations, I need to know that my data type (Integer) is <em>big<br /> enough</em> to hold the range of values I want to work with. Personally, I<br /> noticed and even wrote about the fact that Integers and Longs have changed from<br /> VB6 to VB.NET, but that change has had almost no effect on most VB6 code<br /> upgraded to VB.NET, except when calling out to external libraries. So, if in<br /> future implementations of the VB.NET compiler, they decide that (for efficiency<br /> on the standard processors of the day, perhaps) Integer should map to Int64,<br /> then I would hope that wouldn&#8217;t cause me much of a problem&#8230; if they decided,<br /> and I don&#8217;t think they would, to change the mapping to Int16, then I think I<br /> would be screwed.</font>

<font face="Trebuchet MS" color="teal">Right after the PDC in 2000, I had just<br /> installed the .NET Framework &#8220;alpha&#8221; onto a machine and was busily writing a<br /> book on VB.NET&#8230; I decided that I should always use fully qualified types<br /> (System.Text.StringBuilder, instead of using an Imports and then just<br /> StringBuilder)&#8230; .NET was so new to many people that I wanted to err on the<br /> side of clarity. I also decided that I shouldn&#8217;t use things like Integer or<br /> MsgBox and that I should instead use System.Int32 and<br /> System.Windows.Forms.MessageBox.Show()&#8230; in time though I realized that I<br /> prefer to work with the terms/keywords that I am familiar with, and that even<br /> with Intellisense, I prefer to work with relatively short and easy to remember<br /> terms as well. So, now I use Imports for common namespaces (on a code file by<br /> code file basis, I really find the &#8220;default&#8221; Imports in VS.NET confusing)<br /> and&nbsp;I use language specific data types. I think that this is natural for<br /> people, and I wouldn&#8217;t want to try and change developers to Int32 or to change<br /> VB6 developers so that they stop using MsgBox(&#8220;Test&#8221;).&nbsp;Developers have<br /> habits; for example, I still use hungarian notation in lots of my own code<br /> (sorry <a href="http://blogs.gotdotnet.com/BradA/" class="broken_link">Brad</a>, I did read the<br /> design guidelines, I really did&#8230; I even use FxCop&#8230; my public members are<br /> generally ok, I just can&#8217;t stop using hungarian in my private variables!) even<br /> though it is no longer recommended.</font>

<font face="Trebuchet MS" color="teal">I am still undecided about using fully<br /> qualified types in samples, sometimes people copy/paste a snippet of code from<br /> one of my articles that it is not a complete class or code file (and therefore<br /> does not include any Imports statements) and get quite confused when it doesn&#8217;t<br /> compile and they have all of these squigglies under the class names. When I can<br /> write code samples in such a way that the required Imports are automatically<br /> attached (even to a single code snippet) then I won&#8217;t have to use fully<br /> qualified class names, but for now I think I will have to change my coding style<br /> for snippets.</font>

<font face="Trebuchet MS" color="teal">Darren, you said you didn&#8217;t want a<br /> debate and here I am replying with such a long post&#8230; but there really is no<br /> debate, at least not from me. I don&#8217;t know what the &#8220;best&#8221; way is, I<br /> just&nbsp;hope that some of my comments help explain why I have chosen a certain<br /> set of coding rules.</font>