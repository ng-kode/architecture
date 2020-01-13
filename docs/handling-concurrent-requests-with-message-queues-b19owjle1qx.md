---
id: handling-concurrent-requests-with-message-queues-b19owjle1qx
title: Handling Concurrent Requests With Message Queues
sidebar_label: Handling Concurrent Requests With Message Queues
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will have an insight into how concurrent requests are handled with a message queue.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#using-a-message-queue-to-handle-the-traffic-surge">Using A Message Queue To Handle the Traffic Surge</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#how-facebook-handles-concurrent-requests-on-its-live-video-streaming-service-with-a-message-queue">How Facebook Handles Concurrent Requests On Its Live Video Streaming Service With a Message Queue?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="using-a-message-queue-to-handle-the-traffic-surge" data-id="ce254b3e357a6f668e6624502f5436ce">Using A Message Queue To Handle the Traffic Surge <a class="markdownIt-Anchor" href="#using-a-message-queue-to-handle-the-traffic-surge"><span class="anchor-link">#</span></a></h2>
<p data-id="4fb453989c15745d86d0b07fd51dfb3a">In the distributed <em>NoSQL</em> databases lesson, we learned about <a href="https://www.educative.io/collection/page/6064040858091520/6411938009448448/6373547041619968" target="_blank">Eventual Consistency</a> &amp; <a href="https://www.educative.io/collection/page/6064040858091520/6411938009448448/5677430486335488" target="_blank">Strong Consistency</a>. We discussed how both the consistency models come into effect when incrementing the value of a “<em>Like</em>” counter.</p>
<p data-id="7b6fd1bd221e2253fbbb06e7638e277a">Here is a quick insight into a way where we can use a message queue to manage a high number of concurrent requests to update an entity.</p>
<p data-id="a33644c51f506c02db99a9f6df1c00bc">When millions of users around the world update an entity concurrently, we can queue all the update requests in a high throughput message queue. Then we can process them one by one in a <em>FIFO First in First Out</em> approach sequentially.</p>
<p data-id="7376adf255b617e6b07f1879294b7f93">This would enable the system to be highly available, open to updation &amp; still being consistent at the same time.</p>
<p data-id="e9b4ef686f8258625954cdba1384c0ed">Though the implementation of this approach is not as simple as it sounds, implementing anything in a distributed real-time environment is not so trivial. I thought I will just bring this approach up so that you guys can meditate upon this.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="how-facebook-handles-concurrent-requests-on-its-live-video-streaming-service-with-a-message-queue" data-id="9b20b053ac8f8df1de54dcf468b7e27a">How Facebook Handles Concurrent Requests On Its Live Video Streaming Service With a Message Queue? <a class="markdownIt-Anchor" href="#how-facebook-handles-concurrent-requests-on-its-live-video-streaming-service-with-a-message-queue"><span class="anchor-link">#</span></a></h2>
<p data-id="779c150dd00d44fcffac40c80aad9ec2">Facebook’s approach of handling concurrent user requests on its LIVE video streaming service is another good example of how queues can be used to efficiently handle the traffic surge.</p>
<p data-id="f8d2ba551ae13fc8fcc81c39a3721dd4">On the platform, when a popular person goes LIVE there is a surge of user requests on the LIVE streaming server. To avert the incoming load on the server Facebook uses cache to intercept the traffic.</p>
<p data-id="2f8ee5d922976e207209d8dbedc64a35">But, since the data is streamed LIVE often the cache is not populated with real-time data before the requests arrive. Now, this would naturally result in a <em>cache-miss</em> &amp; the requests would move on to hit the streaming server.</p>
<p data-id="e41783349bde2cee0aa359c18ad12be1">To avert this, Facebook queues all the user requests, requesting for the same data. It fetches the data from the streaming server, populates the cache &amp; then serves the queued requests from the cache.</p>
<p data-id="d08cdd2a9a9a050e1538b5393b2904cb"><a href="https://engineering.fb.com/ios/under-the-hood-broadcasting-live-video-to-millions/" target="_blank">This is a recommended read on Facebook’s Live Streaming architecture</a>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="e16862e1af81ab23e86219b9b5702fa4">Alright, moving on!! In the next chapter we will take a deep dive into stream processing.</p>
</div></div></div></div></div></div></div></div></div>