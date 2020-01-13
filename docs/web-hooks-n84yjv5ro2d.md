---
id: web-hooks-n84yjv5ro2d
title: Web Hooks
sidebar_label: Web Hooks
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we’ll understand the need for web hooks &amp; how do they work?</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-are-web-hooks">What Are Web Hooks?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#how-do-web-hooks-work">How Do Web Hooks Work?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-are-web-hooks" data-id="5d1b9e437fdbe950af541280a155f4ab">What Are Web Hooks? <a class="markdownIt-Anchor" href="#what-are-web-hooks"><span class="anchor-link">#</span></a></h2>
<p data-id="87982ff4b0f7d38b4279c54854a76f09">Imagine you’ve written an <em>API</em> which provides information on the latest exclusive events on <em>Baseball</em>. Now your <em>API</em> is consumed by a lot many third-party services, that fetch the information from the API, add their own flavour to it &amp; present it before their users.</p>
<p data-id="b1dc2d4cc61369d0d700c24fd8e607ff">But so many API requests every now and then, just to check if a particular event has occurred is crushing your server. The server can hardly keep up with the requests. There is no way for consumers to know that the new information isn’t available on the server yet, or an event hasn’t occurred yet. They just keep polling the API. This would eventually pile up the unwanted load on the server and could bring it down.</p>
<p data-id="a868213bb77999ab7e1ad47293c5b15d"><em>What do we do? Is there a way we can cut down the load on our servers?</em></p>
<p data-id="a89bdf19b2b973917fff30e07b519c10">Yes!! <em>WebHooks</em>.</p>
<p data-id="8c9dee3f3ca9d8aab08c6aa48ef67730"><em>WebHooks</em> are more like <em>call-backs</em>. It’s like I will call you when new information is available. You carry on with your work.</p>
<p data-id="f5532122d6b233846a91de401b2a5b7a"><em>WebHooks</em> enable communication between two services without a middleware. They have an <em>event-based</em> mechanism.</p>
<p data-id="dcac764685482a1270970738b4bf941b"><em>So, how do they work?</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="how-do-web-hooks-work" data-id="578dc4efbc0d002a0a8fd2e347e9fb15">How Do Web Hooks Work? <a class="markdownIt-Anchor" href="#how-do-web-hooks-work"><span class="anchor-link">#</span></a></h2>
<p data-id="3ed4c15803e7c4a75cdfd16d931a8771">To use the <em>Webhooks</em>, consumers register an <em>HTTP</em> endpoint with the service with a unique <em>API</em> Key. It’s like a phone number. Call me on this number, when an event occurs. I won’t call you anymore.</p>
<p data-id="174706b2202e81b3dec32c3fff13732d">Whenever the new information is available on the backend. The server fires an <em>HTTP</em> event to all the registered endpoints of the consumers, notifying them of the new update.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5429868697223168_image_4954686534713344.jpeg" alt=""></p>
<p data-id="db6607d811102eb7539523b6217fe6bd">Browser notifications are a good example of <em>Webhooks</em>. Instead of visiting the websites every now and then for new info, the websites notify us when they publish new content.</p>
</div></div></div></div></div></div></div></div></div>