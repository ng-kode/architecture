---
id: eventual-consistency-n7xwgdpv3np
title: Eventual Consistency
sidebar_label: Eventual Consistency
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss Eventual Consistency.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-eventual-consistency">What Is Eventual Consistency?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-world-use-case">Real World Use Case</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-eventual-consistency" data-id="a13ea41bb50f81452d1cec0bc229187c">What Is Eventual Consistency? <a class="markdownIt-Anchor" href="#what-is-eventual-consistency"><span class="anchor-link">#</span></a></h2>
<p data-id="cdb87c2f78952e6b94ccfbedb51de703"><em>Eventual consistency</em> is a consistency model which enables the data store to be <em>highly available</em>. It is also known as <em>optimistic replication</em> &amp; is key to distributed systems.</p>
<p data-id="8bd87a3eda0659a391a6ecb144a33f49"><em>So, how exactly does it work?</em></p>
<p data-id="a11818d0a02ffb2ca5a6d161409d346f">We’ll understand this with the help of a use case.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-world-use-case" data-id="ab04785d769545c547a79cec54c99cb5">Real World Use Case <a class="markdownIt-Anchor" href="#real-world-use-case"><span class="anchor-link">#</span></a></h2>
<p data-id="31d16604c406c0d72192da7f07fff1e0">Think of a popular microblogging site deployed across the world in different geographical regions like Asia, America, Europe. Moreover, each geographical region has multiple data centre zones: North, East, West, South. Furthermore, each of the zones has multiple clusters which have multiple server nodes running.</p>
<p data-id="d58d8ad300149d916198affeb350ba2a">So, we have many datastore nodes spread across the world which the micro-blogging site uses for persisting data.</p>
<p data-id="bf2ae0287e0ed7b2e9bbc968dc7a5341">Since there are so many nodes running, there is no <em>single point of failure</em>. The data store service is <em>highly available</em>. Even if a few nodes go down the persistence service as a whole is still up.</p>
<p data-id="e5f7352d267c3aaa04f70c8b426ae632">Alright, now let’s say a celebrity makes a post on the website which everybody starts liking around the world.</p>
<p data-id="0f5b74479f5cfde0c82de2a6d0e6c93b">At a point in time, a user in Japan likes the post which increases the “Like” count of the post from say 100 to 101. At the same point in time, a user in America, in a different geographical zone clicks on the post and he sees the “Like” count as 100, not 101.</p>
<p data-id="16850cb0174a7c39b12721594f8af55b"><em>Why did this happen?</em></p>
<p data-id="6dbf7ed4b9f9a2a58482aa45194db0fd">Simply, because the new updated value of the Post “Like” counter needs some time to move from Japan to America and update the server nodes running there.</p>
<p data-id="b93508bbbddf5a709d7b861f90452e41">Though the value of the counter at that point in time was 101, the user in America sees the old inconsistent value.</p>
<p data-id="9cee19c2b114884dc9608cc0ac5ece84">But when he refreshes his web page after a few seconds the “Like” counter value shows as 101. So, the data was initially inconsistent but eventually got consistent across the server nodes deployed around the world.
This is what <em>eventual consistency</em> is.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_6373547041619968_image_6521446723485696.jpeg" alt=""></p>
<p data-id="751c7f690ddeae7cdecf8ead26438c4a">Let’s take it one step further, what if at the same point in time both the users in Japan and America <em>Like</em> the post, and a user in another geographic zone say Europe accesses the post.</p>
<p data-id="a34f68f63ad9c86919da6472bed569d0">All the nodes in different geographic zones have different post values. And they will take some time to reach a consensus.</p>
<p data-id="ef33f4be897e2216b8668ffff7f00ed9">The upside of eventual consistency is that the system can add new nodes on the fly without the need to block any of them, the nodes are available to the end-users to make an update at all times.</p>
<p data-id="bf8292f3ff6288d79652e9814d1cd06b">Millions of users across the world can update the values at the same time without having to wait for the system to reach a common final value across all nodes before they make an update. This feature enables the system to be <em>highly available</em>.</p>
<p data-id="0d7631cc8166d9102d3342ead92947a7"><em>Eventual consistency</em> is suitable for use cases where the accuracy of values doesn’t matter much like in the above-discussed use case.</p>
<p data-id="425527cdc6da0ef00bb914773c2a04aa">Other use cases of eventual consistency can be when keeping the count of users watching a Live video stream online. When dealing with massive amounts of analytics data. A couple of counts up and down won’t matter much.</p>
<p data-id="16ac9db62d266488739d2a2b1a21d664">But there are use cases where the data has to be laser accurate like in banking, stock markets. We just cannot have our systems to be <em>Eventually Consistent</em>, we need <em>Strong Consistency</em>.</p>
<p data-id="df7455f651926410733e13f12ab6deb5">Let’s discuss it in the next lesson.</p>
</div></div></div></div></div></div></div></div></div>