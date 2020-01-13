---
id: publish-subscribe-model-q2nll5wzgbk
title: Publish Subscribe Model
sidebar_label: Publish Subscribe Model
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the Publish-Subscribe model, when it is used &amp; what are Exchanges in messaging?</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-publish-subscribe-model">What Is A Publish Subscribe Model?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#exchanges">Exchanges</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-publish-subscribe-model" data-id="9b1bed790bd67bf5194298c2e981422c">What Is A Publish Subscribe Model? <a class="markdownIt-Anchor" href="#what-is-a-publish-subscribe-model"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="482d1fba228c60e9f58312e24db1035f">
<p>A <em>Publish-Subscribe</em> model is the model where multiple consumers receive the same message sent from a single or multiple producers.</p>
</blockquote>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/courses_web-application-software-architecture-101_assets_api_collection_6064040858091520_6411938009448448_page_5270046194532352_image_5842943451594752.jpeg.jpeg" alt=""></p>
<p data-id="e097fffd53c85051f1e0f47a6621feb7">A real-world newspaper service is a good analogy for the <em>publish-subscribe</em> pattern, where the consumers subscribe to a newspaper service, and the service delivers the news to the multiple consumers of its service, every single day.</p>
<p data-id="cef7dceef2a9579796f620271c9bbf80">In the online world, we often subscribe to various topics in applications to be continually notified of the new updates on any particular segment. Be it sports, politics, or economics etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="exchanges" data-id="db0f19f27e4827cc37561bae628203e9">Exchanges <a class="markdownIt-Anchor" href="#exchanges"><span class="anchor-link">#</span></a></h2>
<p data-id="09ebab94cd6fafc1b172036f753743df">To implement the <em>pub-sub</em> pattern, message queues have <em>exchanges</em> which further push the messages to the queues based on the exchange type and the rules which are set. <em>Exchanges</em> are just like telephone exchanges which route messages from sender to the receiver through the infrastructure based on a certain logic.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/courses_web-application-software-architecture-101_assets_api_collection_6064040858091520_6411938009448448_page_5270046194532352_image_4632709445976064.jpeg.jpeg" alt=""></p>
<p data-id="844e1366d3692710fe25935d46d1fc60">There are different types of exchanges available in message queues, some of which are, <em>direct</em>, <em>topic</em>, <em>headers</em>, <em>fanout</em>. To have more insight into how these different exchange types work, <a href="https://www.rabbitmq.com/tutorials/amqp-concepts.html" target="_blank">this RabbitMQ article is a good read</a>.</p>
<p data-id="9cf818efe9309547389112d772ab767b">There is no certainty that every message queue tech will have the same exchange type. These are just general scenarios I am discussing here. Things can change with technologies. Besides, technology is not important, all you need right now is just an idea of how things work.</p>
<p data-id="93fbf723a27e4bc862833e4fcb6f3e7a">So, we would pick a <em>fanout</em> exchange type to broadcast the messages from the queue. The exchange will push the message to the queue and the consumers will receive the message. The relationship between exchange and the queue is known as <em>Binding</em>.</p>
<p data-id="4415949b8249ff8372b5c3c492cc30bc">This is how we get updates of new content generated in real-time on social apps by businesses or individuals followed by a lot of people.</p>
<p data-id="422d96636b4b026a35711b9599ecb2b6">In the upcoming lessons, I will discuss this in detail how real-time feeds and notification systems work in social networks powered by the message queues.</p>
<p data-id="24bdd035c2f45b8291f7b84756a3a3cb">Let’s move on to the point to point messaging model.</p>
</div></div></div></div></div></div></div></div></div>