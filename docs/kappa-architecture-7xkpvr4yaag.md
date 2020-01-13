---
id: kappa-architecture-7xkpvr4yaag
title: Kappa Architecture
sidebar_label: Kappa Architecture
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss the Kappa Architecture of data processing</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-kappa-architecture">What Is Kappa Architecture?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#layers-of-kappa-architecture">Layers Of Kappa Architecture</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-kappa-architecture" data-id="05c1b72fd318fa3f6c4f579c9b2812ee">What Is Kappa Architecture? <a class="markdownIt-Anchor" href="#what-is-kappa-architecture"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="744325457ccd5821d776ba5544b92e12">
<p>In Kappa architecture, all the data flows through a single data streaming pipeline as opposed to the Lambda architecture which has different data streaming layers that converge into one.</p>
</blockquote>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4736273858166784_image_5259002013286400.jpeg" alt=""></p>
<p data-id="dc16e085aefd50f1e321c56100deb63d">The architecture flows the data of both <em>real-time</em> &amp; <em>batch processing</em> through a single streaming pipeline reducing the complexity of not having to manage separate layers for processing data.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="layers-of-kappa-architecture" data-id="e75a7cdcd9c6234b0d2db5ed552d4a05">Layers Of Kappa Architecture <a class="markdownIt-Anchor" href="#layers-of-kappa-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="f3e3051a97973c12ceea97070e72af58"><em>Kappa</em> contains only two layers. <em>Speed</em>, which is the streaming processing layer, &amp; the <em>Serving</em> which is the final layer.</p>
<p data-id="ee20d144e7667f11ccf143ce7c717e89"><em>Kappa is not an alternative for Lambda</em>. Both the architectures have their use cases.</p>
<p data-id="6f8acbc750836b36d9543d1c3e0299fe"><em>Kappa</em> is preferred if the batch and the streaming analytics results are fairly identical in a system. <em>Lambda</em> is preferred if they are not.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="a02615dcd0aabbf07c7461daf8e54d37">Well, this concludes the stream processing chapter. Though the entire distributed data processing approach appears pretty smooth and efficient it’s important that we do not forget that setting up and managing a distributed data processing system is something not trivial. It’ requires years of work in perfecting the system. Also, a distributed system does not promise <em>Strong Consistency</em> of data.</p>
<p data-id="579ad99f2f8dfccbfb596594aded2b2a">With this being said, let’s move on to the next chapter where I talk about different kinds of architectures involved in the domain of software development.</p>
</div></div></div></div></div></div></div></div></div>