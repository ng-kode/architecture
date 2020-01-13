---
id: lambda-architecture-x100zj6eadj
title: Lambda Architecture
sidebar_label: Lambda Architecture
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about Lambda Architecture of data processing.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-lambda-architecture">What Is Lambda Architecture?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#layers-of-the-lambda-architecture">Layers Of the Lambda Architecture</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-lambda-architecture" data-id="179cde40800b4a55e9b22b0b4ec51618">What Is Lambda Architecture? <a class="markdownIt-Anchor" href="#what-is-lambda-architecture"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="4376cf9895f41baf34d1dea3017f8300">
<p><em>Lambda</em> is a distributed data processing architecture that leverages both the <em>batch</em> &amp; the <em>real-time</em> streaming data processing approaches to tackle the latency issues arising out of the <em>batch processing</em> approach. It joins the results from both the approaches before presenting it to the end user.</p>
</blockquote>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4700526509817856_image_4614345407332352.jpeg" alt=""></p>
<p data-id="960f0005366249c3ae28e94b3a66adc8"><em>Batch processing</em> does take time considering the massive amount of data businesses have today but with it the accuracy of the approach is high &amp; the results are comprehensive.</p>
<p data-id="f7cd9d6b2fd06d1c42c3466a0a2e0fca">On the contrary, <em>real-time streaming data processing</em> provides quick access to insights. In this scenario, the analytics is run over a small portion of data so the results are not that accurate &amp; comprehensive when compared to that of the batch approach.</p>
<p data-id="61ef63e6998c4c75419481eaa5922244"><em>Lambda architecture</em> makes the most of the two approaches.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="layers-of-the-lambda-architecture" data-id="48d35afa77abd18c5b2ad8d0740a1570">Layers Of the Lambda Architecture <a class="markdownIt-Anchor" href="#layers-of-the-lambda-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="1df3bd404f6a4ae4e78dcc57438d79df">The architecture has typically three layers:</p>
<ul data-id="76e51a403b7873934b83cb0c68583e1c">
<li>Batch Layer</li>
<li>Speed Layer</li>
<li>Serving layer</li>
</ul>
<p data-id="a3dc72e8784ddb0f337d6119137b919e">The <em>Batch Layer</em> deals with the results acquired via batch processing the data. The <em>Speed layer</em> gets data from the real-time streaming data processing &amp; the <em>Serving layer</em> combines the results obtained from both the <em>Batch</em> &amp; the <em>Speed</em> layers.</p>
</div></div></div></div></div></div></div></div></div>