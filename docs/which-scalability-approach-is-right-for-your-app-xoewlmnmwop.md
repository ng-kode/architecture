---
id: which-scalability-approach-is-right-for-your-app-xoewlmnmwop
title: Which Scalability Approach Is Right For Your App?
sidebar_label: Which Scalability Approach Is Right For Your App?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about which type of scaling is better for a given scenario.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#pros-cons-of-vertical-horizontal-scaling">Pros &amp; Cons of Vertical &amp; Horizontal Scaling</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-about-the-code-why-does-the-code-need-to-change-when-it-has-to-run-on-multiple-machines">What about the code? Why does the code need to change when it has to run on multiple machines?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#which-scalability-approach-is-right-for-your-app">Which Scalability Approach Is Right for Your App?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="pros-cons-of-vertical-horizontal-scaling" data-id="8f7d00bb20abbb38334423dacdc57de1">Pros &amp; Cons of Vertical &amp; Horizontal Scaling <a class="markdownIt-Anchor" href="#pros-cons-of-vertical-horizontal-scaling"><span class="anchor-link">#</span></a></h2>
<p data-id="525350b93f80581e6dc24c8741e28487">This is the part where I talk about the plus &amp; minuses of both the approaches.</p>
<p data-id="d3094482dacdb5ebde04c329baf49a31">Vertical scaling for obvious reasons is simpler in comparison to scaling horizontally as we do not have to touch the code or make any complex distributed system configurations. It takes much less administrative, monitoring, management efforts as opposed to when managing a distributed environment.</p>
<p data-id="dd9b347f57b5fa9d593c87f3a08751f9">A major downside of vertical scaling is availability risk. The servers are powerful but few in number, there is always a risk of them going down &amp; the entire website going offline which doesn’t happen when the system is scaled horizontally. It becomes more highly available.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-about-the-code-why-does-the-code-need-to-change-when-it-has-to-run-on-multiple-machines" data-id="eb895a4fa811d22eb40f70e68395ba4a">What about the code? Why does the code need to change when it has to run on multiple machines? <a class="markdownIt-Anchor" href="#what-about-the-code-why-does-the-code-need-to-change-when-it-has-to-run-on-multiple-machines"><span class="anchor-link">#</span></a></h2>
<p data-id="334ddcf8ae231bab007e9e8ba88a7e5f">If you need to run the code in a distributed environment, it needs to be <em>stateless</em>. There should be no state in the code. <strong>What do I mean by that?</strong></p>
<p data-id="37058960ce79eb0223c8bf36a4401f3d">No <em>static instances</em> in the class. Static instances hold application data &amp; if a particular server goes down all the static data/state is lost. The app is left in an inconsistent state.</p>
<p data-id="0fac4d8a6c37da0c56b3037b288e7150">Rather, use a persistent memory like a <em>key-value</em> store to hold the data &amp; to remove all the state/static variable from the class. This is why functional programming got so popular with distributed systems. The functions don’t retain any state.</p>
<p data-id="d400915ee3df69ec21c2cd28d271aa7d">Always have a ballpark estimate on mind when designing your app. <strong>How much traffic will it have to deal with?</strong></p>
<p data-id="1e6b538c22260003b9edd0e699ec819e">Development teams today are adopting a distributed micro-services architecture right from the start &amp; the workloads are meant to be deployed on the cloud. So, inherently the workloads are horizontally scaled out on the fly.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_6582657154547712_image_6728318856462336.jpeg" alt=""></p>
<p data-id="fc110dc036622f395e003bd128986668">The upsides of horizontally scaling include no limit to augmenting the hardware capacity. Data is replicated across different geographical regions as nodes &amp; data centres are set up across the globe.</p>
<p data-id="86df362bf2dd37569c43a71dc8145317">I’ll discuss cloud, serverless and microservices in the upcoming lessons. So, stay tuned.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="which-scalability-approach-is-right-for-your-app" data-id="526eda47a9b81a41f10cd4b2ece480c3">Which Scalability Approach Is Right for Your App? <a class="markdownIt-Anchor" href="#which-scalability-approach-is-right-for-your-app"><span class="anchor-link">#</span></a></h2>
<p data-id="e8db1a94fc0adaac17b2789a51c48b97">If your app is a utility or a tool which is expected to receive minimal consistent traffic, it may not be mission-critical. For instance, an internal tool of an organization or something similar.</p>
<p data-id="3a9d5ef24bb210d87c9ab48adfcfa211">Why bother hosting it in a distributed environment? A single server is enough to manage the traffic, go ahead with vertical scaling when you know that the traffic load would not increase significantly.</p>
<p data-id="60fa643e7d1ece593ef0cc56991033ed">If your app is a public-facing social app like a social network, a fitness app or something similar, then the traffic is expected to spike exponentially in the near future. Both high availability &amp; horizontal scalability is important to you.</p>
<p data-id="4f183e9bee1dfcc590813d62b488d0c9">Build to deploy it on the cloud &amp; always have horizontal scalability in mind right from the start.</p>
</div></div></div></div></div></div></div></div></div>