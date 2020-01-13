---
id: http-push-pull-introduction-je1yez4xyzj
title: HTTP Push & Pull - Introduction
sidebar_label: HTTP Push & Pull - Introduction
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will have an introduction to the HTTP Push &amp; Pull mechanism.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#http-pull">HTTP PULL</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#http-push">HTTP PUSH</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="756112d048816ba63b28769a87e185ce">In this lesson, we will get an insight into the HTTP Push &amp; Pull mechanism. We know that the majority of the communication on the web happens over <em>HTTP</em>, especially wherever the client-server architecture is involved.</p>
<p data-id="9eb7e6052f3c1fde253ff508accfb9d4">There are two modes of data transfer between the client and the server. <em>HTTP PUSH</em> &amp; <em>HTTP PULL</em>.
Let’s find out what they are &amp; what they do.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="http-pull" data-id="f2f2160cc57ea8b4ba888d429c9bee46">HTTP PULL <a class="markdownIt-Anchor" href="#http-pull"><span class="anchor-link">#</span></a></h2>
<p data-id="378648ee486c4aaca70891fe8ce8eee6">As I stated earlier, for every response, there has to be a request first. The client sends the request &amp; the server responds with the data. This is the default mode of HTTP communication, called the HTTP PULL mechanism.</p>
<p data-id="dd04cc1672e68a38475f09e8fbd96680">The client pulls the data from the server whenever it requires. And it keeps doing it over and over to fetch the updated data.</p>
<p data-id="c3c9215223814fdd5c68a7c64d37344f">An important thing to note here is that every request to the server and the response to it consumes bandwidth. Every hit on the server costs the business money &amp; adds more load on the server.</p>
<p data-id="2dbca88960d9a5def489935346baef67">What if there is no updated data available on the server, every time the client sends a request?</p>
<p data-id="047b3230150cab76d1b0650896e08353">The client doesn’t know that, so naturally, it would keep sending the requests to the server over and over. This is not ideal &amp; a waste of resources. Excessive pulls by the clients have the potential to bring down the server.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="http-push" data-id="a5fb16595290a1c2fd94fa0c6880ecfd">HTTP PUSH <a class="markdownIt-Anchor" href="#http-push"><span class="anchor-link">#</span></a></h2>
<p data-id="ca55b26f0bd1601f9090c19b05274973">To tackle this, we have the HTTP PUSH based mechanism. In this mechanism, the client sends the request for particular information to the server, just for the first time, &amp; after that the server keeps pushing the new updates to the client whenever they are available.</p>
<p data-id="387a5ff9e11ad2c2e6ff4fc8dd6e5d78">The client doesn’t have to worry about sending requests to the server, for data, every now &amp; then. This saves a lot of network bandwidth &amp; cuts down the load on the server by notches.</p>
<p data-id="6b5b3a89e6c934c31dc85011a8e45485">This is also known as a <em>Callback</em>. Client phones the server for information. The server responds, Hey!! I don’t have the information right now but I’ll call you back whenever it is available.</p>
<p data-id="cdea3145468c30e46295a981e4c3ba2e">A very common example of this is user notifications. We have them in almost every web application today. We get notified whenever an event happens on the backend.</p>
<p data-id="736c9d00ce82247ca99613965a5d5d71">Clients use <em>AJAX (Asynchronous JavaScript &amp; XML)</em> to send requests to the server in the HTTP Pull based mechanism.</p>
<p data-id="b23d74870ba4f09e6dd5fea581b4373a">There are multiple technologies involved in the <em>HTTP Push</em> based mechanism such as:</p>
<ul data-id="0ad752f28c99ece073ba0e4f4e360095">
<li><em>Ajax Long polling</em></li>
<li><em>Web Sockets</em></li>
<li><em>HTML5 Event Source</em></li>
<li><em>Message Queues</em></li>
<li><em>Streaming over HTTP</em></li>
</ul>
<p data-id="5cdb7a5b60bbb739baf5c9459427354c">We’ll go over all of them in detail up-next.</p>
</div></div></div></div></div></div></div></div></div>