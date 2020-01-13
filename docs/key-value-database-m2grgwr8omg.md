---
id: key-value-database-m2grgwr8omg
title: Key Value Database
sidebar_label: Key Value Database
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will get to know about the Key-Value database and when to choose it for our projects.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-key-value-database">What Is A Key Value Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#features-of-a-key-value-database">Features Of A Key Value Database</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#popular-key-value-databases">Popular Key Value Databases</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#when-do-i-pick-a-key-value-database">When Do I Pick A Key Value Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-life-implementations">Real Life Implementations</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-key-value-database" data-id="95daa3e353f4c6b8775190f6fe390910">What Is A Key Value Database? <a class="markdownIt-Anchor" href="#what-is-a-key-value-database"><span class="anchor-link">#</span></a></h2>
<p data-id="e1c2b141807ee32a4083052cc3d0b714"><em>Key-value</em> databases also are a part of the <em>NoSQL family</em>. These databases use a simple <em>key-value</em> method to store and quickly fetch the data with minimum latency.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="features-of-a-key-value-database" data-id="99f99b9581515d900e29f7f7aea2aab5">Features Of A Key Value Database <a class="markdownIt-Anchor" href="#features-of-a-key-value-database"><span class="anchor-link">#</span></a></h2>
<p data-id="110237e1de4e2a6e7546a0ec9871bc28">A primary use case of a <em>Key-value</em> database is to implement caching in applications due to the minimum latency they ensure.</p>
<p data-id="4d1577293e5e8493bc8bc1133e157dec">The <em>Key</em> serves as a unique identifier and has a <em>value</em> associated with it. The value can be as simple as a block of text &amp; can be as complex as an object graph.</p>
<p data-id="8d00abe6d310a488b3f77069a8ee8d29">The data in <em>Key-value</em> databases can be fetched in <em>constant time O(1)</em>, there is no query language required to fetch the data. It’s just a simple no-brainer fetch operation. This ensures minimum latency.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="popular-key-value-databases" data-id="0ee10950d46a3dcb514ec4ad23407ea9">Popular Key Value Databases <a class="markdownIt-Anchor" href="#popular-key-value-databases"><span class="anchor-link">#</span></a></h2>
<p data-id="4a85974f7300aa2cd07d495de965e86a">Some of the popular <em>key-value</em> data stores used in the industry are <em>Redis</em>, <em>Hazelcast</em>, <em>Riak</em>, <em>Voldemort</em> &amp; <em>Memcache</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="when-do-i-pick-a-key-value-database" data-id="a75dd0ae0390ef4674f541de7237ba8e">When Do I Pick A Key Value Database? <a class="markdownIt-Anchor" href="#when-do-i-pick-a-key-value-database"><span class="anchor-link">#</span></a></h2>
<p data-id="4f0e38228689db1d80262e5046cd3f5e">If you have a use case where you need to fetch data real fast with minimum fuss &amp; backend processing then you should pick a <em>key-value</em> data store.</p>
<p data-id="b6f7edfbe2db57afb09486d36b3e0291"><em>Key-value</em> stores are pretty efficient in pulling off scenarios where super-fast data fetch is the order of the day.</p>
<p data-id="2203b77994f6f952adc28a10b514eae4">Typical use cases of a <em>key value</em> database are the following:</p>
<ul data-id="c0c3a05d354bd2112e43713c45dc4afd">
<li>Caching</li>
<li>Persisting user state</li>
<li>Persisting user sessions</li>
<li>Managing real-time data</li>
<li>Implementing queues</li>
<li>Creating leaderboards in online games &amp; web apps</li>
<li>Implementing a pub-sub system</li>
</ul>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-life-implementations" data-id="4a3328dc5b6d054ca0d10e3f5b389a32">Real Life Implementations <a class="markdownIt-Anchor" href="#real-life-implementations"><span class="anchor-link">#</span></a></h2>
<p data-id="97ec9cc33bc3966d0f82c6d69d2f1db8"><em>Some of the real-life implementations of the tech are -</em></p>
<ul data-id="554b5848dcb4e765ee014beaf09e6229">
<li>
<p><a href="https://redislabs.com/customers/inovonics/" target="_blank">Inovonics uses Redis to drive real-time analytics on millions of sensor data</a></p>
</li>
<li>
<p><a href="https://redislabs.com/docs/microsoft-relies-redis-labs/" target="_blank">Microsoft uses Redis to handle the traffic spike on its platforms</a></p>
</li>
<li>
<p><a href="https://cloud.google.com/appengine/docs/standard/python/memcache/" target="_blank">Google Cloud uses Memcache to implement caching on their cloud platform</a></p>
</li>
</ul>
</div></div></div></div></div></div></div></div></div>