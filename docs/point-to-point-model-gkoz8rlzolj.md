---
id: point-to-point-model-gkoz8rlzolj
title: Point to Point Model
sidebar_label: Point to Point Model
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the point to point messaging model, its applications, popular message queue protocols &amp; the technology used to implement them. </p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-point-to-point-model">What Is Point to Point Model?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#messaging-protocols">Messaging Protocols</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#technology-used-to-implement-the-messaging-protocols">Technology Used To Implement the Messaging Protocols</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-point-to-point-model" data-id="a9fe42474645a7038def2b4b7c16a37f">What Is Point to Point Model? <a class="markdownIt-Anchor" href="#what-is-point-to-point-model"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="430519467042412813ec35c1b7053757">
<p><em>Point to point</em> communication is a pretty simple use case where the message from the producer is consumed by only one consumer.</p>
</blockquote>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5325654478290944_image_6547336517910528.jpeg" alt=""></p>
<p data-id="170c97e1047af703b0586cac38c8a8f0">It’s like a <em>one to one</em> relationship, a <em>publish-subscribe</em> model is a <em>one to many</em> relationship.</p>
<p data-id="29fb78b53139627ee42495f0b6522f09">Though based on the business requirements we can set up multiple combinations in this messaging model, like adding multiple producers &amp; consumers to a queue. But at the end of the day, a message sent by the producer will be consumed by only one consumer. This is why it’s called a <em>point to point</em> queuing model. It’s not a broadcast of messages rather an entity to entity communication.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="messaging-protocols" data-id="494bcf208d121aa181788e3377218b94">Messaging Protocols <a class="markdownIt-Anchor" href="#messaging-protocols"><span class="anchor-link">#</span></a></h2>
<p data-id="40af6814f8f770bb042aa751a5f3681e">Speaking of the messaging protocols, there are two protocols popular when working with message queues. <a href="https://en.wikipedia.org/wiki/Advanced_Message_Queuing_Protocol" target="_blank">AMQP Advanced Message Queue Protocol</a> &amp; <a href="https://en.wikipedia.org/wiki/Streaming_Text_Oriented_Messaging_Protocol" target="_blank">STOMP Simple or Streaming Text Oriented Message Protocol</a>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="technology-used-to-implement-the-messaging-protocols" data-id="1edac0daece976610bfb68f1cb6a3346">Technology Used To Implement the Messaging Protocols <a class="markdownIt-Anchor" href="#technology-used-to-implement-the-messaging-protocols"><span class="anchor-link">#</span></a></h2>
<p data-id="2e5e3bf0dedcc54701ad25172fe77b47">Speaking of the queuing tech widely used in the industry, they are <em>RabbitMQ</em>, <em>ActiveMQ</em>, <em>Apache Kafka</em> etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="5e90650d2dd10f39f8b7db5182b8cfa0">So, Guys!! this is pretty much it on the queuing models. Now, let’s have an insight into how do notification systems work with message queues.</p>
</div></div></div></div></div></div></div></div></div>