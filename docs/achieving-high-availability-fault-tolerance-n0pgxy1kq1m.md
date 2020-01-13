---
id: achieving-high-availability-fault-tolerance-n0pgxy1kq1m
title: Achieving High Availability - Fault Tolerance
sidebar_label: Achieving High Availability - Fault Tolerance
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about fault tolerance &amp; designing a HA fault tolerant service. </p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-fault-tolerance">What is Fault Tolerance?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#designing-a-highly-available-fault-tolerant-service-architecture">Designing A Highly Available Fault-Tolerant Service – Architecture</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="4ebba671dfd599d88e8194700d1d3093">There are several approaches to achieve HA. The most important of them is to make the system fault-tolerant.</p>
<h2 id="what-is-fault-tolerance" data-id="8b24a63826ce52bed02b881a7a753ced">What is Fault Tolerance? <a class="markdownIt-Anchor" href="#what-is-fault-tolerance"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="2047e54f07e1b95fd0463e2098299806">
<p><em>Fault tolerance</em> is the ability of the system to stay up despite taking hits.</p>
</blockquote>
<p data-id="4a775af1ed88f5167c5478d862dfd8cc">A fault-tolerant system is equipped to handle faults. Being fault-tolerant is an essential element in designing life-critical systems.</p>
<p data-id="49d9e49709d7ae4260ab2c4d284ef3be">A few of the <em>instances/nodes</em>, out of several, running the service go offline &amp; bounce back all the time. In case of these internal failures, the system could work at a reduced level but it will not go down entirely.</p>
<p data-id="9334b961af23e1fd4735c90786d2c2fc">A very basic example of a system being fault-tolerant is a social networking application. In the case of backend node failures, a few services of the app such as image upload, post likes etc. may stop working. But the application as a whole will still be up. This approach is also technically known as <em>Fail Soft</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="designing-a-highly-available-fault-tolerant-service-architecture" data-id="4bb344a000b7e3c42dbd4e1b0dbbdf3c">Designing A Highly Available Fault-Tolerant Service – Architecture <a class="markdownIt-Anchor" href="#designing-a-highly-available-fault-tolerant-service-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="0cf1f24dc25c3ec3835e89e209b7c22b">To achieve high availability at the application level, the entire massive service is architecturally broken down into smaller loosely coupled services called the <strong>micro-services</strong>.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4911548562669568_image_5237658383024128.jpeg" alt=""></p>
<p data-id="b64bc3ff36bb1a97a15a3987be617673">There are many upsides of splitting a big monolith into several microservices, as it provides:</p>
<ul data-id="b114a34c9edbe7b1dda929d96f9f3f19">
<li>Easier management</li>
<li>Easier development</li>
<li>Ease of adding new features</li>
<li>Ease of maintenance</li>
<li>High availability</li>
</ul>
<p data-id="530020f6942c4ead41f26c07d4bacde5">Every microservice takes the onus of running different features of an application such as image upload, comment, instant messaging etc.</p>
<p data-id="a24141059a8ed5dd49859d6199859eb8">So, even if a few services go down the application as a whole is still up.</p>
</div></div></div></div></div></div></div></div></div>