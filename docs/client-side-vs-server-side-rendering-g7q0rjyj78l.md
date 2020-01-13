---
id: client-side-vs-server-side-rendering-g7q0rjyj78l
title: Client-Side Vs Server-Side Rendering
sidebar_label: Client-Side Vs Server-Side Rendering
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the client side and the server-side rendering &amp; the use cases for both the approaches.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#client-side-rendering-how-does-a-browser-render-a-web-page">Client-Side Rendering - How Does A Browser Render A Web Page?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#server-side-rendering">Server-Side Rendering</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#use-cases-for-server-side-client-side-rendering">Use Cases For Server-Side &amp; Client-Side Rendering</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="client-side-rendering-how-does-a-browser-render-a-web-page" data-id="38d39861d6714ce7640b22981aec3676">Client-Side Rendering - How Does A Browser Render A Web Page? <a class="markdownIt-Anchor" href="#client-side-rendering-how-does-a-browser-render-a-web-page"><span class="anchor-link">#</span></a></h2>
<p data-id="030f24231f687da741676fd9df9689e3">When a user requests a web page from the server &amp; the browser receives the response. It has to render the response on the window in the form of an HTML page.</p>
<p data-id="718b2fe47e710108f48c429d65936c0a">For this, the browser has several components, such as the:</p>
<ul data-id="4034d466665ac4b98e6842929815b985">
<li><em>Browser engine</em></li>
<li><em>Rendering engine</em></li>
<li><em>JavaScript interpreter</em></li>
<li><em>Networking &amp; the UI backend</em></li>
<li><em>Data storage</em> etc.</li>
</ul>
<p data-id="9ea2ff69893da6cd040e275b77b942f0">I won’t go into much detail but the browser has to do a lot of work to convert the response from the server into an HTML page.</p>
<p data-id="6257252a582a438415570bd8e83fa291">The rendering engine constructs the <em>DOM</em> tree, renders &amp; paints the construction. And naturally, all this activity needs a bit of time.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="server-side-rendering" data-id="bee2bbeda1242252e770d636dacc9565">Server-Side Rendering <a class="markdownIt-Anchor" href="#server-side-rendering"><span class="anchor-link">#</span></a></h2>
<p data-id="4618f28bcbe7727b667a8e05c6dc1c70">To avoid all this rendering time on the client, developers often render the UI on the server, generate HTML there &amp; directly send the HTML page to the UI.</p>
<p data-id="9e4178158eeef19e581667cd913c4262">This technique is known as the <em>Server-side rendering</em>. It ensures faster rendering of the UI, averting the UI loading time in the browser window since the page is already created &amp; the browser doesn’t have to do much assembling &amp; rendering work.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="use-cases-for-server-side-client-side-rendering" data-id="7bf7ec4444e1b1cc238a5a41a5f7ca4d">Use Cases For Server-Side &amp; Client-Side Rendering <a class="markdownIt-Anchor" href="#use-cases-for-server-side-client-side-rendering"><span class="anchor-link">#</span></a></h2>
<p data-id="2770d254cf52736774d5a542af6dae6f">The server-side rendering approach is perfect for delivering static content, such as WordPress blogs. It’s also good for SEO as the crawlers can easily read the generated content.</p>
<p data-id="e3c0b0c25afb209530e9a758cf70123f">However, the modern websites are highly dependent on Ajax. In such websites, content for a particular module or a section of a page has to be fetched &amp; rendered on the fly.</p>
<p data-id="8b8cc6b5646a1d79acba3218928812af">Therefore, server-side rendering doesn’t help much. For every Ajax-request, instead of sending just the required content to the client, the approach generates the entire page on the server. This process consumes unnecessary bandwidth &amp; also fails to provide a smooth user experience.</p>
<p data-id="2809ca201a267fd2f918019ef19fd0bf">A big downside to this is once the number of concurrent users on the website rises, it puts an unnecessary load on the server.</p>
<p data-id="bd4fd7b1dc0f7aeab95d39067555f68e"><em>Client-side rendering</em> works best for modern dynamic Ajax-based websites.</p>
<p data-id="c3e09437123bea2abd5206edfea0a2bc">Though we can leverage a hybrid approach, to get the most out of both techniques. We can use server-side rendering for the home page &amp; for the other static content on our website &amp; use client-side rendering for the dynamic pages.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="f91eb5be6a60a53b923086f245cbf9c0">Alright, before moving down to the database, message queue &amp; the caching components. It’s important for us to understand a few concepts such as:</p>
<ul data-id="1d0ce4f7c836f47722737399b5265e84">
<li><em>Monolithic architecture</em></li>
<li><em>Micro-services</em></li>
<li><em>Scalability</em></li>
<li><em>High availability</em></li>
<li><em>Distributed systems</em></li>
<li><em>What are nodes in distributed systems? Why are they important to software design?</em></li>
</ul>
<p data-id="0bba6691bb1ca8befe8094ea102d5d14">The clarity on these concepts will help us understand the rest of the web components better.
Let’s have a look one by one.</p>
</div></div></div></div></div></div></div></div></div>