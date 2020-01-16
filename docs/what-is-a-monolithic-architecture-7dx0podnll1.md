---
id: what-is-a-monolithic-architecture-7dx0podnll1
title: What Is A Monolithic Architecture?
sidebar_label: What Is A Monolithic Architecture?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss the Monolithic Architecture.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-monolithic-architecture">What Is A Monolithic Architecture?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-monolithic-architecture" data-id="33388a834ce807e1ced415788d68ea09">What Is A Monolithic Architecture? <a class="markdownIt-Anchor" href="#what-is-a-monolithic-architecture"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="36c4d7ad4458143dc535a6618e9c2fec">
<p>An application has a monolithic architecture if it contains the entire application code in a single codebase.</p>
</blockquote>
<p data-id="dd86de39edbf79ba9c18648b9a93c992">A monolithic application is a self-contained, single-tiered software application unlike the microservices architecture, where different modules are responsible for running respective tasks and features of an app.</p>
<p data-id="d10f3961baa793470290c299cf284dc2">The diagram below represents a monolithic architecture:</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_6286949360861184_image_6008277051637760.jpeg" alt=""></p>
<p data-id="1f1f370fa245ac46cbe6928106d0daa5">In a monolithic web-app all the different layers of the app, UI, business, data access etc. are in the same codebase.</p>
<p data-id="2f928907791808615a9466f50e564394">We have the <em>Controller</em>, then the <em>Service Layer interface</em>, <em>Class</em> implementations of the interface, the <em>business logic</em> goes in the <em>Object Domain model</em>, a bit in the Service, Business and the <em>Repository/DAO [Data Access Object]</em> classes.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_6286949360861184_image_5373720531042304.jpeg" alt=""></p>
<p data-id="614930043df03e8dcc113de819931b43">Monolithic apps are simple to build, test &amp; deploy in comparison to a microservices architecture.</p>
<p data-id="d4c3fcadb4944a465dfb10ebdb3404b0">There are times during the initial stages of the business when teams chose to move forward with the monolithic architecture &amp; then later intend to branch out into the distributed, microservices architecture.</p>
<p data-id="faa28fc1af212066c0362b7c6393b172">Well, this decision has several trade-offs. And there is no standard solution to this.</p>
<p data-id="7ae8ae0928333dc47604a46e5eeb5ee3">In the present computing landscape, the applications are being built &amp; deployed on the cloud. A wise decision would be to pick the loosely coupled stateless microservices architecture right from the start if you expect things to grow at quite a pace in the future.</p>
<p data-id="995729eacc4afcaca6482caee4fdcc56">Because re-writing stuff has its costs. Stripping down things in a tightly coupled architecture &amp; re-writing stuff demands a lot of resources &amp; time.</p>
<p data-id="a4fb9ae6f04e109a32ec618aae1d50ba">On the flip side, if your requirements are simple why bother writing a microservices architecture? Running different modules in conjunction with each other isn’t a walk in the park.</p>
<p data-id="1f055f0e2e47e8a247004aa88ca180d7">Let’s go through some of the pros and cons of monolithic architecture.</p>
</div></div></div></div></div></div></div></div></div>