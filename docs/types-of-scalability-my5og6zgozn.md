---
id: types-of-scalability-my5og6zgozn
title: Types Of Scalability
sidebar_label: Types Of Scalability
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will explore the two types of scaling: Vertical and Horizontal Scaling.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-vertical-scaling">What is Vertical Scaling?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-is-horizontal-scaling">What is Horizontal Scaling?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#cloud-elasticity">Cloud Elasticity</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="a78698549b365866b69169e0ab7ea391">An application to scale well needs solid computing power. The servers should be powerful enough to handle increased traffic loads.</p>
<p data-id="e3caa530bfa44986111293245b95af27">There are two ways to scale an application:</p>
<ol data-id="d6a7c3d5a35053c63f0c21b8fe5dad14">
<li>Vertical Scaling</li>
<li>Horizontal Scaling</li>
</ol>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-vertical-scaling" data-id="6f6f588705a6676abd238f9c320732b8">What is Vertical Scaling? <a class="markdownIt-Anchor" href="#what-is-vertical-scaling"><span class="anchor-link">#</span></a></h2>
<p data-id="ef67e0d25fabc965c6dcc824fac9d200">Vertical scaling means adding more power to your server. Let’s say your app is hosted by a server with 16 Gigs of RAM. To handle the increased load you increase the RAM to 32 Gigs. You have vertically scaled the server.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4772974026555392_image_4645757866999808.jpeg" alt=""></p>
<p data-id="52b0ac9086264e347d5963b86063799a">Ideally, when the traffic starts to build upon your app the first step should be to scale vertically. Vertical scaling is also called <em>scaling up</em>.</p>
<p data-id="a5a62fd14aab07814d64222394d45497">In this type of scaling we increase the power of the hardware running the app. This is the simplest way to scale since it doesn’t require any code refactoring, not making any complex configurations and stuff. I’ll discuss further down the lesson, why code refactoring is required when we horizontally scale the app.</p>
<p data-id="404ff803464231723211e2ec523d1802">But there is only so much we can do when scaling vertically. There is a limit to the capacity we can augment for a single server.</p>
<p data-id="1522d29db1d622245e794188c6667fc0">A good analogy would be to think of a multi-story building we can keep adding floors to it but only upto a certain point. What if the number of people in need of a flat keeps rising? We can’t scale up the building to the moon, for obvious reasons.</p>
<p data-id="6c96dc81d9084364e2de2163ae22ca88">Now is the time to build more buildings. This is where <em>Horizontal Scalability</em> comes in.</p>
<p data-id="48af6c4ef5b24991d003f0af0ccaeead">When the traffic is just too much to be handled by single hardware, we bring in more servers to work together.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-horizontal-scaling" data-id="9ae725f3b250ab33b6c3a9932afbd685">What is Horizontal Scaling? <a class="markdownIt-Anchor" href="#what-is-horizontal-scaling"><span class="anchor-link">#</span></a></h2>
<p data-id="2fbb3016bb52c508ce27f025f595e0bf">Horizontal scaling, also known as <em>scaling out</em>, means adding more hardware to the existing hardware resource pool. This increases the computational power of the system as a whole.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4772974026555392_image_5602418949619712.jpeg" alt=""></p>
<p data-id="36a536fa947c34fb7a880fece20e781a">Now the increased traffic influx can be easily dealt with the increased computational capacity &amp; there is literally no limit to how much we can scale horizontally assuming we have infinite resources. We can keep adding servers after servers, setting up data centres after data centres.</p>
<p data-id="69633cf81f7e8064e5c0b5ddafaca335">Horizontal scaling also provides us with the ability to dynamically scale in real-time as the traffic on our website increases &amp; decreases over a period of time as opposed to vertical scaling which requires pre-planning &amp; a stipulated time to be pulled off.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="cloud-elasticity" data-id="6a9224bfeaf1ae58f88a7c9a8ff9e533">Cloud Elasticity <a class="markdownIt-Anchor" href="#cloud-elasticity"><span class="anchor-link">#</span></a></h2>
<p data-id="6bccb199e471d5db3d43e7e6919ab580">The biggest reason why <em>cloud computing</em> got so popular in the industry is the ability to scale up &amp; down dynamically. The ability to use &amp; pay only for the resources required by the website became a trend for obvious reasons.</p>
<p data-id="a264477a406c7cd2268f4f481631beaa">If the site has a heavy traffic influx more server nodes get added &amp; when it doesn’t the dynamically added nodes are removed.</p>
<p data-id="d67f75c3f882ea853776bf8a73a6a466">This approach saves businesses bags of money every single day. The approach is also known as <em>cloud elasticity</em>. It indicates the stretching &amp; returning to the original infrastructural computational capacity.</p>
<p data-id="e6b96a54f75ecc54b3eeb7b88a874278">Having multiple server nodes on the backend also helps with the website staying alive online all the time even if a few server nodes crash. This is known as <em>High Availability</em>. We’ll get to that in the upcoming lessons.</p>
</div></div></div></div></div></div></div></div></div>