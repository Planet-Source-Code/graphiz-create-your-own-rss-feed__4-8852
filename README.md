<div align="center">

## Create your own RSS Feed


</div>

### Description

Really Simple Syndication (RSS) is a lightweight XML format designed for sharing headlines, news, website updates and other Web content easily amongst various websites. Think of RSS as a mini portable database which can be shared at other websites using really simple methods. RSS also helps you to get more traffic to your webpage, so you can consider it as means of better webmasters methdology. RSS is not too hard to understand to create. Here in this article I would be showing how to create your own RSS Feed using ASP.

In my next article I would be showing how to create a XML parser which can take RSS Feed as input and output HTML. A version of which can be seen on my website at http://www.graphiz.net/Blog-G/rssreader.asp

The current article can also be viewed at

http://www.graphiz.net/Blog%2DG/viewentry.asp?id=43
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[graphiz](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/graphiz.md)
**Level**          |Intermediate
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |ASP \(Active Server Pages\), HTML, VbScript \(browser/client side\)

**Category**       |[Complete Applications](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/complete-applications__4-7.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/graphiz-create-your-own-rss-feed__4-8852/archive/master.zip)





### Source Code

```
<P><STRONG>What is RSS?<BR></STRONG>Really Simple Syndication (RSS) is a lightweight XML format designed for sharing headlines, news, website updates and other Web content easily amongst various websites. Think of RSS as a mini portable database which can be shared at other websites using really simple methods. RSS also helps you to get more traffic to your webpage, so you can consider it as means of better webmasters methdology. </P>
<P><STRONG>RSS Syntax</STRONG><BR>RSS defines an XML grammar for sharing news, view and web content. Each RSS text file contains both static information about your site, plus dynamic information about your new stories and blogs, all surrounded by matching start and end tags which being predefined provides a universal acceptance. The starting static tags in RSS file are TITLE, LINK, DESCRIPTION, COPYRIGHT and GENERATOR. You can provide your website information here.</P>
<DIV id=code>
<P><title>Graphiz Design Blog RSS Feed for Latest Articles</title> <BR><link>http://www.graphiz.net/Blog-G/journal.asp</link> <BR><description>Welcome to Graphiz, where I serve you the latest news, articles, review, tech stories, hot and fresh. Whether you are person in quest for code, tip or someone just browsing, I'll keep you up to date with the latest announcements. </description> <BR><copyright>Copyright (C) Graphiz.net All rights reserved.</copyright> <BR><generator>Graphiz RSS Generator</generator> </P></DIV>
<P>Each story or blog is defined by an <item> tag, which contains a TITLE, URL, and DESCRIPTION. Here's an example: </P>
<DIV id=code>
<P><item><BR>  <title>How to use RSS</title> <BR>  <link>http://www.graphiz.net/Blog-G/viewarticle?id=40</link> <BR>  <description>Description goes here</description> <BR>  <pubDate>Tuesday, 24 May 2004 12:00:00 AM GMT</pubDate> <BR>  </item><BR></div></P></DIV>
<P>Each RSS channel can contain up to 15 items and is easily parsed using ASP, Perl or other programming language or open source software. <BR>Once you've created and validated your RSS text file, register it at the various aggregators, and watch the hits roll in. Any site can now grab and display your feed regularly, driving traffic your way. Update your RSS file, and all the external sites that subscribe to your feed will be automatically updated. </P>
<P>If you are not really aware as to where to publish your RSS feed, take care look at what communication expert has to say.Robin Good has provided his Best Blog Directory and RSS Submission sites which can be viewed at http://www.masternewmedia.org/2004/02/05/rsstop55_best_blog_directory.htm</P>
<P><STRONG>How to Create RSS Blog in ASP<BR></STRONG>This can be a seperate blog but you can very well add to RSS Introduction here. After your static code, try putting code which gets all blog information from database and put them in XML format.</P>
<DIV id=code>
<P><%<BR>set conn = server.createobject(""adodb.connection"")<BR>DSNtemp=""DRIVER={Microsoft Access Driver (*.mdb)}; ""<BR>DSNtemp=dsntemp & ""DBQ="" & server.mappath(""YourDB.mdb"")<BR>conn.Open DSNtemp<BR>sqlstmt = ""SELECT * FROM Your_Blog_Table""<BR>Set rs = Server.CreateObject(""ADODB.Recordset"")<BR>rs.Open sqlstmt, DSNtemp, 3, 3<BR>x = 0<BR>For x = 1 to 10<BR> If rs.eof then<BR>  Exit For<BR> Else<BR>  Response.Write ""<item>""<BR>  Response.Write ""<title>"" & rs(""Your_Blog_Title"") & ""</title>""<BR>  Response.Write ""<link>Your_Blog_Link</link>""<BR>  Response.Write ""<description>Your_Blog_Summary</description>""<BR>  Response.Write ""<pubDate>Your_Blog_Posted_Date</pubDate>""<BR>  Response.Write ""</item>""<BR>  rs.MoveNext<BR> End If<BR>Next<BR>%></P></DIV>
<P>That is it and you have your own personalized RSS feed. </P>
<b>Other Useful Links at Graphiz related to RSS</b>
<ul>
<li><b>Universal RSS Reader -http://www.graphiz.net/Blog-G/rssreader.asp<b><br>If you are confused as to how your RSS Feed would look at various webpages, try this Universal RSS reader which would parse your feed and display as a simple HTML page</li>
<li><b>Open RSS Directory - http://www.graphiz.net/Blog-G/rssdirectory.asp</b><br>This contains links to various RSS feeds all around the web. Browse through them for tons of information and usefulness of having an RSS Feed</li>
</ul>
```

