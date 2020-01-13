---
id: introduction-to-message-queues-m7aoo5jkw90
title: Introduction to Message Queues
sidebar_label: Introduction to Message Queues
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the message queues and their functionalities.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-message-queue">What Is A Message Queue?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#features-of-a-message-queue">Features Of A Message Queue</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-world-example-of-a-message-queue">Real World Example Of A Message Queue</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#message-queue-in-running-batch-jobs">Message Queue In Running Batch Jobs</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-message-queue" data-id="35004a50d7fa15f37861ed4d155f14d5">What Is A Message Queue? <a class="markdownIt-Anchor" href="#what-is-a-message-queue"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="4478421a64e68df6e3ee2dd52544cbde">
<p>Message queue as the name says is a <em>queue</em> which routes messages from the source to the destination or we can say from the sender to the receiver.</p>
</blockquote>
<p data-id="d2d494df4565bc5ebf53dee89fa6407d">Since it is a <em>queue</em> it follows the <em>FIFO (First in First Out)</em> policy. The message that is sent first is delivered first. Though messages do have a priority attached with them that makes the queue a <em>priority queue</em> but for now let’s keep things simple.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_6744669151035392_image_5927735367041024.jpeg" alt=""></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="features-of-a-message-queue" data-id="6d5a294bee98f604de3b6f3ab6a044a5">Features Of A Message Queue <a class="markdownIt-Anchor" href="#features-of-a-message-queue"><span class="anchor-link">#</span></a></h2>
<p data-id="97ac4c606e632d3ee3698807ebb81f31">Message queues facilitate asynchronous behaviour. We have already learned what asynchronous behaviour is in the <em>AJAX</em> lesson. Asynchronous behaviour allows the modules to communicate with each other in the background without hindering their primary tasks.</p>
<p data-id="373e205985b27ab9efc34438190dbbec">We will understand the behaviour of message queues with the help of an example in a short while, for now, let’s have a quick look at the features of the message queues.</p>
<p data-id="07512162417c0729e81d99228ca740b3">Message queues facilitate <em>cross-module communication</em> which is key in <em>service-oriented</em> or <em>microservices</em> architecture. It allows communication in a heterogeneous environment. They also provide temporary storage for storing messages until they are processed &amp; consumed by the consumer.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-world-example-of-a-message-queue" data-id="94b2c840a081a08d4b841e127c78aca4">Real World Example Of A Message Queue <a class="markdownIt-Anchor" href="#real-world-example-of-a-message-queue"><span class="anchor-link">#</span></a></h2>
<p data-id="0f7da27367535ab7164f7ed4d1f8dbd1">Think of email as an example, both the sender and receiver of the email don’t have to be online at the same moment to communicate with each other.
The sender sends an email, the message is temporarily stored on the message server until the recipient comes online and reads the message.</p>
<p data-id="0cff77b83725968622918ac8a1f37d23">Message queues enable us to run background processes, tasks, batch jobs. Speaking of background processes, let’s understand this with the help of a use case.</p>
<p data-id="e47d93987a17c4bf8aa46704ee29aaf9">Think of a user signing up on a portal. After he signs up, he is immediately allowed to navigate to the home page of the application, but the sign-up process isn’t complete yet. The system has to send a confirmation email to the registered email id of the user. Then the user has to click on the confirmation email for the confirmation of the sign-up event.</p>
<p data-id="d69f63fc1e924e5577dee8a29f6535ec">But the website cannot keep the user waiting until it sends the email to the user. Either he is allowed to navigate to the home page or he bounces off.  So, this task is assigned as an asynchronous background process to a message queue. It sends an email to the user for confirmation while the user continues to browse the website.</p>
<p data-id="85cd3ec38a7f661dd6436e8968abd0cc">This is how a message queue can be used to add asynchronous behaviour to a web application. Message queues are also used to implement notification systems just like Facebook notifications. I’ll discuss that in the upcoming lessons.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="message-queue-in-running-batch-jobs" data-id="6edc500940c46cb75ca2dfe32b795235">Message Queue In Running Batch Jobs <a class="markdownIt-Anchor" href="#message-queue-in-running-batch-jobs"><span class="anchor-link">#</span></a></h2>
<p data-id="298b44becbcfad8c9879aa473df9bcaa">Now coming to the batch jobs. Do you remember the scenario from the previous caching lesson where I discussed how I used the cache to cut down the application deployment costs?</p>
<p data-id="0a0b544eda769f7e5ffdedaa5f96dbcd">The batch job which updated the stock prices at regular intervals in the database was run by a message queue.</p>
<p data-id="0dbefcec464cd544da01c1709deb23dc">So, by now I am sure we kind of have an idea what a message queue is why do we use it in applications.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="deea68f1ad85f9ad2226d4ee370f9cda">So, we now have a basic understanding that there is a <em>queue</em>, there is a message sender also called the <em>producer</em> and there is a message receiver also called the <em>consumer</em>.</p>
<p data-id="d08417b052ebe873c6bff27c626679f0">Both the <em>producer</em> and the <em>consumer</em> don’t have to reside on the same machine to communicate, that is pretty obvious.</p>
<p data-id="79dcc3255d9a06560f7e8c3f7d37abf5">In this routing of messages through the <em>queue</em>, we can define several rules based on our business requirements. Adding priority to the messages is one I pointed out. Other important features of queuing include message acknowledgements, retrying failed messages etc.</p>
<p data-id="39f93a23294cb8ab3f8c1fe652cd8bf9">Speaking of the size of the queue, there is no definite size, it can be an infinite buffer, depending on the infrastructure the business has.</p>
<p data-id="0ed18df4b5c45701e2dda0df35918c0f">We’ll now look into the messaging models widely used in the industry, beginning with the <em>publish subscribe</em> message routing model, which is pretty popular in today’s online universe. Also, it is how we consume information at large.</p>
</div></div></div></div></div></div></div></div></div>