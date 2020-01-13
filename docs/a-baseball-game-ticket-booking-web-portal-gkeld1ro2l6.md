---
id: a-baseball-game-ticket-booking-web-portal-gkeld1ro2l6
title: A Baseball Game Ticket Booking Web Portal
sidebar_label: A Baseball Game Ticket Booking Web Portal
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we’ll discuss the case study of a baseball game online ticket booking application.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#database">Database</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#handling-concurrency">Handling Concurrency</a>
<ul>
<li><a href="#message-queue">Message Queue</a></li>
<li><a href="#database-locks">Database Locks</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li><a href="#caching">Caching</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#backend-tech">Backend Tech</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#user-interface">User Interface</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="a2d69eb7aca47a80cb1ae6195ce3b76f">In this lesson, we’ll have an understanding of the architecture &amp; the key points to consider when designing an application like a baseball game online ticket booking portal.</p>
<p data-id="e37e79ee84a4da9c76194b6f36bc6edf">Let’s get started.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="database" data-id="77b118cce6c1c03a436ac621c802ae98">Database <a class="markdownIt-Anchor" href="#database"><span class="anchor-link">#</span></a></h2>
<p data-id="15ef5e55d77839402cc0701ec88e6660">Starting with the <em>database</em>, one key thing in this particular use case is the sale of tickets online. We need to set up a foolproof payment system for the fans to buy tickets to their most awaited baseball game.</p>
<p data-id="614a945a03782f5a76a755147ce61207"><em>For setting up payments, what do you think what database should we pick &amp; why?</em></p>
<p data-id="3d93aae9e52c090449469a0b39c92d25">Implementing an online payment system makes <em>transactions</em> &amp; <em>strong consistency</em> vital. The database needs to be <em>ACID</em> compliant. This makes a <em>relational database</em> like <em>MySQL</em> an obvious pick for us.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="handling-concurrency" data-id="0a87c2372d3df71c685773d8199b817a">Handling Concurrency <a class="markdownIt-Anchor" href="#handling-concurrency"><span class="anchor-link">#</span></a></h2>
<p data-id="82660729dcda3e4dec59370107fa2b52">Another important thing to note is that the application should be designed to handle a high number of <em>concurrent</em> connections. There will be a surge of fans on the portal, to buy tickets for the baseball game as soon as they are made available.</p>
<p data-id="7dfeee3cf14ea6a12c5187b1772b1726">Also, the number of requests will be a lot more than the number of tickets available.</p>
<p data-id="8ae28f2ddf4b01a4491b8026a1e022a0">At one point in time, there will be n requests to buy one ticket. We need to make sure the system handles this concurrent scenario well.</p>
<p data-id="bb01f74fc9d75769cace9a8a8f67172b"><em>How will you implement this scenario? Think about it</em></p>
<h3 id="message-queue" data-id="392136d481a57b9298d93327b992c6bd">Message Queue <a class="markdownIt-Anchor" href="#message-queue"><span class="anchor-link">#</span></a></h3>
<p data-id="dc5ed26f77c33f4ed77f11625e3ab3b0">One way is to <em>queue</em> all the ticket buy requests using a <em>message queue</em>. Apply the <em>FIFO First In First Out</em> principle. We’ve talked about this in the message queue lesson, handling concurrent requests with the help of message queue.</p>
<h3 id="database-locks" data-id="427ad0076f0fb978cf9ba4f2fd10038e">Database Locks <a class="markdownIt-Anchor" href="#database-locks"><span class="anchor-link">#</span></a></h3>
<p data-id="cfce787202f414c11ea0cb7fe100a546">Another approach is to use <em>database locks</em>. Use the right <em>Transaction Isolation Level</em>.</p>
<p data-id="a30504909aa470fd08cb20c5907e76be">A <em>transaction isolation level</em> ensures <em>consistency</em> in a database transaction. It ensures that at one point in time only one transaction has access to a resource in the database.</p>
<p data-id="7d27349576f777a6e5de36a96b9d11c6">This is a <a href="https://en.wikipedia.org/wiki/Isolation_(database_systems)" target="_blank">good read on it</a>. Also, read <a href="https://en.wikipedia.org/wiki/Snapshot_isolation" target="_blank">snapshot isolation</a></p>
<p data-id="a4a90cc09cc4ec50e77775b4b9dfbffa"><em>Transaction isolation levels</em> can be implemented only with a <em>transactional ACID</em> compliant database like <em>MySQL</em>.</p>
<p data-id="246f71fd21031ff5be6bfd6e27246574">Generally, in e-commerce sites or when booking travel tickets, the number of tickets shown on the website are not accurate, they are the cached values. When a user moves on to buy a particular ticket, checks out the cart, then the system polls the database for the accurate value &amp; locks the resource for the transaction.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="caching" data-id="8330f29f6da6e8e986662b9ac8ebb44b">Caching <a class="markdownIt-Anchor" href="#caching"><span class="anchor-link">#</span></a></h2>
<p data-id="72d8b0c89859a31407253df689533591">Speaking of <em>caching</em>. Pick any of the popular caches like <em>Redis</em>, <em>Memcache</em> or <em>Hazelcast</em> to implement caching. There are a lot number of user events on the portal where the users just browse the website to look at the current price of the tickets and not buy them. Caching averts the load on the database in this scenario.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="backend-tech" data-id="78df883e6a6e97385f8ddb31a75c5133">Backend Tech <a class="markdownIt-Anchor" href="#backend-tech"><span class="anchor-link">#</span></a></h2>
<p data-id="4d6ec5836693dd460a63b1449cf07926">Speaking of the backend technology, we can take a pick from <em>Java</em>, <em>Scala</em>, <em>Python</em>, <em>Go</em> etc.</p>
<p data-id="3e421f1c1bf86ff20e99a2ec081064db">To send notifications to the users we can pick a message queue like <em>RabbitMQ</em> or <em>Kafka</em>.</p>
<p data-id="71b4a29f4182d526d32300719fa823bb">Let’s move to the UI</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="user-interface" data-id="35b3e99244601321f151cf6e6b8d0473">User Interface <a class="markdownIt-Anchor" href="#user-interface"><span class="anchor-link">#</span></a></h2>
<p data-id="0fa5fddb83b3e9a5b75112bc8b7785ca">We don’t really need to establish a <em>persistent connection</em> with the server as the application is kind of a <em>CRUD Create Read Update Delete</em> based app. Simple <em>Ajax</em> queries will work good.</p>
<p data-id="9ff84b982a5824594d1fbdf434eb731a">It’s a good idea to make the <em>UI responsive</em>, as fans will access it via devices having different screen sizes. The <em>UI</em> should be smart enough to adjust itself based on the screen size.</p>
<p data-id="4f58bed6ddc07aa1178d11dc848a31f0">We can either design the responsive behaviour from the ground up using <em>CSS3</em> or leverage a popular <em>open-source</em> responsive framework like <em>Bootstrap JS</em>.</p>
<p data-id="5bd46d84ae65121a7f8acf243bf084c9">If you are fond of <em>JavaScript</em> frameworks you can use a framework like <em>React</em>, <em>Angular</em>, <em>Vue</em> etc. These frameworks are pretty popular in the industry &amp; businesses prefer to use them to standardize the behaviour &amp; the implementation of their applications.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="bbe74d5d93c00ced243cc78ea5f580f7">Well, this pretty much sums the case study on a baseball ticket booking web portal.</p>
</div></div></div></div></div></div></div></div></div>