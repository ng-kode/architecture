---
id: how-to-pick-the-right-server-side-technology-qa9gjeo6p97
title: How to Pick the Right Server-Side Technology?
sidebar_label: How to Pick the Right Server-Side Technology?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we’ll learn how to pick the right server-side technology for our projects.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li>
<ul>
<li><a href="#real-time-data-interaction">Real-time Data Interaction</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#peer-to-peer-web-application">Peer to Peer Web Application</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#crud-based-regular-application">CRUD-based Regular Application</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#simple-small-scale-applications">Simple, Small Scale Applications</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#cpu-memory-intensive-applications">CPU &amp; Memory Intensive Applications</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="7cec0556bd36a6931cd10d4b183441d0">Before commencing the lesson, I would like to say that there is no rule of thumb that for a use case <em>X</em> you should always pick a technology <em>Y</em>.</p>
<p data-id="73e3bb6570f3c0be20a35892b04955d6">Everything depends on our business requirements. Every use case has its unique needs. There is no perfect tech, everything as has its pros &amp; cons. You can be as creative as you want. There is no rule that holds us back.</p>
<p data-id="ef5c9b30bd26105a0582982d36601b97">Alright, this being said. I have listed some of the general scenarios or I can say the common use cases in the world of application development and the fitting backend technology for those based on my development experience.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="real-time-data-interaction" data-id="d44df88cecaac28afbf95d8d496e3ed0">Real-time Data Interaction <a class="markdownIt-Anchor" href="#real-time-data-interaction"><span class="anchor-link">#</span></a></h3>
<p data-id="ecd0ca85358b449d5b1323cdff9f3395">If you are building an app that needs to interact with the backend server in real-time like stream data to &amp; fro. For instance, a messaging application, a real-time browser-based massive multiplayer game, a real-time collaborative text editor or an audio-video streaming app like <em>Spotify</em>, <em>Netflix</em> etc.</p>
<p data-id="f9e0386bbfeb6fb44b2653fa080bd23c">You need a <em>persistent connection</em> between the client and server, also you need a <em>non-blocking</em> technology on the back-end. We’ve already talked about both the concepts in detail.</p>
<p data-id="fad833f1586687f66dba9d39dcbeac3f">Some of the popular technologies which enable us to write these apps are <em>NodeJS</em>, <em>Python</em> has a framework called <em>Tornado</em>. If you are working in the <em>Java</em> Ecosystem you can look into <em>Spring Reactor</em>, <em>Play</em>, <em><a href="http://Akka.io" target="_blank">Akka.io</a></em>.</p>
<p data-id="6ed51517ac84f8a044dfbf45354d1ff9">Once you start researching on these technologies, go through the architecture, concepts given in the developer docs. You’ll gain further insights into how things work, what other tech and concepts I can leverage to implement my use case. One thing leads us to the other.</p>
<p data-id="d661748506d2b436ef7e3070a535433d">This is a good read how <a href="https://foundation.nodejs.org/wp-content/uploads/sites/50/2017/09/Nodejs-at-Uber.pdf" target="_blank">Uber uses NodeJS to scale their business</a></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="peer-to-peer-web-application" data-id="61edc4ffbf09107380d2e0e7c5b98756">Peer to Peer Web Application <a class="markdownIt-Anchor" href="#peer-to-peer-web-application"><span class="anchor-link">#</span></a></h3>
<p data-id="a183e68de0e6d96918b9c2668d73bbe5">If you intend to build a <em>peer to peer</em> web app, for instance, a <em>P2P</em> distributed search engine or a <em>P2P</em> Live TV radio service, something similar to <em>LiveStation</em> by <em>Microsoft</em>.</p>
<p data-id="e9fb358c6bdc168900846762bb4e8aee">Look into <em>JavaScript</em>, protocols like <em>DAT</em>, <em>IPFS</em>. Checkout <em>FreedomJS</em>, it’s a framework for building <em>P2P</em> web apps that work in the modern web browsers.</p>
<p data-id="c82661fbc9fc07f02d2561d657929d78">This is a good read <a href="https://arstechnica.com/information-technology/2014/04/netflix-researching-large-scale-peer-to-peer-technology-for-streaming/" target="_blank">Netflix researching on Peer to peer technology for streaming data.</a></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="crud-based-regular-application" data-id="2f6a60da64ee977f50c66ab42f809a7a">CRUD-based Regular Application <a class="markdownIt-Anchor" href="#crud-based-regular-application"><span class="anchor-link">#</span></a></h3>
<p data-id="e3b3758f6c51b50ae298bdca466bb523">If you have simple use cases such as a regular <em>CRUD-based</em> app like online movie booking portal, a tax filing app etc.</p>
<p data-id="4bbfb0ed2758841f20c7606d8dd66c69"><em>CRUD (Create Read Update Delete)</em> is the most common form of web apps being built today by businesses. Be it an online booking portal, an app collecting user data or a social site etc. all have an <em>MVC (Model View Controller)</em> architecture on the backend.</p>
<p data-id="6233de3e9b818bca1cc994dad4017b19">Though the view part is tweaked a little with the rise of <em>UI</em> frameworks by <em>React</em>, <em>Angular</em>, <em>Vue</em> etc. The <em>Model View Controller</em> pattern stays.</p>
<p data-id="07d8fbd118074179c2775e93bd4f51bc">Some of the popular technologies which help us implement these use cases are <em>Spring MVC</em>, <em>Python Django</em>, <em>Ruby on Rails</em>, <em>PHP Laravel</em>, <em>ASP .NET MVC</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="simple-small-scale-applications" data-id="11fa355f45ea40267526625703e5dcb6">Simple, Small Scale Applications <a class="markdownIt-Anchor" href="#simple-small-scale-applications"><span class="anchor-link">#</span></a></h3>
<p data-id="363a9cf59e610a7d9ea1395472b166c5">If you intend to write an app which doesn’t involve much complexity like a blog, a simple online form, simple apps which integrate with social media that run within in the IFrame of the portal. This includes web browser-based strategy, airline, football manager kind of games. You can pick <em>PHP</em>.</p>
<p data-id="d4827d001931d560916603e70aab52df"><em>PH</em>P is ideally used in these kinds of scenarios. We can also consider other web frameworks like <em>Spring boot</em>, <em>Ruby on Rails</em>, which cut down the verbosity, configuration, development time by notches &amp; facilitate rapid development. But <em>PHP</em> hosting will cost much less in comparison to hosting other technologies. It is ideal for very simple use cases.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="cpu-memory-intensive-applications" data-id="6fb5ef4c2a7d50d8d5223b0d7e0b1a80">CPU &amp; Memory Intensive Applications <a class="markdownIt-Anchor" href="#cpu-memory-intensive-applications"><span class="anchor-link">#</span></a></h3>
<p data-id="464110e653800fb4cbe313b61f91cbcd">Do you need to run <em>CPU</em> Intensive, <em>Memory</em> Intensive, heavy computational tasks on the backend such as <em>Big Data Processing</em>, <em>Parallel Processing</em>, Running <em>Monitoring &amp; Analytics</em> on quite a large amount of data?</p>
<p data-id="551895c6c174d46921794c34d71dbbdc">Performance is critical in systems running tasks which are <em>CPU</em> &amp; <em>Memory</em> intensive. Handling massive amounts of data has its costs. A system with high latency &amp; memory consumption can blow up the economy of a tech company.</p>
<p data-id="b18bc3ae8dcd845a4fb9246e2e34eb6b">Also, regular web frameworks &amp; scripting languages are not meant for number crunching.</p>
<p data-id="2272b17e7a0159ac873d1ab5a795930d"><em>Tech commonly used in the industry to write performant, scalable, distributed systems are –</em></p>
<p data-id="183aad118ffe7302d3ead21996aebf2c"><em>C++</em>, it has features that facilitate low-level memory manipulation. Provides more control over memory to the developers when writing distributed systems. <a href="https://en.wikipedia.org/wiki/List_of_cryptocurrencies" target="_blank">Majority of the cryptocurrencies are written using this language</a>.</p>
<p data-id="fc41b52f3de03263b707baf80ea6b91f"><em>Rust</em> is a programming language similar to <em>C++</em>. It is built for high performance and safe concurrency. It’s gaining a lot of popularity lately amongst the developer circles.</p>
<p data-id="e9b713a3bd2b985fbaa83a7bdfb89e1a"><em>Java</em>, <em>Scala</em> &amp; <em>Erlang</em> are also a good pick. Most of the large scale enterprise systems are written in <em>Java</em>.</p>
<p data-id="522a9dd873d405c9133a7ed2a1d35b18"><a href="https://en.wikipedia.org/wiki/Elasticsearch" target="_blank">Elastic search</a> an open-source real-time search and analytics engine is written in <em>Java</em>.</p>
<p data-id="291a8eb21f4702f4d558c499dafe9ee2"><em>Erlang</em> is a functional programming language with built-in support for concurrency, fault-tolerance &amp; distribution. It facilitates the development of massively scalable systems. <a href="https://stackoverflow.com/questions/1636455/where-is-erlang-used-and-why" target="_blank">This is a good read on Erlang</a></p>
<p data-id="a767e6b178e5f07f213704cab6ed5cb5"><em>Go</em> is a programming language by <em>Google</em> to write apps for multi-core machines &amp; handling a large amount of data.</p>
<p data-id="f331e915bc7a4f95b4d90b78094199c0"><em>Julia</em> is a dynamically programmed language built for high performance &amp; running computations &amp; numerical analytics.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="1562ffde8bfc03f2ce3e061a7cf4be12">Well, this is pretty much it. In the next lesson, let’s talk about a few key things which we should bear in mind when researching on picking a fitting technology stack for our project.</p>
</div></div></div></div></div></div></div></div></div>