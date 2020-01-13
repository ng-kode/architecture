---
id: different-ways-of-ingesting-data-the-challenges-involved-7agqn620kay
title: Different Ways Of Ingesting Data & the Challenges Involved
sidebar_label: Different Ways Of Ingesting Data & the Challenges Involved
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss the different ways in which we can ingest the data. Also, we will cover the challenges involved in this process.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#different-ways-to-ingest-data">Different Ways To Ingest Data</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#challenges-with-data-ingestion">Challenges with Data Ingestion</a></li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#slow-process">Slow Process</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#complex-expensive">Complex &amp; Expensive</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#moving-data-around-is-risky">Moving Data Around Is Risky</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="different-ways-to-ingest-data" data-id="5bc6decdf8a413f54839b651331e73f4">Different Ways To Ingest Data <a class="markdownIt-Anchor" href="#different-ways-to-ingest-data"><span class="anchor-link">#</span></a></h2>
<p data-id="5e42edc59023d07bc91e28601a179719">There are two primary ways to ingest data, in <em>Real-time</em> &amp; in <em>Batches</em> which run at regular intervals. Which one to pick of the two entirely depends on the business requirements.</p>
<p data-id="1f1681c313cb34b39c533021936d19ac">Data Ingestion in real-time is typically preferred in systems reading medical data like a heartbeat, blood pressure via wearable IoT sensors where the time is of critical importance. Also, in systems handling financial data like stock market events etc. These are a few instances where time, lives &amp; money are closely linked &amp; we need information as soon as we can get.</p>
<p data-id="eef8aeb838e1660d2cbb694f712291e5">On the contrary, in systems that read trends over time, we can always ingest data in batches. For instance, when estimating the popularity of a sport in a region over a period of time.</p>
<p data-id="9f5c51b8152d9fd83e8daf9db2d8076f">Let’s talk about some of the challenges which developers have to face when ingesting massive amounts of data. I have added this lesson just to give you a deeper insight into the entire process.
In the upcoming lesson, I also talk about the general use-cases of data streaming in the application development domain.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="challenges-with-data-ingestion" data-id="a361b168e10ffcf74fdb39c7d187904e">Challenges with Data Ingestion <a class="markdownIt-Anchor" href="#challenges-with-data-ingestion"><span class="anchor-link">#</span></a></h2>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="slow-process" data-id="57fffaac30ec9d009a1c161905acc0fb">Slow Process <a class="markdownIt-Anchor" href="#slow-process"><span class="anchor-link">#</span></a></h3>
<p data-id="2ef8d1c463d639db71d5250c6f2e5ddd">Data ingestion is a slow process. Why? I’ve brought up this before. When the data is streamed from several different sources into the system, data coming from each &amp; every different source has a different format, different syntax, attached metadata. The data as a whole is heterogeneous. It has to be transformed into a common format like <em>JSON</em> or something to be understood well by the analytics system.</p>
<p data-id="3153ebd57faefb84e80f134a083093df">The conversion of data is a tedious process. It takes a lot of computing resources &amp; time. Flowing data has to be staged at several stages in the pipeline, processed &amp; then moved ahead.</p>
<p data-id="44fe12caafb847ebf7924e0e5df49e4e">Also, at each &amp; every stage data has to be authenticated &amp; verified to meet the organization’s security standards. With the traditional data cleansing processes, it takes weeks if not months to get useful information on hand. Traditional data ingestion systems like <em>ETL</em> ain’t that effective anymore.</p>
<p data-id="2f1c0ba7815a698e09d62d1bdeeeb631"><strong>Okay!! But you just said data can be ingested in real-time Right? So, how is it slow?</strong></p>
<p data-id="f1c2787b4bc2568b6c11a2b0d0fe6695">Two things, I would like to bring up here, <em>first</em> the modern data processing tech &amp; frameworks are continually evolving to beat the limitations of the legacy, traditional data processing systems. Real-time data ingestion wasn’t even possible with the traditional systems.</p>
<p data-id="035088e31b7fc9c04bfdac0e7a375c7d"><em>Second</em>, analytics information obtained from real-time processing is not that accurate &amp; holistic since the analytics continually runs on a limited set of data as it streams as opposed to the batch processing approach which takes into account the entire data set. So, it’s basically the more time we spend studying the data the more accurate results we get.</p>
<p data-id="2635af8448cb80f0966c547ffc343198">You’ll learn more about this when we go through the <em>Lambda</em> and the <em>Kappa</em> architectures of data processing.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="complex-expensive" data-id="7b3bc49c5cb7be98958e576ac0dc53da">Complex &amp; Expensive <a class="markdownIt-Anchor" href="#complex-expensive"><span class="anchor-link">#</span></a></h3>
<p data-id="2658a2f04b94cb1dda4249fe89dd9565">The entire data flow process is resource-intensive. A lot of heavy lifting has to be done to prepare the data before being ingested into the system. Also, it isn’t a side process, a dedicated team is required to pull off something like that.</p>
<p data-id="bb49614270cbe71e17b14ada8e93c04d">Engineering teams often come across scenarios where the tools &amp; frameworks available in the market fail to serve their needs &amp; they have no option other than to write a custom solution from the bare bones.</p>
<p data-id="9e9d0bb64186d770c729be0411e1de0b"><em>Gobblin</em> is a data ingestion tool by LinkedIn. At one point in time, LinkedIn had 15 data ingestion pipelines running which created several data management challenges. <a href="https://engineering.linkedin.com/data-ingestion/gobblin-big-data-ease" target="_blank">To tackle this problem, LinkedIn wrote Gobblin in-house.</a></p>
<p data-id="05ae6c63358b3f27a0a5f27fb7ed32ed">It is a part of the Apache Software Foundation now. <a href="https://engineering.linkedin.com/blog/2018/01/gobblin-enters-apache-incubation" target="_blank">This is a good read</a></p>
<p data-id="2e26f7116cc2737a1c9702333a8c902d">The semantics of the data coming from externals sources changes sometimes as they are not always under our control, which then requires a change in the backend data processing code. Today the IoT machines in the industry are continually evolving at a rapid pace.</p>
<p data-id="c18ce18f76c033ff147d94962c09c234">These are the factors we have to keep in mind when setting up a data processing &amp; analytics system.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="moving-data-around-is-risky" data-id="9742a92620f68c6e9c5b122cbfd39283">Moving Data Around Is Risky <a class="markdownIt-Anchor" href="#moving-data-around-is-risky"><span class="anchor-link">#</span></a></h3>
<p data-id="6c8563c74adddc2bfe7aa21320ed3fca">When data is moved around it opens up the possibility of a breach. Moving data is vulnerable. It goes through several different staging areas &amp; the engineering teams have to put in additional effort and resources to ensure their system meets the security standards at all times.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="c2945f0910801444ad253d0f1faa41e0">These are some of the challenges which developers face when working with streaming data.</p>
</div></div></div></div></div></div></div></div></div>