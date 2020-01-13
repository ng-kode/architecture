---
id: strong-consistency-gxknzgrd626
title: Strong Consistency
sidebar_label: Strong Consistency
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss Strong Consistency.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-strong-consistency">What Is Strong Consistency?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-world-use-case">Real World Use Case</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#acid-transaction-support">ACID Transaction Support</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-strong-consistency" data-id="e6d2d52c9a3afc28c476c251ecbc7808">What Is Strong Consistency? <a class="markdownIt-Anchor" href="#what-is-strong-consistency"><span class="anchor-link">#</span></a></h2>
<p data-id="412f6b566878e2302a74ef9033d63a55"><em>Strong Consistency</em> simply means the data has to be strongly consistent at all times. All the server nodes across the world should contain the same value of an entity at any point in time. And the only way to implement this behaviour is by locking down the nodes when being updated.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-world-use-case" data-id="ab04785d769545c547a79cec54c99cb5">Real World Use Case <a class="markdownIt-Anchor" href="#real-world-use-case"><span class="anchor-link">#</span></a></h2>
<p data-id="eefb0a9e7dc49a09bc1e753d4118581b">Let’s continue the same Eventual Consistency example from the previous lesson. To ensure <em>Strong Consistency</em> in the system, when the user in Japan likes the post, all the nodes across different geographical zones have to be locked down to prevent any concurrent updates.</p>
<p data-id="9a596263c91b8de5608cf76dd895c459">This means at one point in time, only one user can update the post “<em>Like</em>” counter value.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5677430486335488_image_5844259724853248.jpeg" alt=""></p>
<p data-id="f1dd4377b78ffe34c8a6356c865b1f5f">So, once the user in Japan updates the “<em>Like</em>” counter from 100 to 101. The value gets replicated globally across all nodes. Once all the nodes reach a consensus, the locks get lifted.</p>
<p data-id="c574e4374fa7134f498fa2162779b18c">Now, other users can <em>Like</em> the post. If the nodes take a while to reach a consensus, they have to wait until then.</p>
<p data-id="bbc83d686ceaebe3af91d22097adb6e3">Well, this is surely not desired in case of social applications. But think of a stock market application where the users are seeing different prices of the same stock at one point in time and updating it concurrently. This would create chaos.</p>
<p data-id="32ccba7daaa41a677a15076186de42dd">Therefore, to avoid this confusion we need our systems to be <em>Strongly Consistent</em>. The nodes have to be locked down for updates.</p>
<p data-id="8503dd9ab9c88611e71df0bda13f75fb">Queuing all the requests is one good way of making a system <em>Strongly Consistent</em>. Well, the implementation is beyond the scope of this course. Though we will discuss a theorem called the <em>CAP theorem</em> which is key to implementing these consistency models.</p>
<p data-id="7d51c94fc7849c7e22740e78acdc7edd">So, by now I am sure you would have realized that picking the <em>Strong Consistency</em> model hits the capability of the system to be <em>Highly Available</em>.</p>
<p data-id="7465d0aa8a424d8c716b9d13cca417bb">The system while being updated by one user does not allow other users to perform concurrent updates. This is how strongly consistent ACID transactions are implemented.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="acid-transaction-support" data-id="9e7d2ae6e8b7df7eeffeb5c32010d3af">ACID Transaction Support <a class="markdownIt-Anchor" href="#acid-transaction-support"><span class="anchor-link">#</span></a></h2>
<p data-id="f51be77633351619b678a4e66bca9368">Distributed systems like <em>NoSQL</em> databases which scale horizontally on the fly don’t support <em>ACID transactions</em> globally &amp; this is due to their design. The whole reason for the development of <em>NoSQL</em> tech is the ability to be <em>Highly Available</em> and <em>Scalable</em>. If we have to lock down the nodes every time, it becomes just like <em>SQL</em>.</p>
<p data-id="5b967a116e50ba3a0038f240439a9385">So, NoSQL databases don’t support <em>ACID transactions</em> and those that claim to, have terms and conditions applied to them.</p>
<p data-id="763324756dc8adb08f858035277312b4">Generally, the transaction support is limited to a geographic zone or an entity hierarchy. Developers of the tech make sure that all the Strongly consistency entity nodes reside in the same geographic zone to make the <em>ACID transactions</em> possible.</p>
<p data-id="d6aa4b346f129c5d1aabaed0140fc352">Well, this is pretty much about <em>Strong Consistency</em>. Now let’s take a look into the <em>CAP Theorem</em></p>
</div></div></div></div></div></div></div></div></div>