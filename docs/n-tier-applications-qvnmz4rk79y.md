---
id: n-tier-applications-qvnmz4rk79y
title: N Tier Applications
sidebar_label: N Tier Applications
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will go over the N Tier applications and its components. </p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#n-tier-application">N-Tier Application</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#why-the-need-for-so-many-tiers">Why The Need For So Many Tiers?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#single-responsibility-principle">Single Responsibility Principle</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#separation-of-concerns">Separation Of Concerns</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#difference-between-layers-tiers">Difference Between Layers &amp; Tiers</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="n-tier-application" data-id="582b0c269e1d7640067b4d5db2f2b31f">N-Tier Application <a class="markdownIt-Anchor" href="#n-tier-application"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="422164a00d8c5c7bda576e7aacde022d">
<p>An <em>N-tier</em> application is an application which has more than three components involved.</p>
</blockquote>
<p data-id="e30a36a15b21364143c051454c84cb18">What are those components?</p>
<ul data-id="e401ebf716684689d2f9c418ce21d01c">
<li><em>Cache</em></li>
<li><em>Message queues for asynchronous behaviour</em></li>
<li><em>Load balancers</em></li>
<li><em>Search servers for searching through massive amounts of data</em></li>
<li><em>Components involved in processing massive amounts of data</em></li>
<li><em>Components running heterogeneous tech commonly known as web services</em> etc.</li>
</ul>
<p data-id="c211e88a2e2cb1b5f1b21e092c633868">All the social applications like <em>Instagram</em>, <em>Facebook</em>, large scale industry services like <em>Uber</em>, <em>Airbnb</em>, online massive multiplayer games like <em>Pokemon Go</em>, applications with fancy features are <em>n-tier</em> applications.</p>
<blockquote data-id="70b955cd1ef32e6235ae5c9497417e40">
<p><strong>Note:</strong> There is another name for n-tier apps, the “<strong>distributed applications</strong>”. But, I think it’s not safe to use the word “<em>distributed</em>” yet, as the term <em>distributed</em> brings along a lot of complex stuff with it. It would rather confuse us than help. Though I will discuss the <em>distributed architecture</em> in this course, for now, we will just stick with the term <strong>N-tier applications</strong>.</p>
</blockquote>
<p data-id="370955f2223d02a573abf1085ae0bf70"><em>So, why the need for so many tiers?</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="why-the-need-for-so-many-tiers" data-id="411a51558c60a7d1ae533daaeb447a7b">Why The Need For So Many Tiers? <a class="markdownIt-Anchor" href="#why-the-need-for-so-many-tiers"><span class="anchor-link">#</span></a></h2>
<p data-id="a24006b3502556f8b631500e53b69efd">Two software design principles that are key to explaining this are the <em>Single Responsibility Principle</em> &amp; the <em>Separation of Concerns</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="single-responsibility-principle" data-id="abc0aae8822094ba908900619c750571">Single Responsibility Principle <a class="markdownIt-Anchor" href="#single-responsibility-principle"><span class="anchor-link">#</span></a></h2>
<p data-id="11e870983f93b337989f88a41e987713"><strong>Single Responsibility Principle</strong> simply means giving one, just one responsibility to a component &amp; letting it execute it with perfection. Be it saving data, running the application logic or ensuring the delivery of the messages throughout the system.</p>
<p data-id="0f83bfa1030e36bc58327849ee72c65b">This approach gives us a lot of flexibility &amp; makes management easier.</p>
<p data-id="4e6f0281505ccf0225be3264f15a8a58">For instance, when upgrading a <em>database</em> server.
Like when installing a new <em>OS</em> or a patch, it wouldn’t impact the other components of the service running &amp; even if something amiss happens during the OS installation process, just the database component would go down. The application as a whole would still be up &amp; would only impact the features requiring the database.</p>
<p data-id="512750fc29954c9457193da4db22d4b9">We can also have dedicated teams &amp; code repositories for every component, thus keeping things cleaner.</p>
<p data-id="6df54580fa50122a9cc0cfea82154b18"><em>Single responsibility principle</em> is a reason, why I was never a fan of <em>stored procedures</em>.</p>
<p data-id="f4143b81540ef3f63340ae8c40d30def">Stored procedures enable us to add business logic to the database, which is a big no for me. What if in future we want to plug in a different database? Where do we take the business logic? To the new database? Or do we try to refactor the application code &amp; squeeze in the stored procedure logic somewhere?</p>
<p data-id="d521bb93a982908e6121a9e5db0761f3">A database should not hold business logic, it should only take care of persisting the data. This is what the <em>single responsibility principle</em> is. And this is why we have separate <em>tiers</em> for separate components.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="separation-of-concerns" data-id="c441ae395d892497395b73eee544a3c0">Separation Of Concerns <a class="markdownIt-Anchor" href="#separation-of-concerns"><span class="anchor-link">#</span></a></h2>
<p data-id="199b8e1809586a7926f934957a640e02"><strong>Separation of concerns</strong> kind of means the same thing, be concerned about your work only &amp; stop worrying about the rest of the stuff.</p>
<p data-id="2e861e3d0ad3baa3e5fcd4ae17b14252">These principles act at all the levels of the service, be it at the tier level or the code level.</p>
<p data-id="11622197bc19ac61f414d743a1417fc8">Keeping the components separate makes them reusable. Different services can use the same database, the messaging server or any component as long as they are not tightly coupled with each other.</p>
<p data-id="68ece49bbf7dad45b8cdf50fc5cabad4">Having loosely coupled components is the way to go. The approach makes scaling the service easy in future when things grow beyond a certain level.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="difference-between-layers-tiers" data-id="4d218ae190b6c2c331270efaaea4460d">Difference Between Layers &amp; Tiers <a class="markdownIt-Anchor" href="#difference-between-layers-tiers"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="18d694a5934e7c56202eb2f9055ec11f">
<p><strong>Note:</strong> Don’t confuse tiers with the layers of the application. Some prefer to use them interchangeably. But in the industry layers of an application typically means the <em>user interface layer</em>, <em>business layer</em>, <em>service layer</em>, or the <em>data access layer</em>.</p>
</blockquote>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_6047815849476096_image_5802038963208192.jpeg" alt=""></p>
<p data-id="5a62acc6951ec6b1ea8d718df930bac8">The layers mentioned in the illustration are at the code level. The difference between <em>layers</em> and <em>tiers</em> is that the layers represent the organization of the code and breaking it into components. Whereas, tiers involve physical separation of components.</p>
<p data-id="b0dba1c997cb4f37807d86eda3823a75">All these layers together can be used in any tiered application. Be it single, two, three or N-tier. I’ll discuss these layers in detail in the course ahead.</p>
<p data-id="d406aa42865126b9662a54f4398cc4c3">Alright, now we have an understanding of tiers. Let’s zoom-in one notch &amp; focus on web architecture.</p>
</div></div></div></div></div></div></div></div></div>