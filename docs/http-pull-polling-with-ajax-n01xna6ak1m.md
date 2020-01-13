---
id: http-pull-polling-with-ajax-n01xna6ak1m
title: HTTP Pull - Polling with Ajax
sidebar_label: HTTP Pull - Polling with Ajax
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will understand HTTP Pull, AJAX and how polling is done using AJAX.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li>
<ul>
<li><a href="#ajax-asynchronous-javascript-xml">AJAX – Asynchronous JavaScript &amp; XML</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="2bcd691856b67a335a36d66e0e16df47">There are two ways of pulling/fetching data from the server.</p>
<p data-id="a8fcc7f88f45e22c475009e8deddf2a3">The first is sending an <em>HTTP GET</em> request to the server manually by triggering an event, like by clicking a button or any other element on the web page.</p>
<p data-id="354b76c66e4cef9f7b66fac162803de9">The other is fetching data dynamically at regular intervals by using <em>AJAX</em> without any human intervention.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="ajax-asynchronous-javascript-xml" data-id="6fc20b5c09e694863c1b6ce1eb059168">AJAX – Asynchronous JavaScript &amp; XML <a class="markdownIt-Anchor" href="#ajax-asynchronous-javascript-xml"><span class="anchor-link">#</span></a></h3>
<blockquote data-id="075ab36e810a5d6d8a92b19034b0c3e6">
<p><em>AJAX</em> stands for asynchronous <em>JavaScript</em> &amp; <em>XML</em>. The name says it all, it is used for adding asynchronous behaviour to the web page.</p>
</blockquote>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4541869587431424_image_5892486276841472.jpeg" alt=""></p>
<p data-id="b9c407e47d95e9b4783efd8fc014e738">As we can see in the illustration above, instead of requesting the data manually every time with the click of a button. AJAX enables us to fetch the updated data from the server by automatically sending the requests over and over at stipulated intervals.</p>
<p data-id="b8f82e61cf3aca16aa4485ee2437692f">Upon receiving the updates, a particular section of the web page is updated dynamically by the <em>callback</em> method. We see this behaviour all the time on news &amp; sports websites, where the updated event information is dynamically displayed on the page without the need to reload it.</p>
<p data-id="ba9a7ba7a2e8f978b14d37a2b3feba93">AJAX uses an <em>XMLHttpRequest</em> object for sending the requests to the server which is built-in the browser and uses JavaScript to update the <em>HTML DOM</em>.</p>
<p data-id="64d771ea896347dcf7902f1d0ec36ded">AJAX is commonly used with the <em>Jquery</em> framework to implement the asynchronous behaviour on the UI.</p>
<p data-id="0b2f7e8035f99c729b3e09109e01d72e">This dynamic technique of requesting information from the server after regular intervals is known as <em>Polling</em>.</p>
</div></div></div></div></div></div></div></div></div>