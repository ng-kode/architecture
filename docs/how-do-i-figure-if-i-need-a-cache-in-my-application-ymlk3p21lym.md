---
id: how-do-i-figure-if-i-need-a-cache-in-my-application-ymlk3p21lym
title: How Do I figure If I Need A Cache In My Application?
sidebar_label: How Do I figure If I Need A Cache In My Application?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss how to tell if we need caching in our application.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#different-components-in-the-application-architecture-where-the-cache-can-be-used">Different Components In the Application Architecture Where the Cache Can Be Used</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="262d7884da62cf56e169aa51a71c179b">First up, it’s always a good idea to use a cache as opposed to not using it. It doesn’t do any harm. It can be used at any layer of the application &amp; there are no ground rules as to where it can and cannot be applied.</p>
<p data-id="c24e56598a697ae4712738802993cfd0">The most common usage of caching is database caching. Caching helps alleviate the stress on the database by intercepting the requests being routed to the database for data.</p>
<p data-id="757158bbd4cc24b2c908fcaa32d5246f">The cache then returns all the frequently accessed data. Thus, cutting down the load on the database by notches.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="different-components-in-the-application-architecture-where-the-cache-can-be-used" data-id="b782e127a8edec932988108ee994f3f4">Different Components In the Application Architecture Where the Cache Can Be Used <a class="markdownIt-Anchor" href="#different-components-in-the-application-architecture-where-the-cache-can-be-used"><span class="anchor-link">#</span></a></h2>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5376897221394432_image_6038989893009408.jpeg" alt=""></p>
<p data-id="6a9f9ca3fe4c5670121862d2647aad37">Across the architecture of our application, we can use caching at multiple places. Caching is used in the client browser to cache static data. It is used with the database to intercept all the data requests, in the REST API implementation etc.</p>
<p data-id="113d64a63f9def7f5ebf16f30ea9ac0d">Besides these places, I would suggest you to look for patterns. We can always cache the frequently accessed content on our website, be it from any component. There is no need to compute stuff over and over when it can be cached.</p>
<p data-id="fb429c521713a81ae73f985e4e50a274">Think of <em>Joins</em> in relational databases. They are notorious for making the response slow. More <em>Joins</em> means more latency. A cache can avert the need for running <em>joins</em> every time just by storing the data in demand. Now imagine how much would this mechanism speed up our application.</p>
<p data-id="820c7ded44e1bc7259719c9ae30b8663">Also, even if the database goes down for a while. The users won’t notice it as the cache would continue to serve the data requests.</p>
<p data-id="357f5e3994c86d1e001f1e2666b42304">Caching is also the core of the <em>HTTP</em> protocol. <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching" target="_blank">This is a good resource to read more about it.</a></p>
<p data-id="e69388e58513c742d8a58d8a4bf1a07c">We can store user sessions in a cache. It can be implemented at any layer of an application be it at the OS level, at the network level, CDN or the database.</p>
<p data-id="01e6f9e07694880700f14cd2112db594">You might remember, we talked about the <em>Key-value</em> data stores in the database lesson. They are primarily used to implement caching in web applications.</p>
<p data-id="d12b241f95631ba247e8b532d2c95d0a">They can be used for <em>cross-module communication</em> in a <em>microservices</em> architecture by saving the shared data which is commonly accessed by all the services. It acts as a backbone for the <em>microservice</em> communication.</p>
<p data-id="aef815b7c10775f4a3e0f736bb320afe"><em>Key-value</em> data stores via caching are also widely used in <em>in-memory data stream processing</em> and running <em>analytics</em>.</p>
</div></div></div></div></div></div></div></div></div>