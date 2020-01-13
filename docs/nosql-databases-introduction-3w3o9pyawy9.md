---
id: nosql-databases-introduction-3w3o9pyawy9
title: NoSQL Databases - Introduction
sidebar_label: NoSQL Databases - Introduction
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will get an insight into NoSQL databases and how they are different from Relational databases.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-nosql-database">What Is A NoSQL Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#how-is-a-nosql-database-different-from-a-relational-database">How Is A NoSQL Database Different From A Relational Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#scalability">Scalability</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#clustering">Clustering</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-nosql-database" data-id="582d9014e8d12f6c3db1d28515e1bdc2">What Is A NoSQL Database? <a class="markdownIt-Anchor" href="#what-is-a-nosql-database"><span class="anchor-link">#</span></a></h2>
<p data-id="1f3f589d9c1b6feb4dfb0c608d165837">In this lesson, we will get an insight into NoSQL databases and how they are different from Relational databases. As the name implies <em>NoSQL</em> databases have no <em>SQL</em>, they are more like <em>JSON-based</em> databases built for Web 2.0</p>
<p data-id="4e1b8dac987740f0d12d8e5b4975d1d6">They are built for high frequency read &amp; writes, typically required in social applications like Twitter, LIVE real-time sports apps, online massive multi-player games etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="how-is-a-nosql-database-different-from-a-relational-database" data-id="226b7b4344dc76e003ecf4b9d60f27c6">How Is A NoSQL Database Different From A Relational Database? <a class="markdownIt-Anchor" href="#how-is-a-nosql-database-different-from-a-relational-database"><span class="anchor-link">#</span></a></h2>
<p data-id="a7feb4524393f6a089ddfede57473d62">Now, one obvious question that would pop-up in our minds is:</p>
<p data-id="d547177c175221e51d65bea9c36668f4"><strong>Why the need for NoSQL databases when relational databases were doing fine, were battle-tested, well adopted by the industry &amp; had no major persistence issues?</strong></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="scalability" data-id="606356a1fd48ac2cc748cd731178ae57">Scalability <a class="markdownIt-Anchor" href="#scalability"><span class="anchor-link">#</span></a></h2>
<p data-id="65e630c7721da3c63fe29e862ff916fb">Well, one big limitation with <em>SQL</em> based relational databases is <em>Scalability</em>. Scaling relational databases is something which is not trivial. They have to be <em>Sharded</em> or <em>Replicated</em> to make them run smoothly on a cluster. In short, this requires careful thought and human intervention.</p>
<p data-id="f14ffec8d8d7fe618c4b736be592a4b4">On the contrary, <em>NoSQL</em> databases have the ability to add new server nodes on the fly &amp; continue the work, without any human intervention, just with a snap of the fingers.</p>
<p data-id="79d2da00b088677c53f8fa6d09244835">Today’s websites need fast read writes. There are millions, if not billions of users connected with each other on social networks.</p>
<p data-id="ecc6587de7cbd2686e630a025c3ee66b">Massive amount of data is generated every micro-second, we needed an infrastructure designed to manage this exponential growth.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="clustering" data-id="f0225f6153001ea2eeb89ca6fc6ccf65">Clustering <a class="markdownIt-Anchor" href="#clustering"><span class="anchor-link">#</span></a></h2>
<p data-id="79a9b130908e5ad33ae8a953bbdb19e4"><em>NoSQL</em> databases are designed to run intelligently on clusters. And when I say intelligently, I mean with minimal human intervention.</p>
<p data-id="24fc0a63b12869fda08de963bbd37b5c">Today, the server nodes even have <em>self-healing</em> capabilities. That’s pretty smooth. The infrastructure is intelligent enough to self-recover from faults.</p>
<p data-id="cef61b1d68b59794621e606c3ed231a9">Though all this innovation does not mean old school relational databases aren’t good enough &amp; we don’t need them anymore.</p>
<p data-id="54f668643544b479698ae90fbdecefc4">Relational databases still work like a charm &amp; are still in demand. They have a specific use-case. We have already gone through this in <a href="https://www.educative.io/collection/page/6064040858091520/6411938009448448/6652931912761344" target="_blank"><em>When to pick a relational database lesson</em></a>. Remember? 😊</p>
<p data-id="be850454acb6c1506978996b29894876">Also, <em>NoSQL</em> databases had to sacrifice <em>Strong consistency</em>, <em>ACID Transactions</em> &amp; much more to scale horizontally over a cluster &amp; across the data centres.</p>
<p data-id="f3cfc95b64502e21f4aeca1e9a811d0b">The data with <em>NoSQL</em> databases is more <em>Eventually Consistent</em> as opposed to being <em>Strongly Consistent</em>.</p>
<p data-id="9ebe756c377577c5373267b7c6fc3620">So, this obviously means <em>NoSQL</em> databases aren’t the silver bullet. And it’s completely alright, we don’t need silver bullets. We aren’t hunting werewolves, we are upto a much harder task connecting the world online.</p>
<p data-id="ce84861da5e2226780e3a89c34c47095">I’ll talk about the underlying design of <em>NoSQL</em> databases in much detail and why they have to sacrifice <em>Strong consistency</em> and <em>Transactions</em> in the upcoming lessons.</p>
<p data-id="c5ddf9333003469d7bc7e6cba4ba4aeb">For now, let’s focus on some of the features of <em>NoSQL</em> databases.</p>
</div></div></div></div></div></div></div></div></div>