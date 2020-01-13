---
id: redundancy-bnjg2jmzgpx
title: Redundancy
sidebar_label: Redundancy
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about Redundancy as a High Availability mechanism.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#redundancy-active-passive-ha-mode">Redundancy – Active-Passive HA Mode</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#getting-rid-of-single-points-of-failure">Getting Rid Of Single Points Of Failure</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#monitoring-automation">Monitoring &amp; Automation</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="redundancy-active-passive-ha-mode" data-id="a65d9888463ede1920833953b0ce3549">Redundancy – Active-Passive HA Mode <a class="markdownIt-Anchor" href="#redundancy-active-passive-ha-mode"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="fbae8051cadfd56e1f0279c7902d916d">
<p>Redundancy is duplicating the components or instances &amp; keeping them on standby to take over in case the active instances go down. It’s the fail-safe, backup mechanism.</p>
</blockquote>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5254824025128960_image_4609628669214720.jpeg" alt=""></p>
<p data-id="5fa939156efd3a452247b78f18f1e3b3">In the above diagram, you can see the instances active &amp; on standby. The standby instances take over in case any of the active instances goes down.</p>
<p data-id="aaf94a62f9a280533a0f3ed40775892a">This approach is also known as <em>Active-Passive HA mode</em>. An initial set of nodes are active &amp; a set of redundant nodes are passive, on standby. Active nodes get replaced by passive nodes, in case of failures.</p>
<p data-id="fcdd4f64db99107efece80ee456eac17">There are systems like GPS, aircrafts, communication satellites which have zero downtime. The availability of these systems is ensured by making the components redundant.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="getting-rid-of-single-points-of-failure" data-id="3ecc2c5506f467d11ba5f13c547c537a">Getting Rid Of Single Points Of Failure <a class="markdownIt-Anchor" href="#getting-rid-of-single-points-of-failure"><span class="anchor-link">#</span></a></h2>
<p data-id="7d0060d36d399dd709466a4f441a25b3">Distributed systems got so popular solely due to the reason that with them, we could get rid of the single points of failure present in a monolithic architecture.</p>
<p data-id="54b5ca1b68a3e2b6cafa5bab27fa4536">A large number of distributed nodes work in conjunction with each other to achieve a single synchronous application state.</p>
<p data-id="1bf1fd35cf27a601b57e1c817b8d7c83">When so many redundant nodes are deployed, there are no single points of failure in the system. In case a node goes down redundant nodes take its place. Thus, the system as a whole remains unimpacted.</p>
<p data-id="77be42283569e3fa8316b347fcfc9979">Single points of failure at the application level mean bottlenecks. We should detect bottlenecks in performance testing &amp; get rid of them as soon as we can.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="monitoring-automation" data-id="d8c6a28be146e6eda0a07563a162c470">Monitoring &amp; Automation <a class="markdownIt-Anchor" href="#monitoring-automation"><span class="anchor-link">#</span></a></h2>
<p data-id="f6ba73198236fc471bf321b76851ec94">Systems should be well monitored in real-time to detect any bottlenecks or single point of failures. Automation enables the instances to self-recover without any human intervention. It gives the instances the power of self-healing.</p>
<p data-id="fddce3b68ed65d297db2834c2d6a6b9c">Also, the systems become intelligent enough to add or remove instances on the fly as per the requirements.</p>
<p data-id="c46579d7d9b705be743763e218e21e10">Since the most common cause of failures is human error, automation helps cut down failures to a big extent.</p>
</div></div></div></div></div></div></div></div></div>