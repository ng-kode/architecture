---
id: replication-q2glm948zpp
title: Replication
sidebar_label: Replication
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about Replication as a High Availability mechanism.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#replication-active-active-ha-mode">Replication – Active-Active HA Mode</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#geographical-distribution-of-workload">Geographical Distribution of Workload</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="replication-active-active-ha-mode" data-id="ae8991f40070dee30a5da976ae8654cc">Replication – Active-Active HA Mode <a class="markdownIt-Anchor" href="#replication-active-active-ha-mode"><span class="anchor-link">#</span></a></h2>
<p data-id="a0cfe9347c3b62273684b8ea0454880e">Replication means having a number of similar nodes running the workload together. There are no standby or passive instances. When a single or a few nodes go down, the remaining nodes bear the load of the service. Think of this as load balancing.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5508982540075008_image_6234524285403136.jpeg" alt=""></p>
<p data-id="69f3d1ccce74258b2ee665a2c518741e">This approach is also known as the <em>Active-Active High Availability</em> mode. In this approach, all the components of the system are active at any point in time.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="geographical-distribution-of-workload" data-id="c6a48e5c9800ba720267af4e06fd8635">Geographical Distribution of Workload <a class="markdownIt-Anchor" href="#geographical-distribution-of-workload"><span class="anchor-link">#</span></a></h2>
<p data-id="279a5d81218836408bbae97eef2a30bc">As a contingency for natural disasters, data centre regional power outages &amp; other big-scale failures, workloads are spread across different data centres across the world in different geographical zones.</p>
<p data-id="4a4e0afbaf05630f25f641abf71892c9">This avoids the single point of failure thing in context to a data centre. Also, the latency is reduced by quite an extent due to the proximity of data to the user.</p>
<p data-id="4138d2f1b91a330adc8b2f5540a7ed86">All the highly available fault-tolerant design decisions are subjective to how critical the system is? What are the odds that the components will fail? Etc.</p>
<p data-id="0605adc72b7af6c6f01f8ad712686ab8">Businesses often use multi-cloud platforms to deploy their workloads which ensures further availability. If things go south with one cloud provider, they have another to fail back over.</p>
</div></div></div></div></div></div></div></div></div>