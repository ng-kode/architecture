---
id: when-to-pick-a-nosql-database-qzz4p43rpk7
title: When To Pick A NoSQL Database?
sidebar_label: When To Pick A NoSQL Database?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discover when to choose a NoSQL Database over any other kind of database.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#handling-a-large-number-of-read-write-operations">Handling A Large Number Of Read Write Operations</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#flexibility-with-data-modeling">Flexibility With Data Modeling</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#eventual-consistency-over-strong-consistency">Eventual Consistency Over Strong Consistency</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#running-data-analytics">Running Data Analytics</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="handling-a-large-number-of-read-write-operations" data-id="62988fdc7482c927074a5a8e268de0f1">Handling A Large Number Of Read Write Operations <a class="markdownIt-Anchor" href="#handling-a-large-number-of-read-write-operations"><span class="anchor-link">#</span></a></h2>
<p data-id="d562d15d83bc549039ef62511fff087b">Look towards <em>NoSQL</em> databases when you need to scale fast. And when do you generally need to scale fast?</p>
<p data-id="d6270b2286e83021c247226ae57cb97c">When there are a large number of read-write operations on your website &amp; when dealing with a large amount of data, <em>NoSQL</em> databases fit best in these scenarios. Since they have the ability to add nodes on the fly, they can handle more concurrent traffic &amp; big amount of data with minimal latency.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="flexibility-with-data-modeling" data-id="f27f3f0617f1eeb8c51786b62e2a1acb">Flexibility With Data Modeling <a class="markdownIt-Anchor" href="#flexibility-with-data-modeling"><span class="anchor-link">#</span></a></h2>
<p data-id="489e31ddaad2bd0ab1dabc9a2786998d">The second cue is during the initial phases of development when you are not sure about the data model, the database design, things are expected to change at a rapid pace. <em>NoSQL</em> databases offer us more flexibility.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="eventual-consistency-over-strong-consistency" data-id="65c0d9542048e210ed51276a3c512dc8">Eventual Consistency Over Strong Consistency <a class="markdownIt-Anchor" href="#eventual-consistency-over-strong-consistency"><span class="anchor-link">#</span></a></h2>
<p data-id="ecbaee662b4d342f86a27b98c47627d6">It’s preferable to pick <em>NoSQL</em> databases when it’s OK for us to give up on <em>Strong consistency</em> and when we do not require <em>transactions</em>.</p>
<p data-id="8cf124daa2e4cbd38d5087b316c8afbb">A good example of this is a social networking website like Twitter.
When a tweet of a celebrity blows up and everyone is liking and re-tweeting it from around the world. Does it matter if the count of <em>likes</em> goes up or down a bit for a short while?</p>
<p data-id="67feb50ba7245f09bf7c7a074fe2074a">The celebrity would definitely not care if instead of the actual 5 million 500 <em>likes</em>, the system shows the <em>like</em> count as 5 million 250 for a short while.</p>
<p data-id="36d01d7d3ca5cbb20529cf57ecd1d98a">When a large application is deployed on hundreds of servers spread across the globe, the geographically distributed nodes take some time to reach a global consensus.</p>
<p data-id="9a34c837163ff7f138abf88af52fec9c">Until they reach a consensus, the value of the entity is inconsistent. The value of the entity eventually gets consistent after a short while. This is what <em>Eventual Consistency</em> is.</p>
<p data-id="9d53d6850ee7173da8266caec9b5a580">Though the inconsistency does not mean that there is any sort of data loss. It just means that the data takes a short while to travel across the globe via the internet cables under the ocean to reach a global consensus and become consistent.</p>
<p data-id="69fbc37b12b6e2752efff4123abc464f">We experience this behaviour all the time. Especially on YouTube. Often you would see a video with 10 views and 15 likes. How is this even possible?</p>
<p data-id="37fec5a106faad87da5ba05e0c4172ad">It’s not. The actual views are already more than the likes. It’s just the count of views is inconsistent and takes a short while to get updated.
I will discuss <em>Eventual consistency</em> in more detail further down the course.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="running-data-analytics" data-id="60e39089fb814f0b29f0a596a3c0b17e">Running Data Analytics <a class="markdownIt-Anchor" href="#running-data-analytics"><span class="anchor-link">#</span></a></h2>
<p data-id="39e0088a6748b1577973ad88ba7f8cb6"><em>NoSQL</em> databases also fit best for <em>data analytics</em> use cases, where we have to deal with an influx of massive amounts of data.</p>
<p data-id="fe9e53e7410d19da32c1b2b6c1b9e5b9">There are dedicated databases for use cases like this such as <em>Time-Series databases</em>, <em>Wide-Column</em>, <em>Document Oriented</em> etc. I’ll talk about each of them further down the course.</p>
<p data-id="584cff6ae6ee547f468b8b92bcd6f122">Right now, let’s have an insight into the performance comparison of SQL and NoSQL tech.</p>
</div></div></div></div></div></div></div></div></div>