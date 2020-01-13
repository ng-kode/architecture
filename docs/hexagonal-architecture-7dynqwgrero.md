---
id: hexagonal-architecture-7dynqwgrero
title: Hexagonal Architecture
sidebar_label: Hexagonal Architecture
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will have an insight into the Hexagonal architecture.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-hexagonal-architecture">What Is A Hexagonal Architecture?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-world-code-implementation">Real World Code Implementation</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"></div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-hexagonal-architecture" data-id="8e2e85db2e397248735f08e02117ef9f">What Is A Hexagonal Architecture? <a class="markdownIt-Anchor" href="#what-is-a-hexagonal-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="74d753947a47a3a11ea7fee0e3765d01">The architecture consists of three components:</p>
<ul data-id="bba2ba31f290b7186bc2ce9486ee0512">
<li>Ports</li>
<li>Adapters</li>
<li>Domain</li>
</ul>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/courses_web-application-software-architecture-101_assets_api_collection_6064040858091520_6411938009448448_page_6366983450787840_image_6736074485268480.jpeg.jpeg" alt=""></p>
<p data-id="e55167e2728f203c8f34cff032df338b">The focus of this architecture is to make different components of the application: independent, loosely coupled &amp; easy to test.</p>
<p data-id="cece2daf6054eb884c6bc88d5377c274">The application should be designed in a way such that it can be tested by humans, automated tests, with mock databases, mock middleware, with &amp; without a UI, without making any changes or adjustments to the code.</p>
<p data-id="8c1467087ca6ba89ba743d768a9ba063">The architectural pattern holds the <em>domain</em> at its core, that’s the <em>business logic</em>. On the outside, the outer layer has <em>Ports</em> &amp; <em>Adapters</em>.
<em>Ports</em> act like an <em>API</em>, as an interface. All the input to the app goes through the interface.</p>
<p data-id="fa7c71deffd2c6ac6e46b5d10be4bc73">So, the external entities don’t have any direct interaction with the <em>domain</em>, the business logic.
The <em>Adapter</em> is the implementation of the interface. Adapters convert the data obtained from the <em>Ports</em>, to be processed by the <em>business logic</em>. The <em>business logic</em> lies at the centre isolated &amp; all the input and output is at the edges of the structure.</p>
<p data-id="6ef629be57d9c946f8e8b1075e3bc376">The hexagonal shape of the structure doesn’t have anything to do with the pattern, it’s just a visual representation of the architecture.
Initially, the architecture was called as the <em>Ports and the Adapter pattern</em>, later the name <em>Hexagonal</em> stuck.</p>
<p data-id="1b20bd6834d58d2928f7df7a92b973e8">The <em>Ports &amp; the Adapter</em> analogy comes from the computer ports, as they act as the input interface to the external devices &amp; the <em>Adapter</em> converts the signals obtained from the ports to be processed by the chips inside.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-world-code-implementation" data-id="c392e6ab56963225c45023c805d1d336">Real World Code Implementation <a class="markdownIt-Anchor" href="#real-world-code-implementation"><span class="anchor-link">#</span></a></h2>
<p data-id="acab3fd595bc017cae381660c3961503">Coming down to the real-world code implementation, isn’t that’s what we already do with the <em>Layered Architecture</em> approach? We have different layers in our applications, we have the <em>Controller</em>, then the <em>Service Layer</em> interface, <em>Class</em> implementations of the interface, the <em>Business logic</em> goes in the <em>Domain model</em>, a bit in the <em>Service</em>, <em>Business</em> and the <em>Repository</em> classes.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/courses_web-application-software-architecture-101_assets_api_collection_6064040858091520_6411938009448448_page_6366983450787840_image_4806117710364672.jpeg.jpeg" alt=""></p>
<p data-id="11f9f6adaabb9c4c8e13a3e1f742c160">Well, yeah. That’s right. First up, I would say that the Hexagonal approach is an evolution of the layered architecture. It’s not entirely different.
As long as the business logic stays in one place, things should be fine. The issue with the layered approach is, often large repos end up with too many layers beside the regular service, repo &amp; business ones.</p>
<p data-id="70bbb4e0e609989f2954203f6a4507f8">The business logic gets scattered across the layers making testing, refactoring &amp; pluggability of new entities difficult. Remember the <em>Stored procedures</em> in the databases &amp; the business logic coupled with the UI in <em>JSP Java Server Pages</em>?</p>
<p data-id="5ddb4054a2e4a36d12ce8876b8f5c10b">When working with <em>JSPs</em> and <em>Stored procedures</em>, we still have the layered architecture, the <em>UI layer</em> is separate, the <em>persistence layer</em> is separate but the <em>business logic</em> is tightly coupled with these layers.</p>
<p data-id="87299ca4884f73f9312f9216bfd68405">On the contrary, the <em>Hexagonal pattern</em> has its stance pretty clear, there is an inside component which holds the <em>business logic</em> &amp; then the outside layer, the <em>Ports</em> &amp; the <em>Adapters</em> which involve the <em>databases</em>, <em>message queues</em>, <em>APIs</em> &amp; stuff.</p>
</div></div></div></div></div></div></div></div></div>