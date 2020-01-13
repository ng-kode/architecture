---
id: distributed-data-processing-rlnjvrrwlal
title: Distributed Data Processing
sidebar_label: Distributed Data Processing
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss distributed data processing and the technologies used for it.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-distributed-data-processing">What Is Distributed Data Processing?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#distributed-data-processing-technologies">Distributed Data Processing Technologies</a></li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#mapreduce-apache-hadoop">MapReduce – Apache Hadoop</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#apache-spark">Apache Spark</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#apache-storm">Apache Storm</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#apache-kafka">Apache Kafka</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="fd6d51474b1ac9dd0794066be3383d75">Alright!! Fellas, this lesson is all about distributed data processing. I’ll talk about what it is? How different is it in comparison to a centralized data processing system? What are the architectures involved in it? And other similar topics.</p>
<p data-id="e50651df22fa60901879b46a2153722b">So, let’s get on with it.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-distributed-data-processing" data-id="5830406a52ee8c33dcc196b0471fd628">What Is Distributed Data Processing? <a class="markdownIt-Anchor" href="#what-is-distributed-data-processing"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="a07ac5249c6de5a72959a05347d2ac2c">
<p><em>Distributed data processing</em> means diverging large amounts of data to several different nodes, running in a cluster, for parallel processing.</p>
</blockquote>
<p data-id="85cccca8043a8c77078663643b21fb11">All the nodes execute the task allotted parallelly, working in conjunction with each other co-ordinated by a node-co-ordinator. <em>Apache Zookeeper</em> is a pretty popular, de-facto, node co-ordinator used in the industry.</p>
<p data-id="45b6b45eeba652df4fd09e47b3a5c583">Since the nodes are distributed and the tasks are executed parallelly, this makes the entire set-up pretty <em>scalable</em> &amp; <em>highly available</em>. The workload can be scaled both horizontally &amp; vertically. Data is made <em>redundant</em> &amp; <em>replicated</em> across the cluster to avoid any sort of data loss.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5202497322876928_image_5116764474048512.jpeg" alt=""></p>
<p data-id="172cd0033fc4cd4cd8c48ba8cc2795a1">Processing data in a distributed environment helps accomplish the task in a significantly less amount of time as opposed to when running it on a centralized data processing system.</p>
<p data-id="d4f24c697c85b38dd0b4d8ed4b46833c">In a distributed system the tasks are shared by several nodes on the contrary in a centralized system the tasks are queued in a queue to be processed one by one.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="distributed-data-processing-technologies" data-id="443e104328c655a34154a0bae2ef9236">Distributed Data Processing Technologies <a class="markdownIt-Anchor" href="#distributed-data-processing-technologies"><span class="anchor-link">#</span></a></h2>
<p data-id="3d8e97a7272b166308dd6abd62f1ac8c">Here are some of the popular technologies, I’ve listed, that are used in the industry for large scale data processing.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="mapreduce-apache-hadoop" data-id="0f71c5488fa28620cd059b2ff31f7e1e">MapReduce – Apache Hadoop <a class="markdownIt-Anchor" href="#mapreduce-apache-hadoop"><span class="anchor-link">#</span></a></h3>
<p data-id="26813ed61d1c1e348b7edd9f8c1451b1"><em>MapReduce</em> is a programming model written for managing distributed data processing across several different machines in a cluster, distributing tasks to several machines, running work in parallel, managing all the communication and data transfer within different parts of the system.</p>
<p data-id="7d4026a05cbd685155e3ec4f23996ad8">The <em>Map</em> part of the programming model involves sorting the data based on a parameter and the <em>Reduce</em> part involves summarizing the sorted data.</p>
<p data-id="fe8af2049fad83107f486728ef3e8323">The most popular open-source implementation of the <em>MapReduce programming model</em> is <em>Apache Hadoop</em>.
The framework is used by all big guns in the industry to manage massive amounts of data in their system. It is used by Twitter for running analytics. It is used by Facebook for storing big data.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="apache-spark" data-id="6afd30bed624c8f3a7fc268946f191d7">Apache Spark <a class="markdownIt-Anchor" href="#apache-spark"><span class="anchor-link">#</span></a></h3>
<p data-id="8b3798762ad7c31713d633cf261b5da8"><em>Apache Spark</em> is an open-source cluster computing framework. It provides high performance for both batch &amp; real-time in-stream processing.
It can work with diverse data sources &amp; facilitates parallel execution of work in a cluster.</p>
<p data-id="4d98c1927cab690b417bb6674b96c7d0">Spark has a cluster manager and distributed data storage. The cluster manager facilitates communication between different nodes running together in a cluster whereas the distributed storage facilitates storage of big data.
Spark seamlessly integrates with distributed data stores like <em>Cassandra, HDFS, MapReduce File System, Amazon S3</em> etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="apache-storm" data-id="e1cb8ca22cc0fb2360f92b5e4fced75b">Apache Storm <a class="markdownIt-Anchor" href="#apache-storm"><span class="anchor-link">#</span></a></h3>
<p data-id="e8813e3cf7dd5f1f08f70b06446afd1b"><em>Apache Storm</em> is a distributed stream processing framework. In the industry, it is primarily used for processing massive amounts of streaming data.
It has several different use cases such as real-time analytics, machine learning, distributed remote procedure calls etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="apache-kafka" data-id="6a1af3c31ac2f0c75dc9ca145d3c5bc7">Apache Kafka <a class="markdownIt-Anchor" href="#apache-kafka"><span class="anchor-link">#</span></a></h3>
<p data-id="d64855a6d4d30c2f0b3a61794785322e"><em>Apache Kafka</em> is an open-source distributed stream processing &amp; messaging platform. It’s written using <em>Java</em> &amp; <em>Scala</em> &amp; was developed by <em>LinkedIn</em>.</p>
<p data-id="e65682b84a5212be3852a147b29dc03f">The storage layer of Kafka involves a distributed scalable pub/sub message queue. It helps read &amp; write streams of data like a messaging system.</p>
<p data-id="9c2315f7b32477518ce4ad92ef9344ff">Kafka is used in the industry to develop real-time features such as notification platforms, managing streams of massive amounts of data, monitoring website activity &amp; metrics, messaging, log aggregation.</p>
<p data-id="4319e8b6127af598fab8a4a7886c6050"><em>Hadoop</em> is preferred for <em>batch processing</em> of data whereas <em>Spark, Kafka</em> &amp; <em>Storm</em> are preferred for processing real-time streaming data.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="b482d84bd56200c132f0de2688c788c4">So, by now, I am sure you have a good idea of what data processing is. It’s use-cases in modern application development. The technologies involved etc.</p>
<p data-id="d79ef0fc816168dc08bf0fca0b5baf6a">Let’s have a look at a couple of architectures involved in the process. <em>Lambda</em> &amp; <em>Kappa</em>.</p>
</div></div></div></div></div></div></div></div></div>