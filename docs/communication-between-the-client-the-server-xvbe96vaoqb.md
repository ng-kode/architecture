---
id: communication-between-the-client-the-server-xvbe96vaoqb
title: Communication Between the Client & the Server
sidebar_label: Communication Between the Client & the Server
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn how communication takes place between the Client and the Server.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#request-response-model">Request-Response Model</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#http-protocol">HTTP Protocol</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#rest-api-api-endpoints">REST API &amp; API Endpoints</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-world-example-of-using-a-rest-api">Real World Example Of Using A REST API</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="request-response-model" data-id="18f0b8727fed882d9e7266cef7233efc">Request-Response Model <a class="markdownIt-Anchor" href="#request-response-model"><span class="anchor-link">#</span></a></h2>
<p data-id="b0b28233229014169c99beeeb5a66530">The client &amp; the server have a <em>request-response</em> model. The client sends the request &amp; the server responds with the data.</p>
<p data-id="1980b60b156fc14a36e0879910cae0aa">If there is no request, there is no response. Pretty simple right?</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="http-protocol" data-id="4ae6aa7feddb31ee760ab6cfffd69c88">HTTP Protocol <a class="markdownIt-Anchor" href="#http-protocol"><span class="anchor-link">#</span></a></h2>
<p data-id="2e0787183a7ac78a40bd78c045010f9c">The entire communication happens over the <em>HTTP</em> protocol. It is the protocol for data exchange over the World Wide Web. <em>HTTP</em> protocol is a <em>request-response</em> protocol that defines how information is transmitted across the web.</p>
<p data-id="ae7b13c180a58962316752f19cf62b7c">It’s a <em>stateless</em> protocol, every process over HTTP is executed independently &amp; has no knowledge of previous processes.</p>
<p data-id="1f5d841ce74a49deec57f1864d3eed94">If you want to read more about the protocol, <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview" target="_blank">this is a good resource on it</a></p>
<p data-id="7b506ee0b1c597c892e0f260c444d112">Alright, moving on…</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="rest-api-api-endpoints" data-id="2118753b831ea618fbeacd9313b29956">REST API &amp; API Endpoints <a class="markdownIt-Anchor" href="#rest-api-api-endpoints"><span class="anchor-link">#</span></a></h2>
<p data-id="5eb8501488897825d0084842816ff2e3">Speaking from the context of modern N-tier web applications, every client has to hit a <em>REST end-point</em> to fetch the data from the backend.</p>
<blockquote data-id="69fe3031a18768fdf04a56f103d03cff">
<p><strong>Note:</strong> If you aren’t aware of the REST API &amp; the API Endpoints, I have discussed it in the next lesson in detail. I’ve brought up the terms in this lesson, just to give you a heads up on how modern distributed web applications communicate.</p>
</blockquote>
<p data-id="c580444c3c12f334ba1c9673e684aba4">The backend application code has a <em>REST-API</em> implemented which acts as an interface to the outside world requests. Every request be it from the client written by the business or the third-party developers which consume our data have to hit the REST-endpoints to fetch the data.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5853088743161856_image_5780359385972736.jpeg" alt=""></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-world-example-of-using-a-rest-api" data-id="0761e99b3cfbe13b08538a086bbb4388">Real World Example Of Using A REST API <a class="markdownIt-Anchor" href="#real-world-example-of-using-a-rest-api"><span class="anchor-link">#</span></a></h2>
<p data-id="3b67003419dee12ec96a454a472260df">For instance, let’s say we want to write an application which would keep track of the birthdays of all our Facebook friends &amp; send us a reminder a couple of days before the event date.</p>
<p data-id="9c8291ecb9477d556e21b9fce2ab9353">To implement this, the first step would be to get the data on the birthdays of all our Facebook friends.</p>
<p data-id="61af4c3145116eb788c8149a2b88857c">We would write a client which would hit the Facebook Social Graph API which is a REST-API to get the data &amp; then run our business logic on the data.</p>
<p data-id="7f7c030255da4db8e888c0fbd7e77bef">Implementing a REST-based API has several advantages. Let’s delve into it in detail to have a deeper understanding.</p>
</div></div></div></div></div></div></div></div></div>