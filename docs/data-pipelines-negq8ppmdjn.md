---
id: data-pipelines-negq8ppmdjn
title: Data Pipelines
sidebar_label: Data Pipelines
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about Data Pipelines.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-are-data-pipelines">What Are Data Pipelines?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#features-of-data-pipelines">Features Of Data Pipelines</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-is-etl">What Is ETL?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-are-data-pipelines" data-id="0efb499d0708c0d2578087ebce8dd5a4">What Are Data Pipelines? <a class="markdownIt-Anchor" href="#what-are-data-pipelines"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="ab02e6f9689974cd68914807171b006e">
<p><em>Data pipelines</em> are the core component of a data processing infrastructure. They facilitate the efficient flow of data from one point to another &amp; also enable the developers to apply filters on the data streaming-in in real-time.</p>
</blockquote>
<p data-id="b29436d59d7d9bf57a0270b65da99acc">Today’s enterprise is data-driven. That makes data pipelines key in implementing scalable analytics systems.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="features-of-data-pipelines" data-id="2839cbabf987e61e42a39f31d7075111">Features Of Data Pipelines <a class="markdownIt-Anchor" href="#features-of-data-pipelines"><span class="anchor-link">#</span></a></h2>
<p data-id="b33f186b0eed942ab111cb317bcb7511">Speaking of some more features of the data pipelines -</p>
<ul data-id="3c794242b0ac0ee809efea38fb1bc9df">
<li>These ensure smooth flow of data.</li>
<li>Enables the business to apply filters and business logic on streaming data.</li>
<li>Avert any bottlenecks &amp; redundancy in the data flow.</li>
<li>Facilitate parallel processing of data.</li>
<li>Avoid data being corrupted.</li>
</ul>
<p data-id="5647fc03f75dde46f44bef61bb9bcc9c">These pipelines work on a set of rules predefined by the engineering teams &amp; the data is routed accordingly without any manual intervention. The entire flow of data extraction, transformation, combination, validation, converging of data from multiple streams into one etc. is completely automated.</p>
<p data-id="d8a3ae402164a1161f96442ce3962c42">Data pipelines also facilitate parallel processing of data via managing multiple streams. I’ll talk more about the distributed data processing in the upcoming lesson.</p>
<p data-id="11022852c38afe8b6eb2600747a35483">Traditionally we used <em>ETL</em> systems to manage all the movement of data, but one major limitation with them is they don’t really support handling of real-time streaming data. Which is possible with new era evolved data processing infrastructure powered by the data pipelines.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-etl" data-id="6094cd2acaf02db91347b1187c3c970a">What Is ETL? <a class="markdownIt-Anchor" href="#what-is-etl"><span class="anchor-link">#</span></a></h2>
<p data-id="ae5e887616bece4af6f6b74266d0ec6d">If you haven’t heard of ETL before, it means Extract Transform Load.</p>
<p data-id="f122c2a174bc02e79611200122ffbd16"><strong>Extract</strong> means fetching data from single or multiple data sources.</p>
<p data-id="62db39d4618c6b1ab4b50e92e3936173"><strong>Transform</strong> means transforming the <em>extracted</em> heterogeneous data into a standardized format based on the rules set by the business.</p>
<p data-id="56c5c63a341cec2d69bb86b2250a05ad"><strong>Load</strong> means moving the <em>transformed</em> data to a data warehouse or another data storage location for further processing of data.</p>
<p data-id="41100b1db54c20179f70deaf83675d66">The <em>ETL</em> flow is the same as the <em>data ingestion</em> flow. It’s just the entire movement of data is done in batches as opposed to streaming it, through the data pipelines, in real-time.</p>
<p data-id="05772c64174e07352e832ed2e2bdb635">Also, at the same time, it doesn’t mean the <em>batch processing</em> approach is obsolete. Both real-time &amp; batch data processing techniques are leveraged based on the project requirements.</p>
<p data-id="4d4574762d6a92596e3423b06a5d6c3d">You’ll gain more insight into it when we will go through the <em>Lambda</em> &amp; <em>Kappa</em> architectures of distributed data processing in the upcoming lessons.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="954ccb3f80977788bea8c3dc18485091">In the previous lesson, I brought up a few of the popular data processing tools such as <em>Apache Flink</em>, <em>Storm</em>, <em>Spark</em>, <em>Kafka</em> etc. All these tools have one thing in common they facilitate processing of data in a cluster, in a distributed environment via data pipelines.</p>
<p data-id="5742c12c1477c2a49c43f2d811d05949"><a href="https://www.infoq.com/articles/netflix-migrating-stream-processing/" target="_blank">This Netflix case study is a good read on how they migrated batch ETL to Stream processing using Kafka &amp; Flink</a></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="6b6d623273f3ba1f380b0a9241c0e909">What is distributed data processing? How does it work? We are gonna look into it in the next lesson. Stay tuned.</p>
</div></div></div></div></div></div></div></div></div>