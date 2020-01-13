---
id: data-ingestion-r1x5erqk7q0
title: Data Ingestion
sidebar_label: Data Ingestion
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will have an insight into the process of data ingestion. </p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-data-ingestion">What Is Data Ingestion?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#layers-of-data-processing-setup">Layers Of Data Processing Setup</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#data-standardization">Data Standardization</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#data-processing">Data Processing</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#data-analysis">Data Analysis</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#data-visualization">Data Visualization</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#data-storage-security">Data Storage &amp; Security</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-data-ingestion" data-id="801f84d1efd56afbff66707dc8856fd4">What Is Data Ingestion? <a class="markdownIt-Anchor" href="#what-is-data-ingestion"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="7e53e11ee048f8c60c09390628f896f5">
<p><em>Data Ingestion</em> is a collective term for the process of collecting data streaming-in from several different sources and making it ready to be processed by the system.</p>
</blockquote>
<p data-id="513d10f5bc17b840bd82653efc6d805e">In a data processing system, the data is ingested from the IoT devices &amp; other sources, into the system to be analysed. It is routed to different components/layers through the <em>data pipelines</em>, algorithms are run on it and is eventually archived.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="layers-of-data-processing-setup" data-id="400eb2df7118517ba07777b7d65ed31c">Layers Of Data Processing Setup <a class="markdownIt-Anchor" href="#layers-of-data-processing-setup"><span class="anchor-link">#</span></a></h2>
<p data-id="3af94adf35f9f68fd1d6770c1d0318ea">There are several stages/layers to this whole data processing setup such as the:</p>
<ul data-id="c283449ede8864190bad8c89c09523c1">
<li>Data collection layer</li>
<li>Data query layer</li>
<li>Data processing layer</li>
<li>Data visualization layer</li>
<li>Data storage layer</li>
<li>Data security layer</li>
</ul>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4569452697878528_image_5250130053693440.jpeg" alt=""></p>
<p data-id="83163d9bdda25422a74d90738f7682c0">As you can see in the diagram all the data processing layers are pretty self-explanatory.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="data-standardization" data-id="3a0d7ac58160856cd230cf95b2453c17">Data Standardization <a class="markdownIt-Anchor" href="#data-standardization"><span class="anchor-link">#</span></a></h2>
<p data-id="78169b9bf938ca870fd76e1f6cc5a749">The data which streams in from several different sources is not in a homogeneous structured format. We have already gone through different types of data, structured, unstructured, semi-structured in the database lesson. So, you have an idea of what unstructured heterogeneous data is.</p>
<p data-id="fcf15f4a86315abf94af65c26e6cf3af">Data streams-in into the system at different speeds &amp; sizes, from the web-based services, social networks, IoT devices, industrial machines &amp; whatnot. Every stream of data has different semantics.</p>
<p data-id="12c9a390c3c3380f43baeaf81c4f4c46">So, in order to make the data uniform and fit for processing, it has to be first collected and converted into a standardized format to avoid any future processing issues. This process of data standardization occurs in the <em>Data collection and preparation layer</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="data-processing" data-id="eda6c69eae53b0122a9bf10389d65284">Data Processing <a class="markdownIt-Anchor" href="#data-processing"><span class="anchor-link">#</span></a></h2>
<p data-id="9cf62e1b954cb6b0940a462f68e448a5">Once the data is transformed into a standard format it is routed to the <em>Data processing layer</em> where it is further processed based on the business requirements. It is generally classified into different flows, routed to different destinations.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="data-analysis" data-id="4269a00395b40e0ef7ef4a27e0d45eb3">Data Analysis <a class="markdownIt-Anchor" href="#data-analysis"><span class="anchor-link">#</span></a></h2>
<p data-id="6709d3add284c8fc4be3a721fc4533d0">After being routed, analytics is run on the data which includes execution of different analytics models such as predictive modelling, statistical analytics, text analytics etc. All the analytical events occur in the <em>Data Analytics layer</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="data-visualization" data-id="94a5cd68edacd327002992518ecb59b5">Data Visualization <a class="markdownIt-Anchor" href="#data-visualization"><span class="anchor-link">#</span></a></h2>
<p data-id="ca9ad97fb3fc18ab2276223935dbd747">Once the analytics are run &amp; we have valuable intel from it. All the information is routed to the <em>Data visualization layer</em> to be presented before the stakeholders, generally in a web-based dashboard.</p>
<p data-id="ad4548f7ef6cdf19509a9973f820b90d"><em>Kibana</em> is one good example of a data visualization tool, pretty popular in the industry.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="data-storage-security" data-id="40f079af141188e2fdf9be76e2cbea93">Data Storage &amp; Security <a class="markdownIt-Anchor" href="#data-storage-security"><span class="anchor-link">#</span></a></h2>
<p data-id="96de1d8bb8e130fc1ac40a36f6bbf41e">Moving data is highly vulnerable to security breaches. <em>The Data security layer</em> ensures the secure movement of data all along. Speaking of the <em>Data Storage layer</em>, as the name implies, is instrumental in persisting the data.</p>
<p data-id="2764fca6eeb363809332aff16ed8f305">So, this is a gist of how massive amounts of data is processed and analyzed for business use cases. This is just a bird’s eye view of things. The field of data analytics is pretty deep, an in-depth detailed microscopic view of each layer demands a dedicated data analytics course for itself.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="702135fb5542a53a4ce3ad69cab67ffd">Alright, now let’s have a look at the different ways in which the data can be ingested.</p>
</div></div></div></div></div></div></div></div></div>