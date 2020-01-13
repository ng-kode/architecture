---
id: time-series-database-7nvw0zwxm9w
title: Time Series Database
sidebar_label: Time Series Database
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will get to know the Time Series database and when to choose it for our projects.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-time-series-database">What Is A Time Series Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-is-time-series-data">What Is Time Series Data?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#why-store-time-series-data">Why Store Time Series Data?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#popular-time-series-databases">Popular Time Series Databases</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#when-to-pick-a-time-series-database">When To Pick A Time Series Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-life-implementations">Real Life Implementations</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-time-series-database" data-id="e2e479e44f4ec6c2b47bcb3ef8e1a1fc">What Is A Time Series Database? <a class="markdownIt-Anchor" href="#what-is-a-time-series-database"><span class="anchor-link">#</span></a></h2>
<p data-id="c468482c8a8d0c1199a26a9bc29112a7"><em>Time-Series</em> databases are optimized for tracking &amp; persisting time series data.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-time-series-data" data-id="7293c903b2d141e98410d2a36e52862f">What Is Time Series Data? <a class="markdownIt-Anchor" href="#what-is-time-series-data"><span class="anchor-link">#</span></a></h2>
<p data-id="8bf4b7654f9dbb70d2c8efbbccd06463">It is the data containing data points associated with the occurrence of an event with respect to time. These data points are tracked, monitored and then finally aggregated based on certain business logic.</p>
<p data-id="1367a7031f21d6e63068c7deaaa95869"><em>Time-Series</em> data is generally ingested from IoT devices, self-driving vehicles, industry sensors, social networks, stock market financial data etc.</p>
<p data-id="73e8882ea2bc9229cb907c5d5c0017c6"><em>Okay!! But, what is the need for storing such a massive amount of <em>time-series</em> data?</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="why-store-time-series-data" data-id="4b946b3afcd50cf1deb4e47d68b49f1f">Why Store Time Series Data? <a class="markdownIt-Anchor" href="#why-store-time-series-data"><span class="anchor-link">#</span></a></h2>
<p data-id="5e8d51b65da8a4422fb2182c061aa91c">Studying data, streaming-in from applications helps us track the behaviour of the system. It helps us study user patterns, anomalies &amp; how things change over time.</p>
<p data-id="cf941d865ddd414eaf89afb9ba9a5818"><em>Time-series</em> data is primarily used for running analytics, deducing conclusions and making future business decisions looking at the results of the analytics. Running analytics also helps the product evolve continually.</p>
<p data-id="8aa3591de195ca73b58d9452c7528bae">General databases are not built to handle <em>time-series</em> data. With the advent of IoT, these databases are getting pretty popular and are being adopted by the big guns in the industry.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="popular-time-series-databases" data-id="e0c57f5949ce61971778cc493a4f0442">Popular Time Series Databases <a class="markdownIt-Anchor" href="#popular-time-series-databases"><span class="anchor-link">#</span></a></h2>
<p data-id="71d2c980d0ba17f9044c926afdc19328">Some of the popular <em>time-series</em> databases used in the industry are <em>Influx DB</em>, <em>Timescale DB</em>, <em>Prometheus</em> etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="when-to-pick-a-time-series-database" data-id="78110bdfcbb84b9c28a6af8ac3f2500b">When To Pick A Time Series Database? <a class="markdownIt-Anchor" href="#when-to-pick-a-time-series-database"><span class="anchor-link">#</span></a></h2>
<p data-id="c20d64bd99c8ee74f268b7e596eab10b">If you have a use case where you need to manage data in real-time &amp; continually over a long period of time, then a <em>time-series</em> database is what you need.</p>
<p data-id="8e876058d41326752ae6b595d3c132e3">As we know that the <em>time-series</em> databases are built to deal with data, streaming in real-time. The typical use cases of it are fetching data from IoT devices. Managing data for running analytics &amp; monitoring. Writing an autonomous trading platform which deals with changing stock prices in real-time etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-life-implementations" data-id="4a3328dc5b6d054ca0d10e3f5b389a32">Real Life Implementations <a class="markdownIt-Anchor" href="#real-life-implementations"><span class="anchor-link">#</span></a></h2>
<p data-id="e2a46f95266e122b34e8aeb74d25a65c"><em>Here are some of the real-life implementations of the tech -</em></p>
<ul data-id="0f5bdb10fddf8bdff629e1387eb4fa5d">
<li>
<p><a href="https://www.influxdata.com/customer/ibm/" target="_blank">IBM uses Influx DB to run analytics for real-time cognitive fraud detection</a></p>
</li>
<li>
<p><a href="https://www.influxdata.com/customer/customer_case_study_spiio/" target="_blank">Spiio uses Influx DB to remotely monitor vertical lining green walls &amp; plant installations.</a></p>
</li>
</ul>
</div></div></div></div></div></div></div></div></div>