---
id: server-ymgqlnl40oa
title: Server
sidebar_label: Server
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will explore the Server component of the Client-Server Architecture.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-web-server">What is A Web Server?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#server-side-rendering">Server-Side Rendering</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-web-server" data-id="76b66bd0bdb584c3c383098747af897b">What is A Web Server? <a class="markdownIt-Anchor" href="#what-is-a-web-server"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="2a7a8226fe5981610b7713d8a8fbfdfb">
<p>The primary task of a web server is to receive the requests from the client &amp; provide the response after executing the business logic based on the request parameters received from the client.</p>
</blockquote>
<p data-id="87f397d9534ead76ccb4fdb03bca8d55">Every service, running online, needs a server to run. Servers running web applications are commonly known as the <em>application servers</em>.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5411523088351232_image_5089167953362944.jpeg" alt=""></p>
<p data-id="a2b5dc370f4e45c68c4af9a790cb9521">Besides the <em>application servers</em>, there are other kinds of servers too with specific tasks assigned to them such as the:</p>
<ul data-id="9f6925d796cf692afc5df2b0b885f22a">
<li><em>Proxy server</em></li>
<li><em>Mail server</em></li>
<li><em>File server</em></li>
<li><em>Virtual server</em></li>
</ul>
<p data-id="a6650d4c03ff015d999df1cf1888af1f"><em>The server configuration &amp; the type can differ depending on the use case</em>.</p>
<ul data-id="a92fc89d1a9baa2a13470dda86ac14e8">
<li>
<p>For instance, if we run a backend application code written in <em>Java</em>, we would pick <em>Apache Tomcat</em> or <em>Jetty</em>.</p>
</li>
<li>
<p>For simple use cases such as hosting websites, we would pick the <em>Apache HTTP Server</em>.</p>
</li>
</ul>
<p data-id="d9dd0a4430168dfea35ebaecf50d4e1f">In this lesson, we will stick to the <em>application server</em>.</p>
<p data-id="f4ac1c6e64e96bb5a1bb4a4e763c1778">All the components of a web application need a server to run. Be it a database, a message queue, a cache or any other component. In modern application development, even the user interface is hosted separately on a dedicated server.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="server-side-rendering" data-id="bee2bbeda1242252e770d636dacc9565">Server-Side Rendering <a class="markdownIt-Anchor" href="#server-side-rendering"><span class="anchor-link">#</span></a></h2>
<p data-id="4c48122bdf604720697b250270d11392">Often the developers use a server to render the user interface on the backend &amp; then send the rendered data to the client. The technique is known as <em>server-side rendering</em>. I will discuss the pros &amp; cons of <em>client-side</em> vs <em>server-side</em> rendering further down the course.</p>
<p data-id="53ac9d03242c23f75c3baebc105114bf">Now we have a fundamental understanding of both the client &amp; the server. Let’s delve into some of the concepts involved in the communication between them.</p>
</div></div></div></div></div></div></div></div></div>