---
id: http-push-based-technologies-xlx9bqwpvll
title: HTTP Push-Based Technologies
sidebar_label: HTTP Push-Based Technologies
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss some HTTP Push based technologies.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#web-sockets">Web Sockets</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#ajax-long-polling">AJAX – Long Polling</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#html5-event-source-api-server-sent-events">HTML5 Event Source API &amp; Server Sent Events</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#streaming-over-http">Streaming Over HTTP</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#summary">Summary</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="web-sockets" data-id="c60b30a8f4ed0f20fe8027807e8f949a">Web Sockets <a class="markdownIt-Anchor" href="#web-sockets"><span class="anchor-link">#</span></a></h2>
<p data-id="56a3b61684efda57df0c593489be953e">A <em>Web Socket</em> connection is ideally preferred when we need a persistent <em>bi-directional low latency</em> data flow from the client to server &amp; back.</p>
<p data-id="85219eaf2d26888fd6bdc474643ed2a8">Typical use-cases of these are messaging, chat applications, real-time social streams &amp; browser-based massive multiplayer games which have quite a number of read writes in comparison to a regular web app.</p>
<p data-id="5ca4e3a40e9df4ce324038468c07c3e3">With Web Sockets, we can keep the client-server connection open as long as we want.</p>
<p data-id="cc1cea2f41283d1f1e493037b327fa0d"><strong>Have bi-directional data?</strong> Go ahead with Web Sockets. One more thing, Web Sockets tech doesn’t work over <em>HTTP</em>. It runs over <em>TCP</em>. The server &amp; the client should both support web sockets or else it won’t work.</p>
<p data-id="99264f70ea3bb13249352ec2724f304f"><a href="https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API" target="_blank">The WebSocket API</a> &amp; <a href="https://www.html5rocks.com/en/tutorials/websockets/basics/" target="_blank">Introducing WebSockets – Bringing Sockets to the Web</a> are good resources for further reading on web sockets</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="ajax-long-polling" data-id="917762485db56996f456ceadb967d367">AJAX – Long Polling <a class="markdownIt-Anchor" href="#ajax-long-polling"><span class="anchor-link">#</span></a></h2>
<p data-id="d46fe42a6993ee7318f817ac6fd57603"><em>Long Polling</em> lies somewhere between <em>Ajax</em> &amp; <em>Web Sockets</em>. In this technique instead of immediately returning the response, the server holds the response until it finds an update to be sent to the client.</p>
<p data-id="51e330a8acc2408f70d99de8760b144f">The connection in long polling stays open a bit longer in comparison to polling. The server doesn’t return an empty response. If the connection breaks, the client has to re-establish the connection to the server.</p>
<p data-id="fe08283e751b719975ecd9c8b12c67a9">The upside of using this technique is that there are quite a smaller number of requests sent from the client to the server, in comparison to the regular polling mechanism. This reduces a lot of network bandwidth consumption.</p>
<p data-id="f529a90d97b982b87678ad0ac5ff9106">Long polling can be used in simple asynchronous data fetch use cases when you do not want to poll the server every now &amp; then.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="html5-event-source-api-server-sent-events" data-id="f18d4c68ac9bf0cea9727fd7fa36a56b">HTML5 Event Source API &amp; Server Sent Events <a class="markdownIt-Anchor" href="#html5-event-source-api-server-sent-events"><span class="anchor-link">#</span></a></h2>
<p data-id="24ce3ecaa5568cf74046b62260803927">The <em>Server-Sent Events</em> implementation takes a bit of a different approach. Instead of the client polling for data, the server automatically pushes the data to the client whenever the updates are available. The incoming messages from the server are treated as <em>Events</em>.</p>
<p data-id="26ed0b1fd010272b5fc5326a6a68c6c7">Via this approach, the servers can initiate data transmission towards the client once the client has established the connection with an initial request.</p>
<p data-id="c4d185b0fc37cf4db2d4ac353640c124">This helps in getting rid of a huge number of blank request-response cycles cutting down the bandwidth consumption by notches.</p>
<p data-id="64a56ae5edfe6869ffd9c57ad71cad82">To implement server-sent events, the backend language should support the technology &amp; on the UI <em>HTML5 Event source API</em> is used to receive the data in-coming from the backend.</p>
<p data-id="61115db2d8605574b20d142cbd55e625">An important thing to note here is that once the client establishes a connection with the server, the data flow is in one direction only, that is from the server to the client.</p>
<p data-id="b070e775ab6fe788cc19a035898d1dae">SSE is ideal for scenarios such as a real-time feed like that of Twitter, displaying stock quotes on the UI, real-time notifications etc.</p>
<p data-id="8098ce4599596c6b5d96a1f446936891"><a href="https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events" target="_blank">This is a good resource for further reading on SSE</a></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="streaming-over-http" data-id="e60434f49c3c1aad133b33d3a2ec2f8a">Streaming Over HTTP <a class="markdownIt-Anchor" href="#streaming-over-http"><span class="anchor-link">#</span></a></h2>
<p data-id="ce8a7a38b28328c6b31be486c736d13a"><em>Streaming Over HTTP</em> is ideal for cases where we need to stream large data over HTTP by breaking it into smaller chunks. This is possible with <em>HTML5</em> &amp; a <em>JavaScript Stream API</em>.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5272067177971712_image_5628092083077120.jpeg" alt=""></p>
<p data-id="2721b46ce607aa551270db41198e7868">The technique is primarily used for streaming multimedia content, like large images, videos etc, over HTTP.</p>
<p data-id="d5c82dd7f068c1462ba14c1dd3d22087">Due to this, we can watch a partially downloaded video as it continues to download, by playing the downloaded chunks on the client.</p>
<p data-id="b5ad24eef15f388004364ae8568a1bfe">To stream data, both the client &amp; the server agree to conform to some streaming settings. This helps them figure when the stream begins &amp; ends over an HTTP request-response model.</p>
<p data-id="6a33cf9e6fd405e33fc05444b657de99"><a href="https://developer.mozilla.org/en-US/docs/Web/API/Streams_API/Concepts" target="_blank">You can go through this resource for further reading on Stream API</a></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="summary" data-id="5312305a09f2445c0e1dfee8124a628f">Summary <a class="markdownIt-Anchor" href="#summary"><span class="anchor-link">#</span></a></h2>
<p data-id="c170283872a0781d85a945950a67d0f6">So, now we have an understanding of what <em>HTTP Pull</em> &amp; <em>Push</em> is. We went through different technologies which help us establish a persistent connection between the client and the server.</p>
<p data-id="14936a389dd9f639ae5514fc38a25717">Every tech has a specific use case, Ajax is used to dynamically update the web page by polling the server at regular intervals.</p>
<p data-id="293e6b5817df995efe850edb8ff4fde9">Long polling has a connection open time slightly longer than the polling mechanism.</p>
<p data-id="c98fe1dbd37439b27e6ea5c5115c90d1">Web Sockets have bi-directional data flow, whereas Server sent events facilitate data flow from the server to the client.</p>
<p data-id="b1fc577ba6b4eb81a0fa873d302483bc">Streaming over HTTP facilitates streaming of large objects like multi-media files.</p>
<p data-id="0c66f4c9a0d6bc93455d3b3ba96e8c90">What tech would fit best for our use cases depends on the kind of application we intend to build.</p>
<p data-id="5ca7672acc9341ecafa2274c9922355c">Alright, let’s quickly gain an insight into the pros &amp; cons of the client and the server-side rendering.</p>
</div></div></div></div></div></div></div></div></div>