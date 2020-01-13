---
id: event-driven-architecture-part-1-n8rzvyo5rpk
title: Event Driven Architecture - Part 1
sidebar_label: Event Driven Architecture - Part 1
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, which is the part one of the event driven architecture, we will understand concepts like Blocking &amp; Non-blocking.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-blocking">What Is Blocking?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-is-non-blocking">What Is Non-Blocking?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="2970d487ebef4306b820b300b485736b">When writing modern Web 2.0 applications chances are you have across terms like <em>Reactive programming</em>, <em>Event-driven architecture</em>, concepts like <em>Blocking</em> &amp; <em>Non-blocking</em>.</p>
<p data-id="40a6f9b6e3a1fad704c67c83049b7cb6"><em>What are they? Should I be aware of them?</em></p>
<p data-id="b663b0bd2ad55e0c5fb4849ea88d48ea">You might have also noticed that tech like <em>NodeJS</em>, <em>Play</em>, <em>Tornado</em>, <em><a href="http://Akka.io" target="_blank">Akka.io</a></em> are gaining more popularity in the developer circles for modern application development in comparison to the traditional tech.</p>
<p data-id="3557ecc5fe1b992812fe5e547bf9c403">What is the reason for that? Is it just that we are bored of working on the traditional tech like <em>Java</em>, <em>PHP</em> etc. &amp; are attracted towards the shiny new stuff or are there any technical reasons behind this?</p>
<p data-id="0248a93058b253dbcdaa742eeb049c4d">In this lesson, we will go through each and every concept step by step &amp; realize the demands of modern software application development.</p>
<p data-id="3f99b39ae76df941b664850e04444cbb">So, without any further ado, let’s get on with it.</p>
<p data-id="03be94f958f7c2a8f55c70e190f07b79">Alright, at this point in the course, we know what <em>persistent connections</em> are? What <em>asynchronous behaviour</em> is &amp; why do we need it? We can’t really write real-time apps without implementing them.</p>
<p data-id="23eb2e6647ef4a8e58538d4bf7726465">Starting with <em>Blocking</em>. What is it?</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-blocking" data-id="8280ab6354f9297dc56ec4f19c8957e2">What Is Blocking? <a class="markdownIt-Anchor" href="#what-is-blocking"><span class="anchor-link">#</span></a></h2>
<p data-id="d90b74ea1d5ac17562b8e5dfb353ac77">In web applications <em>blocking</em> means the flow of execution is blocked waiting for a process to complete. Until the process completes it cannot move on. Let’s say we have a block of code of 10 lines within a function and every line triggers another external function executing a specific task.</p>
<p data-id="2f9c55b5eeb7134042d5c65793dd2be6">Naturally, when the flow of execution enters the main function it will start executing the code from the top, from the first line. It will run the first line of code and will call the external function.</p>
<p data-id="f093f7905cbd48d231b2731de07c10af">At this point in time until the external function returns the response. The flow is blocked. The flow won’t move further, it just waits for the response. Unless we add <em>asynchronous behaviour</em> to it by annotating it and moving the task to a separate thread. But that’s not what happens in the regular scenario, like in the regular <em>CRUD-based</em> apps. Right?</p>
<p data-id="4e42d3a4ab847bcd883a348c26f14b73">So, this behaviour is known as <em>Blocking</em>. The flow of execution is blocked.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-non-blocking" data-id="98cba3cfe117dbcf3a69c7ae5050205d">What Is Non-Blocking? <a class="markdownIt-Anchor" href="#what-is-non-blocking"><span class="anchor-link">#</span></a></h2>
<p data-id="2460e00e1fe431f98cda99929a629d57">Now coming to the <em>Non-blocking</em> approach. In this approach the flow doesn’t wait for the first function, that is called, to return the response. It just moves on to execute the next lines of code. This approach is a little not so consistent as opposed to the blocking approach since a function might not return anything or throw an error, still the code in the sequence up next is executed.</p>
<p data-id="07ca6407dbc9f560929511f0f7362077">The <em>non-blocking</em> approach facilitates <em>IO Input-Output</em> intensive operations. Besides the disk &amp; other the hardware-based operations, communication and network operations also come under the <em>IO</em> operations.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="d1b051cc6b7764f49675446666ad901b">We will continue this discussion in part two of event-driven architecture lesson. We will have an insight into what are events? what is event-driven architecture? And the technologies used to implement it.</p>
</div></div></div></div></div></div></div></div></div>