---
id: when-should-you-pick-a-monolithic-architecture-gx66ljknjgg
title: When Should You Pick a Monolithic Architecture?
sidebar_label: When Should You Pick a Monolithic Architecture?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the pros and cons of a Monolithic Architecture &amp; when to choose it for our project.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#pros-of-monolithic-architecture">Pros Of Monolithic Architecture</a>
<ul>
<li><a href="#simplicity">Simplicity</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li><a href="#cons-of-monolithic-architecture">Cons Of Monolithic Architecture</a>
<ul>
<li><a href="#continuous-deployment">Continuous Deployment</a></li>
<li><a href="#regression-testing">Regression Testing</a></li>
<li><a href="#single-points-of-failure">Single Points Of Failure</a></li>
<li><a href="#scalability-issues">Scalability Issues</a></li>
<li><a href="#cannot-leverage-heterogeneous-technologies">Cannot Leverage Heterogeneous Technologies</a></li>
<li><a href="#not-cloud-ready-hold-state">Not Cloud-Ready, Hold State</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li><a href="#when-should-you-pick-a-monolithic-architecture">When Should You Pick A Monolithic Architecture?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="pros-of-monolithic-architecture" data-id="ee49e42ca59d43426bc6a54f66faa77e">Pros Of Monolithic Architecture <a class="markdownIt-Anchor" href="#pros-of-monolithic-architecture"><span class="anchor-link">#</span></a></h2>
<h3 id="simplicity" data-id="1e4eb7fbe67592f1e83cb967b118c4c4">Simplicity <a class="markdownIt-Anchor" href="#simplicity"><span class="anchor-link">#</span></a></h3>
<p data-id="e199496be7a145ea317be627a5e9f83d">Monolithic applications are simple to develop, test, deploy, monitor and manage since everything resides in one repository.</p>
<p data-id="6ece7eae5abb539aad19986182efc775">There is no complexity of handling different components, making them work in conjunction with each other, monitoring several different components &amp; stuff. Things are simple.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="cons-of-monolithic-architecture" data-id="b01f76fcbb678515b07a798cde2f798d">Cons Of Monolithic Architecture <a class="markdownIt-Anchor" href="#cons-of-monolithic-architecture"><span class="anchor-link">#</span></a></h2>
<h3 id="continuous-deployment" data-id="488cc65ab6b24c7121bb4f44e27fa02c">Continuous Deployment <a class="markdownIt-Anchor" href="#continuous-deployment"><span class="anchor-link">#</span></a></h3>
<p data-id="7726cce58f7dcaa2f1dd97a7471e0dd6"><em>Continuous deployment</em> is a pain in case of monolithic applications as even a minor code change in a layer needs a re-deployment of the entire application.</p>
<h3 id="regression-testing" data-id="ec90d161be53c333ed1c468e9e088c57">Regression Testing <a class="markdownIt-Anchor" href="#regression-testing"><span class="anchor-link">#</span></a></h3>
<p data-id="00c953c8db5f10596a9b79053bd07702">The downside of this is that we need a thorough <em>regression testing</em> of the entire application after the deployment is done as the layers are tightly coupled with each other. A change in one layer impacts other layers significantly.</p>
<h3 id="single-points-of-failure" data-id="4efec51cd2710e04778dd2abc499bf91">Single Points Of Failure <a class="markdownIt-Anchor" href="#single-points-of-failure"><span class="anchor-link">#</span></a></h3>
<p data-id="6aea3551996fd5e43a197f7a587ef395">Monolithic applications have a <em>single point of failure</em>. In case any of the layers has a bug, it has the potential to take down the entire application.</p>
<h3 id="scalability-issues" data-id="03a843ffe93d0f05b744441ef1053043">Scalability Issues <a class="markdownIt-Anchor" href="#scalability-issues"><span class="anchor-link">#</span></a></h3>
<p data-id="1c54d046afa293da7c844ba9e17b9ae3">Flexibility and scalability are a challenge in monolith apps as a change in one layer often needs a change and testing in all the layers.
As the code size increases, things might get a bit tricky to manage.</p>
<h3 id="cannot-leverage-heterogeneous-technologies" data-id="00d65e29a609bb3df63db277416ab8d2">Cannot Leverage Heterogeneous Technologies <a class="markdownIt-Anchor" href="#cannot-leverage-heterogeneous-technologies"><span class="anchor-link">#</span></a></h3>
<p data-id="7812609266d1d9759caff694ab8b2577">Building complex applications with a monolithic architecture is tricky as using heterogeneous technologies is difficult in a single codebase due to the compatibility issues.</p>
<p data-id="197ffc4a30791ef8bd0818aa25466f27">It’s tricky to use <em>Java</em> &amp; <em>NodeJS</em> together in a single codebase, &amp; when I say tricky, I am being generous. I am not sure if it’s even possible to do that.</p>
<h3 id="not-cloud-ready-hold-state" data-id="4907ec91d96495c5bd8a20d5429c6fce">Not Cloud-Ready, Hold State <a class="markdownIt-Anchor" href="#not-cloud-ready-hold-state"><span class="anchor-link">#</span></a></h3>
<p data-id="51aeea778144958fab4355e42ea30309">Generally, monolithic applications are not cloud-ready as they hold state in the static variables. An application to be cloud-native, to work smoothly &amp; to be consistent on the cloud has to be distributed and stateless.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="when-should-you-pick-a-monolithic-architecture" data-id="51f30467618ab3beb29d7b9b8a46c28f">When Should You Pick A Monolithic Architecture? <a class="markdownIt-Anchor" href="#when-should-you-pick-a-monolithic-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="6e0cc2ea0ba20db106771d3bdf25af49">Monolithic applications fit best for use cases where the requirements are pretty simple, the app is expected to handle a limited amount of traffic. One example of this is an internal tax calculation app of an organization or a similar open public tool.</p>
<p data-id="5965f08c5ff5ea9163f98463b1712dd3">These are the use cases where the business is certain that there won’t be an exponential growth in the user base and the traffic over time.</p>
<p data-id="00ee4191c9d7f99aa6e9420b96ddcb2d">There are also instances where the dev teams decide to start with a monolithic architecture and later scale out to a distributed microservices architecture.</p>
<p data-id="23b8de41fde9c0ad19c572a3ce818615">This helps them deal with the complexity of the application step by step as and when required. <a href="https://engineering.linkedin.com/architecture/brief-history-scaling-linkedin" target="_blank">This is exactly what LinkedIn did.</a></p>
<p data-id="dcae43e583bfb6cc9362e2b6799e85fc">In the next lesson, we will learn about the Microservice architecture.</p>
</div></div></div></div></div></div></div></div></div>