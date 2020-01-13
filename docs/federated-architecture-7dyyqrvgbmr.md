---
id: federated-architecture-7dyyqrvgbmr
title: Federated Architecture
sidebar_label: Federated Architecture
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will have an insight into the Federated Architecture.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-federated-architecture">What Is A Federated Architecture?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#how-is-federated-architecture-implemented-in-decentralized-social-networks">How Is Federated Architecture Implemented In Decentralized Social Networks?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-is-the-need-for-pods">What Is the Need For Pods?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"></div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-federated-architecture" data-id="b45c761443ab2acfcdc31558158cfab8">What Is A Federated Architecture? <a class="markdownIt-Anchor" href="#what-is-a-federated-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="19ff6043af0023a776060b592d50850b"><em>Federated architecture</em> is an extension to the <em>decentralized architecture</em>. It powers social networks like <em>Mastodon</em>, <em>Minds</em>, <em>Diaspora</em> etc.</p>
<p data-id="196eb45d9fb0c1317c31574a5dc11b97">The term <em>federated</em> in a general sense means a group of semi-autonomous entities exchanging information with each other. A real-world example of this would be looking at different states of a country which are managed by the state governments. They are partially self-governing &amp; exercise power to keep things running smoothly.
And then, those states governments share information with each other &amp; with a central government making a complete autonomous government.</p>
<p data-id="339ffa5f1c7a3cd70053f9723af6ee24">This is just an example. The federated model from a technical standpoint is under continual research, development &amp; evolution. There are no standard rules. Developers, architects can have their own designs in place. After all, it’s all <em>decentralized</em>. Not under the control of any single entity.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="how-is-federated-architecture-implemented-in-decentralized-social-networks" data-id="0197ad00e1f4e8037a3e422f217cb12d">How Is Federated Architecture Implemented In Decentralized Social Networks? <a class="markdownIt-Anchor" href="#how-is-federated-architecture-implemented-in-decentralized-social-networks"><span class="anchor-link">#</span></a></h2>
<p data-id="a4176c054f32e8977899b6610633b2d3">As shown in the diagram below. A federated network has entities called <em>servers</em> or <em>pods</em>. A large number of <em>nodes</em> subscribe to the <em>pods</em>. There are several <em>pods</em> in the network that are linked to each other &amp; share information with each other.</p>
<p data-id="21d3bb948ecfb0dd2922bfdbfd046b60">The <em>pods</em> can be hosted by individuals as it is ideally achieved in a decentralized network. As new <em>pods</em> are hosted &amp; introduced to the network, the network keeps growing.</p>
<p data-id="9e4bbc229a8153a2fd451eafff0c0600">In case if the link between a few <em>pods</em> breaks temporarily. The network is still up. <em>Nodes</em> can still communicate with each other via the pods they are subscribed to.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_6411285098921984_image_6206962263916544.jpeg" alt=""></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-the-need-for-pods" data-id="c5014e31e167e8242c9edb9a94f25ccb">What Is the Need For Pods? <a class="markdownIt-Anchor" href="#what-is-the-need-for-pods"><span class="anchor-link">#</span></a></h2>
<p data-id="c0e37962e0f075a005434501ffaaa4e8"><em>What is the need for Pods? Can’t just the nodes be linked to each other like in a regular peer to peer network?</em></p>
<p data-id="640d89009c7705aa87190a5d58e668fd"><em>Pods</em> facilitate node discovery. In a <em>peer to peer</em> network, there is no way of discovering other nodes &amp; we would just sit in the dark if it weren’t for a centralized node registry or something.</p>
<p data-id="48b8b56639bd197f2f8c26bd2a3f4c73">The other way is to run a scan through the network &amp; try to discover other nodes. That’s a really time-consuming &amp; a tedious task. Why not just have a <em>pod</em> instead.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="97ee34b4f5bc7c511a572e13d972b5b1">Okay!! So, Guys, I think I have given you a pretty good insight into the decentralized web.</p>
<p data-id="80778208b56c73267a264859e3551c48">Let’s move on to the next lesson where we talk about picking the right server-side technology.</p>
</div></div></div></div></div></div></div></div></div>