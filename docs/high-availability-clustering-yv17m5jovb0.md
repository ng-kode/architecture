---
id: high-availability-clustering-yv17m5jovb0
title: High Availability Clustering
sidebar_label: High Availability Clustering
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about High Availability Clustering.</p></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="b15d1f265369d8935eb0f49d7d3d3136">Now, that we have a clear understanding of high availability, let’s talk a bit about the high availability cluster.</p>
<p data-id="aaecaead9e797da73d5613b52e6f60c3">A <em>High Availability cluster</em> also known as the <em>Fail-Over cluster</em> contains a set of nodes running in conjunction with each other that ensures high availability of the service.</p>
<p data-id="d651b4d8d09a4e0204b78ac84188cc0d">The nodes in the cluster are connected by a private network called the <em>Heartbeat network</em> that continuously monitors the health and the status of each node in the cluster.</p>
<p data-id="ac464cbf8b634e1941ba2bdf2975c37e">A single state across all the nodes in a cluster is achieved with the help of a shared distributed memory &amp; a distributed co-ordination service like the <em>Zookeeper</em>.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_6702767257157632_image_5224269203111936.jpeg" alt=""></p>
<p data-id="4ca7e6cb543aa1c1df3429f491b023b0">To ensure the availability, HA clusters use several techniques such as <em>Disk mirroring/RAID Redundant Array Of Independent Disks</em>, redundant network connections, redundant electrical power etc. The network connections are made redundant so if the primary network goes down the backup network takes over.</p>
<p data-id="8f14eccc47a6bd9e5e6434e51182f7f9">Multiple HA clusters run together in one geographical zone ensuring minimum downtime &amp; continual service.</p>
<p data-id="f02dc0b0a2fd8fceb26c1de83148dff8">Alright, so now we have a pretty good understanding of scalability and high availability. These two concepts are crucial to software system design.</p>
<p data-id="55eb6f8b6a00b9073c6311bc94d3f9ec">Moving on to the next chapter where we discuss monolithic &amp; microservices architecture.</p>
</div></div></div></div></div></div></div></div></div>