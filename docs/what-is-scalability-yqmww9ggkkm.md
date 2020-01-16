---
id: what-is-scalability-yqmww9ggkkm
title: What Is Scalability?
sidebar_label: What Is Scalability?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">This lesson is an introduction to scalability.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-scalability">What is Scalability?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-is-latency">What Is Latency?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#measuring-latency">Measuring Latency</a>
<ul>
<li><a href="#network-latency">Network Latency</a></li>
<li><a href="#application-latency">Application Latency</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li><a href="#why-is-low-latency-so-important-for-online-services">Why Is Low Latency So Important For Online Services?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="89d5384049145f030608c42205d3917e">I am pretty sure, being in the software development universe, you’ve come across this word a lot many times. <em>Scalability</em>. What is it? Why is it so important? Why is everyone talking about it?
Is it important to scale systems? What are your plans or contingencies to scale when your app or the platform experiences significant traffic growth?</p>
<p data-id="5dfcfc52245d579fc7135a3da17a28f8">This chapter is a deep dive into scalability. It covers all the frequently asked questions on it such as: what does scalability mean in the context of web applications, distributed systems or cloud computing? Etc.</p>
<p data-id="130ec72fb77b37fbe8ce1ba0afd56c60">So, without further ado. Let’s get started.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-scalability" data-id="c34ed5254a890c824f6c5a1d2ac24c19">What is Scalability? <a class="markdownIt-Anchor" href="#what-is-scalability"><span class="anchor-link">#</span></a></h2>
<p data-id="af012066d43914a2568e7d22b852f94a">Scalability means the ability of the application to handle &amp; withstand increased workload without sacrificing the latency.</p>
<p data-id="05906c2c0681725f6c8e38179390959c">For instance, if your app takes x seconds to respond to a user request. It should take the same x seconds to respond to each of the million concurrent user requests on your app.</p>
<p data-id="544d6fd35be7d35ba56e448ad962a5b3">The backend infrastructure of the app should not crumble under a load of a million concurrent requests. It should scale well when subjected to a heavy traffic load &amp; should maintain the latency of the system.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5894859313381376_image_5493542946340864.jpeg" alt=""></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-latency" data-id="1145af1bc8e7c709f7da4c1a0d734039">What Is Latency? <a class="markdownIt-Anchor" href="#what-is-latency"><span class="anchor-link">#</span></a></h2>
<p data-id="93c5d1f9929754e61785c21ddcbe4bb7"><em>Latency</em> is the amount of time a system takes to respond to a user request. Let’s say you send a request to an app to fetch an image &amp; the system takes 2 seconds to respond to your request. The latency of the system is 2 seconds.</p>
<p data-id="27c810d0313829669485d201c75a3aa5">Minimum latency is what efficient software systems strive for. No matter how much the traffic load on a system builds up, the latency should not go up. This is what scalability is.</p>
<p data-id="dfde02815e62cdb14f5e1429ff7b4ba7">If the latency remains the same, we can say yeah, the application scaled well with the increased load &amp; is highly scalable.</p>
<p data-id="35c6e3e8b155b92b4a007685b7757bc4">Let’s think of scalability in terms of <em>Big-O notation</em>. Ideally, the complexity of a system or an algorithm should be <em>O(1)</em> which is <em>constant time</em> like in a key-value database.</p>
<p data-id="d74eb55848c348d4abff84a50ec28e7c">A program with the complexity of <em>O(n^2)</em> where n is the size of the data set is not scalable. As the size of the data set increases the system will need more computational power to process the tasks.</p>
<p data-id="4b3df617e1e598818ef2f5aecb37475d"><em>So, how do we measure latency?</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="measuring-latency" data-id="537096344eceabac21279df2e05c598a">Measuring Latency <a class="markdownIt-Anchor" href="#measuring-latency"><span class="anchor-link">#</span></a></h2>
<p data-id="8d91a4fa7be5fec0002284da806225ab">Latency is measured as the time difference between the action that the user takes on the website, it can be an event like the click of a button, &amp; the system response in reaction to that event.</p>
<p data-id="98f1ebb67c0355454d2fcc1e5f05cb16">This latency is generally divided into two parts:</p>
<ol data-id="e26f06c2cd25d90000719e3d29c51f35">
<li>Network Latency</li>
<li>Application Latency</li>
</ol>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5894859313381376_image_4804805030576128.jpeg" alt=""></p>
<h3 id="network-latency" data-id="f21d08829faf985815ba3baa0d5cc34b">Network Latency <a class="markdownIt-Anchor" href="#network-latency"><span class="anchor-link">#</span></a></h3>
<p data-id="a2ca658bf295e13f602b4e310ff625df">Network Latency is the amount of time that the network takes for sending a data packet from point A to point B. The network should be efficient enough to handle the increased traffic load on the website.
To cut down the network latency, businesses use CDN &amp; try to deploy their servers across the globe as close to the end-user as possible.</p>
<h3 id="application-latency" data-id="956d37e10370978aa90c222f27f4d7b6">Application Latency <a class="markdownIt-Anchor" href="#application-latency"><span class="anchor-link">#</span></a></h3>
<p data-id="d8e0d640ca3b2636cc7414dfa7c1288b">Application Latency is the amount of time the application takes to process a user request. There are more than a few ways to cut down the application latency.
The first step is to run stress &amp; load tests on the application &amp; scan for the bottlenecks that slow down the system as a whole. I’ve talked more about it in the upcoming lesson.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="why-is-low-latency-so-important-for-online-services" data-id="f65c0413ad9ffd18345936f85265d8c6">Why Is Low Latency So Important For Online Services? <a class="markdownIt-Anchor" href="#why-is-low-latency-so-important-for-online-services"><span class="anchor-link">#</span></a></h2>
<p data-id="5adf8707bf129883334c40e2c7b384b6">Latency plays a major role in determining if an online business wins or loses a customer. Nobody likes to wait for a response on a website. There is a well-known saying if you want to test a person’s patience, give him a slow internet connection 😊</p>
<p data-id="779e857236cce44fe5351807c8985d42">If the visitor gets the response within a stipulated time, great or he bounces off to another website.</p>
<p data-id="2a83de4b1f40c354e28e5f408f237a12">There are numerous market researches that present the fact that high latency in applications is a big factor in customers bouncing off a website. If there is money involved, zero latency is what businesses want, only if that was possible.</p>
<p data-id="cd4e1aa0ee0a07a6fa0837c47343a28b">Think of massive multiplayer online MMO games, a slight lag in an in-game event ruins the whole experience. A gamer with a high latency internet connection will have a slow response time despite having the best reaction time of all the players in an arena.</p>
<p data-id="8930a264ae7af4824b2e91d4fd4f3c60">Algorithmic trading services need to process events within milliseconds. Fintech companies have dedicated networks to run low latency trading. The regular network just won’t cut it.</p>
<p data-id="867663466b8bf4d6c6296c74cb9fd4ff">We can realize the importance of low latency by the fact that <a href="https://www.telegraph.co.uk/technology/news/8753784/The-300m-cable-that-will-save-traders-milliseconds.html" target="_blank">Huawei &amp; Hibernia Atlantic in the year 2011 started laying a fibre-optic link cable across the Atlantic Ocean between London &amp; Newyork</a>, that was estimated having a cost of approx. $300M, just to save traders 6 milliseconds of latency.</p>
</div></div></div></div></div></div></div></div></div>
