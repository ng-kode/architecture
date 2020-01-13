---
id: introduction-q2pkd39rk3r
title: Introduction
sidebar_label: Introduction
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will get introduced to the concept of caching and why it is important for performance.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-caching">What Is Caching?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#caching-dynamic-data">Caching Dynamic Data</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#caching-static-data">Caching Static Data</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="b86ef11b79a69d718a32f0e75b712617">Hmmm… before beginning with this lesson, I want to ask you a question. When you visit a website and request certain data from the server. How long do you wait for the response?</p>
<p data-id="7a66cb24812917aee31d6d5bb623d2a0">5 seconds, 10 seconds, 15 seconds, 30 seconds? I know, I know, I am pushing it… 45? What? Still no response…</p>
<p data-id="8226bc3e5591915407f70de54c3aaeed">And then you finally bounce off &amp; visit another website for your answer. We are impatient creatures; we need our answers quick. This makes caching vital to applications to prevent users from bouncing off to other websites, all the time.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-caching" data-id="6058d6746885b8a7f91182122ce271ce">What Is Caching? <a class="markdownIt-Anchor" href="#what-is-caching"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="322e17668d607703de17bdeff5b3bd72">
<p><em>Caching</em> is key to the performance of any kind of application. It ensures <em>low latency</em> and <em>high throughput</em>. An application with caching will certainly do better than an application without caching, simply because it returns the response in less time as opposed to the application without a cache implemented.</p>
</blockquote>
<p data-id="9f82827ad8a4b2d61871d4967fd98d29">Implementing caching in a web application simply means copying frequently accessed data from the database which is <em>disk-based</em> hardware and storing it in <em>RAM Random Access Memory</em> hardware.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5177501393354752_image_4722653954834432.jpeg" alt=""></p>
<p data-id="942def439451e8a2c5936aa7e3b9feb7"><em>RAM-based</em> hardware provides faster access than the disk-based hardware. As I said earlier it ensures low latency and high throughput.
Throughput means the number of network calls i.e. <em>request-response</em> between the client and the server within a stipulated time.</p>
<p data-id="54f2c057730506857915b7829f97da55"><em>RAM-based</em> hardware is capable of handling more requests than the <em>disk-based</em> hardware, on which the databases run.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="caching-dynamic-data" data-id="a5c797f9ed3029c0bccd1867f75853c4">Caching Dynamic Data <a class="markdownIt-Anchor" href="#caching-dynamic-data"><span class="anchor-link">#</span></a></h2>
<p data-id="6f0fab1c0da9eb64f2a5d67292d1f31c">With caching we can cache both the <em>static</em> data and the <em>dynamic</em> data. Dynamic data is the data which changes more often, it has an expiry time or a <em>TTL</em> “Time To Live”. After the <em>TTL</em> ends, the data is purged from the cache and the newly updated data is stored in it. This process is known as <em>Cache Invalidation</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="caching-static-data" data-id="4272972903cd5bbf5324ec175a8c16fa">Caching Static Data <a class="markdownIt-Anchor" href="#caching-static-data"><span class="anchor-link">#</span></a></h2>
<p data-id="2c03011fe29d7841c67a6e9870dfff97"><em>Static</em> data consists of images, font files, CSS &amp; other similar files. This is the kind of data which doesn’t change often &amp; can easily be cached on the client-side in the browser or their local memory. Also, on the CDNs the Content Delivery Networks.</p>
<p data-id="772158d8cdacc302dcb3575718fa870a">Caching also helps applications maintain their expected behaviour during network interruptions.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="5c088edb8ec085ff8f0efbf295e96515">In the next lesson, let’s understand how do we figure if we really need a cache in our applications?</p>
</div></div></div></div></div></div></div></div></div>