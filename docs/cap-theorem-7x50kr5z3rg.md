---
id: cap-theorem-7x50kr5z3rg
title: CAP Theorem
sidebar_label: CAP Theorem
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the CAP theorem.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-cap-theorem">What Is CAP Theorem?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-cap-theorem" data-id="279aa6df6d85f4b2464c4e0cc92e4c7c">What Is CAP Theorem? <a class="markdownIt-Anchor" href="#what-is-cap-theorem"><span class="anchor-link">#</span></a></h2>
<p data-id="4c0e6c5532479ad60199b1b228a4b70c"><em>CAP</em> stands for <strong>Consistency</strong>, <strong>Availability</strong>, <strong>Partition Tolerance</strong>. We’ve gone through consistency and availability in great detail. <em>Partition Tolerance</em> means <em>Fault Tolerance</em>. The system is tolerant of failures or partitions. It keeps working even if a few nodes go down.</p>
<p data-id="3f1635dd84d19ac41b5332880da6c2a2">There are many definitions of the theorem, you’ll find online, which state that amongst the three, <em>Consistency</em>, <em>Availability</em> &amp; the <em>Partition Tolerance</em>, we have to pick two. I find that a teeny tiny bit of confusing. I will try to give a simpler explanation of the theorem.</p>
<blockquote data-id="60bed5740ab00ff4acbffc222711fa06">
<p><em>CAP theorem</em> simply states that in case of a network failure, when a few of the nodes of the system are down, we have to make a choice between <em>Availability</em> &amp; <em>Consistency</em></p>
</blockquote>
<p data-id="02c82cd764c193b067eb22f12b0fea5a">If we pick <em>Availability</em> that means when a few nodes go down, the other nodes are available to the users for making updates. In this situation, the system is inconsistent as the nodes which are down don’t get updated with the new data.
At the point in time when they come back online, if a user fetches the data from them, they’ll return the old values they had when they went down.</p>
<p data-id="cc53c897b8928e1e69d0aaecbb41cdea">If we pick <em>Consistency</em>, in that scenario, we have to lock down all the nodes for further writes until the nodes which have gone down come back online. This would ensure the <em>Strong consistency</em> of the system as all the nodes will have the same entity values.</p>
<p data-id="d5b91fd4f43dd1180097f7a7ce3e9b5a">Picking between <em>Availability</em> and <em>Consistency</em> largely depends on our use case and the business requirements. We have been through this in great detail. Also, the limitation of picking one out of the two is due to the design of the distributed systems. We can’t have both <em>Availability</em> and <em>Consistency</em> at the same time.</p>
<p data-id="999657ee62f41b91ce697fdd6b1b366b">Nodes, spread around the globe, will take some time to reach a consensus. It’s impossible to have zero-latency unless we transit data faster than or at the speed of time.</p>
</div></div></div></div></div></div></div></div></div>