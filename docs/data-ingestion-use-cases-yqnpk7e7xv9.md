---
id: data-ingestion-use-cases-yqnpk7e7xv9
title: Data Ingestion Use Cases
sidebar_label: Data Ingestion Use Cases
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss some common data ingestion use cases in the industry.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li>
<ul>
<li><a href="#moving-big-data-into-hadoop">Moving Big Data Into Hadoop</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#streaming-data-from-databases-to-elasticsearch-server">Streaming Data from Databases to Elasticsearch Server</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#log-processing">Log Processing</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#stream-processing-engines-for-real-time-events">Stream Processing Engines for Real-Time Events</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="856515c7158cda53064f28ba72d776a1">This is the part where I talk about some of the data streaming use cases commonly required in the industry.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="moving-big-data-into-hadoop" data-id="d2c4db8ee616612749e7949b7bd68964">Moving Big Data Into Hadoop <a class="markdownIt-Anchor" href="#moving-big-data-into-hadoop"><span class="anchor-link">#</span></a></h3>
<p data-id="8b877f00a921db05073f07a9df956c4f">This is the most popular use case of data ingestion. As discussed before, Big Data from IoT devices, social apps &amp; other sources, streams through data pipelines, moves into the most popular distributed data processing framework Hadoop for analysis &amp; stuff.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="streaming-data-from-databases-to-elasticsearch-server" data-id="495e59576eb66849f1b17349bc727bff">Streaming Data from Databases to Elasticsearch Server <a class="markdownIt-Anchor" href="#streaming-data-from-databases-to-elasticsearch-server"><span class="anchor-link">#</span></a></h3>
<p data-id="e6734d7d8f85d6717a2fb8674574972e"><em>Elastic search</em> is an open-source framework for implementing search in web applications. It is a defacto search framework used in the industry simply because of its advanced features, &amp; it being open-source. These features enable businesses to write their own custom solutions when they need them.</p>
<p data-id="5a21137401aaee5c4cf8bcc41bab3eb1">In my former workplace, I wrote a product search service using <em>Java</em>, <em>Spring Boot</em> &amp; <em>Elastic Search</em>. Speaking of its design, we would stream &amp; index quite a large amount of product data from the legacy storage solutions to the Elastic search server in order to make the products come up in the search results.</p>
<p data-id="2c27bffaf057cf32bae912733828fc93">All the data intended to show up in the search was replicated from the main storage to the Elastic search storage. Also, as the new data was persisted in the main storage it was asynchronously rivered to the Elastic server in real-time for indexing.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="log-processing" data-id="787d9cdace6e6d9e8a03610ed1e1defb">Log Processing <a class="markdownIt-Anchor" href="#log-processing"><span class="anchor-link">#</span></a></h3>
<p data-id="08f3d56e2c0a5f6e4bd0fe82b7753239">If your project isn’t a hobby project, chances are it’s running on a cluster. When we talk about running a large-scale service, monolithic systems are a thing of the past. With so many microservices running concurrently. There is a massive number of logs which is generated over a period of time. And logs are the only way to move back in time, track errors &amp; study the behaviour of the system.</p>
<p data-id="b151b5b61e87f40f082ae5a027ff9dbd">So, to study the behaviour of the system holistically, we have to stream all the logs to a central place. Ingest logs to a central server to run analytics on it with the help of solutions like ELK Elastic LogStash Kibana stack etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="stream-processing-engines-for-real-time-events" data-id="935f7df31a8e0a0d3e3bf0d241413428">Stream Processing Engines for Real-Time Events <a class="markdownIt-Anchor" href="#stream-processing-engines-for-real-time-events"><span class="anchor-link">#</span></a></h3>
<p data-id="1ecccc4a5e0f6d52d862511b0df42d3b">Real-time streaming &amp; data processing is the core component in systems handling LIVE information such as sports. It’s imperative that the architectural setup in place is efficient enough to ingest data, analyse it, figure out the behaviour in real-time &amp; quickly push the updated information to the fans. After all, the whole business depends on it.</p>
<p data-id="5b9a51bd5a5deaa6564a9c0e1eb565a0">Message queues like <em>Kafka</em>, Stream computation frameworks like <em>Apache Storm, Apache Nifi, Apache Spark, Samza, Kinesis</em> etc are used to implement the real-time large-scale data processing features in online applications.</p>
<p data-id="f1a470638cb992b728fd06ad65659d61">This is a good read on the topic:</p>
<p data-id="4f1e5bbb56e7e3258a8938b309a14ad9">An Insight into <a href="https://medium.com/netflix-techblog/keystone-real-time-stream-processing-platform-a3ee651812a" target="_blank">Netflix’s real-time streaming platform</a></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="8513fcc57c622402fb9cd76b0239f525">Alright!! time to have a look into data pipelines in the lesson up-next.</p>
</div></div></div></div></div></div></div></div></div>