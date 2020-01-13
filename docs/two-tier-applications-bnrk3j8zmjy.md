---
id: two-tier-applications-bnrk3j8zmjy
title: Two Tier Applications
sidebar_label: Two Tier Applications
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the Two Tier applications.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#two-tier-application">Two Tier Application</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#the-need-for-two-tier-application">The Need For Two Tier Application</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="two-tier-application" data-id="6d1356b99250c9c8a1c2324a1589870f">Two Tier Application <a class="markdownIt-Anchor" href="#two-tier-application"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="900e9a36e37d3f41383897a80df90e94">
<p>A <strong>Two-tier</strong> application involves a <em>client</em> and a <em>server</em>. The <em>client</em> would contain the <em>user interface</em> &amp; the <em>business logic</em> in one machine. And the backend <em>server</em> would be the <em>database</em> running on a different machine. The database server is hosted by the business &amp; has control over it.</p>
</blockquote>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5026968460328960_image_6299357118726144.jpeg" alt=""></p>
<p data-id="e171cfed559bcb64361c62646a99236e"><em>Why the need for two-tier applications? Why not host the business logic on a different machine &amp; have control over it?</em></p>
<p data-id="5b9b6ef19e531e5b5e71253d4df31361"><em>Also, again isn’t the application code vulnerable to being accessed by a third person?</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="the-need-for-two-tier-application" data-id="09fec60734fe8d6bd44b6b5bafe010ef">The Need For Two Tier Application <a class="markdownIt-Anchor" href="#the-need-for-two-tier-application"><span class="anchor-link">#</span></a></h2>
<p data-id="c567a52142d46220b9406fb3e710f855">Well, yes!! But there are use cases where <em>two-tier</em> applications come in handy, for instance, a to-do list app or a similar planner or a productivity app.</p>
<p data-id="d02ef7596359c1ec3982f01e3981489b">In these scenarios, it won’t cause the business significant harm, even if the code is accessed by a third person. On the contrary, the upside is since the code &amp; the user interface reside in the same machine, there are fewer network calls to the backend server which keeps the latency of the application low.</p>
<p data-id="d2eab5120260df1974d38a8d5f54a611">The application makes a call to the <em>database</em> server, only when the user has finished creating his to-do list &amp; wants to persist the changes.</p>
<p data-id="07278ba5d026570c55ed55cff1821836">Another good example of this is the online browser &amp; app-based games. The game files are pretty heavy, they get downloaded on the client just once when the user uses the application for the first time. Moreover, they make the network calls only to keep the game state persistent.</p>
<p data-id="4b7da04de6b55abf8b07d96a00ab840c">Also, fewer server calls mean less money to be spent on the servers which is naturally economical.</p>
<p data-id="e893115302d080699351c438be826df2">Though, it largely depends on our business requirements &amp; the use case if we want to pick this type of tier when writing our service.</p>
<p data-id="2004b7408c902ef961133f5e0d661297">We can either keep the <em>user interface</em> and the <em>business logic</em> on the <em>client</em> or move the <em>business logic</em> to a dedicated <em>backend server</em>, which would make it a <em>three-tier</em> application. Which I am going to discuss up next.</p>
</div></div></div></div></div></div></div></div></div>