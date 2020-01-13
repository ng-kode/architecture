---
id: http-push-ym9l8lxn530
title: HTTP Push
sidebar_label: HTTP Push
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the HTTP Push mechanism.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#time-to-live-ttl">Time To Live (TTL)</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#persistent-connection">Persistent Connection</a></li>
<li><a href="#heartbeat-interceptors">Heartbeat Interceptors</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#resource-intensive">Resource Intensive</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="time-to-live-ttl" data-id="7e4d89e13ed122522064412c61e3976c">Time To Live (TTL) <a class="markdownIt-Anchor" href="#time-to-live-ttl"><span class="anchor-link">#</span></a></h2>
<p data-id="33e0137e9914158cf816ccace1da298b">In the regular client-server communication, which is <em>HTTP PULL</em>, there is a <em>Time to Live (TTL)</em> for every request. It could be 30 secs to 60 secs, varies from browser to browser.</p>
<p data-id="103d9ca45946a27d8fdbfcd78dd4769a">If the client doesn’t receive a response from the server within the TTL, the browser kills the connection &amp; the client has to re-send the request hoping it would receive the data from the server before the TTL ends this time.</p>
<p data-id="6cb02ec85d56b2a227df007c34c57239">Open connections consume resources &amp; there is a limit to the number of open connections a server can handle at one point in time. If the connections don’t close &amp; new ones are being introduced, over time, the server will run out of memory. Hence, the TTL is used in client-server communication.</p>
<p data-id="dddf11725372c8878d0e463a533ee421"><em>But what if we are certain that the response will take more time than the TTL set by the browser?</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="persistent-connection" data-id="6488794d1740706053c9700bfc9b7be2">Persistent Connection <a class="markdownIt-Anchor" href="#persistent-connection"><span class="anchor-link">#</span></a></h2>
<p data-id="a3bb6c4ba57364db0535352765ba8a63">In this case, we need a <em>Persistent Connection</em> between the client and the server.</p>
<blockquote data-id="d39b476c3d767ae9b82c71943afbf3e4">
<p>A persistent connection is a network connection between the client &amp; the server that remains open for further requests &amp; the responses, as opposed to being closed after a single communication.</p>
</blockquote>
<p data-id="8d4ec36121870748ef3ac0538c648945">It facilitates HTTP Push-based communication between the client and the server.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5285870967980032_image_5102209878458368.jpeg" alt=""></p>
<h2 id="heartbeat-interceptors" data-id="6653507d7bc53a5f7876d71d72e0400b">Heartbeat Interceptors <a class="markdownIt-Anchor" href="#heartbeat-interceptors"><span class="anchor-link">#</span></a></h2>
<p data-id="01944a938348525f7b8032a9e54ade11"><em>Now you might be wondering how is a persistent connection possible if the browser kills the open connections to the server every X seconds?</em></p>
<p data-id="26b55a7312cfe48bcf318e4c67482771">The connection between the client and the server stays open with the help of <em>Heartbeat Interceptors</em>.</p>
<blockquote data-id="3424c161fc9c0287432798c3643d24d8">
<p>These are just blank request responses between the client and the server to prevent the browser from killing the connection.</p>
</blockquote>
<p data-id="34d72ffcd56ccc1d0af653ef306dc289"><em>Isn’t this resource-intensive?</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="resource-intensive" data-id="eb49e48b4acbbc22c288b36d8385752e">Resource Intensive <a class="markdownIt-Anchor" href="#resource-intensive"><span class="anchor-link">#</span></a></h2>
<p data-id="3e11474080aeb394a46c7c7296bcbcbc">Yes, it is. Persistent connections consume a lot of resources in comparison to the HTTP Pull behaviour. But there are use cases where establishing a persistent connection is vital to the feature of an application.</p>
<p data-id="6fdc260657bcb575eb7243d8ef9f1edd">For instance, a browser-based multiplayer game has a pretty large amount of request-response activity within a certain time in comparison to a regular web application.</p>
<p data-id="6d9284dec63390d9cc71bdf31c8a408e">It would be apt to establish a persistent connection between the client and the server from a user experience standpoint.</p>
<p data-id="e76107c3873decfad6b58dc31e7d2510">Long opened connections can be implemented by multiple techniques such as <em>Ajax Long Polling</em>, <em>Web Sockets</em>, <em>Server-Sent Events</em> etc.</p>
<p data-id="b17265337adecaebb5de01ef43ec12c8">Let’s have a look into each of them.</p>
</div></div></div></div></div></div></div></div></div>