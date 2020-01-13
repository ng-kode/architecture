---
id: peer-to-peer-architecture-part-2-rmdymyo8lle
title: Peer to Peer Architecture – Part 2
sidebar_label: Peer to Peer Architecture – Part 2
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">This lesson contains the second part of the discussion on the Peer to Peer Architecture. We will be continuing where we left off in the previous lesson.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-peer-to-peer-architecture-how-does-it-work">What Is A Peer to Peer Architecture? How Does It Work?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#types-of-p2p-networks">Types Of P2P Networks</a></li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#unstructured-network">Unstructured Network</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#structured-network">Structured Network</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#hybrid-model">Hybrid Model</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"></div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-peer-to-peer-architecture-how-does-it-work" data-id="2ad492de8026188902f296506d263161">What Is A Peer to Peer Architecture? How Does It Work? <a class="markdownIt-Anchor" href="#what-is-a-peer-to-peer-architecture-how-does-it-work"><span class="anchor-link">#</span></a></h2>
<p data-id="536699e64e4e598846222316a0191b11">A <em>P2P Peer to Peer</em> architecture is designed around several <em>nodes</em> in the network taking part equally acting as both the <em>client</em> &amp; the <em>server</em>.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5872353407926272_image_6610234158088192.jpeg" alt=""></p>
<p data-id="7a4fe8d108066635339d42819830e5fa">The data is exchanged over <em>TCP IP</em> just like it happens over the <em>HTTP</em> protocol in a <em>client-server</em> model. The <em>P2P</em> design has an overlay network over <em>TCP IP</em> which enables the users to connect directly. It takes care of all the complexities and the heavy lifting. <em>Nodes/Peers</em> are indexed &amp; discoverable in this overlay network.</p>
<p data-id="be67d1648634befeb5c15678795fbf8e">A large file is transferred between the nodes by being divided into chunks of equal size in a non-sequential order.</p>
<p data-id="67bef666792a27bd190f4189ff0505b0">Say a system hosts a large file of 75 <em>Gigabytes</em>. Other <em>nodes</em> in the network, in need of the file, locate the system containing the file. Then they download the file in chunks, re-hosting the downloaded chunk simultaneously, making it more available to the other users. This approach is known as <em>Segmented P2P file transfer</em>.</p>
<p data-id="038dd7ae2a0f997d4e5cddee1c0bbbe6">Based on how these peers are linked with each other in the network, the networks are classified into a <em>Structured</em>, <em>Unstructured</em> or a <em>Hybrid</em> model.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="types-of-p2p-networks" data-id="eb4d053270d667840fbde4fa984498ac">Types Of P2P Networks <a class="markdownIt-Anchor" href="#types-of-p2p-networks"><span class="anchor-link">#</span></a></h2>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="unstructured-network" data-id="b7db34d3e0151a3a6ca62361221dd5b2">Unstructured Network <a class="markdownIt-Anchor" href="#unstructured-network"><span class="anchor-link">#</span></a></h3>
<p data-id="43bfa7f5c9a45aefd3247048abcb4c99">In an <em>unstructured</em> network <em>nodes/peers</em> keep connecting with each other randomly. So, there is no structure, no rule. Just simply connect &amp; grow the network.</p>
<p data-id="4cfbf8b7207d7808b416cb8bd6970a65">In this architectural design, there is no indexing of the nodes. To search the data, we have to scan through each &amp; every node of the network. This is <em>O(n)</em> in complexity where <em>n</em> is the number of nodes in the network. This is very <em>resource-intensive</em>.</p>
<p data-id="9f3ea8ea4d9e91fdf5300302880dbd9e">Think of it in this way. There are a billion systems connected in the network. And then there is a file stored in just one system in the network. In an <em>unstructured network</em>, we have to run a search through each system in the network to find the file.</p>
<p data-id="ae90a03fd93510a8c505d202696ebd33">So, if the search for a file in a system, say, needs 1 sec. The search through the entire network would require 1 billion seconds.</p>
<p data-id="9e012b3ef8c3e4b8b29a35d7e393fdb9">Some of the protocols of the unstructured network are <em>Gossip</em>, <em>Kazaa</em> &amp; <em>Gnutella</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="structured-network" data-id="276a1967a7b671e9f0da45b0d26d84aa">Structured Network <a class="markdownIt-Anchor" href="#structured-network"><span class="anchor-link">#</span></a></h3>
<p data-id="82ae874e209bd8b1ee62616c3a7ea617">In contrast to an <em>unstructured network</em>, a <em>structured P2P peer to peer network</em> holds proper indexing of the nodes or the topology which makes it easier to search for a specific data in it.</p>
<p data-id="edca1cfca380975115650d26cb1eb3a4">This kind of network implements a <em>Distributed hash table</em> to index the nodes. This index is just like an index of a book where we check to find a piece of particular information in the book rather than searching through every page of it.</p>
<p data-id="06c3019545f481f8989ddae5a687ef88"><em>BitTorrent</em> is an example of this type of network.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="hybrid-model" data-id="6d34b2cb94238fa41ad355a409f2073c">Hybrid Model <a class="markdownIt-Anchor" href="#hybrid-model"><span class="anchor-link">#</span></a></h3>
<p data-id="d1753adb6edad125822511f555547bf4">The majority of the blockchain startups have a <em>hybrid model</em>. A <em>hybrid model</em> means cherry-picking the good stuff from all the models like <em>P2P</em>, <em>client-server</em> etc. It is a network, involving both a <em>peer to peer</em> &amp; a <em>client-server</em> model.</p>
<p data-id="ebbae88bb3f5e5a47ef8ee8e9a0dcc03">As we know in a <em>p2p</em> network one single entity doesn’t have all the control. So to establish control we need to set up our own server. For that, we need a <em>client-server</em> model.</p>
<p data-id="d27ee2a3c403709e1ccd13eb04c61511">A <em>P2P network</em> offers more availability. To take down a blockchain network you have to literally take down all the nodes of the network across the globe. A <em>P2P</em> application can scale to the moon without putting the load on a single entity or the node. In an ideal environment, all the <em>nodes</em> in the network equally share the bandwidth &amp; the storage space; The system scales automatically as new users use the app.</p>
<p data-id="20bac2cd5f9c99531bbe5f4deb1a8868"><em>Nodes</em> get added, as more &amp; more people interact with your data. There are zero data storage and bandwidth costs, you don’t have to shell out money to buy third-party servers to store your data. No third-party intervention, data is secure. Share stuff only with friends you intend to share with.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="5e5f80bb6035f48c3eb5045523b71d72">The cult of the <em>decentralized web</em> is gaining ground in the present times. I can’t deny this that this is a disruptive tech with immense potential. <em>Blockchain</em>, <em>Cryptocurrency</em> is one example of this. It has taken the financial sector, in particular by storm.</p>
<p data-id="94e1c3e4183c1bf05762f409a163ef04">There are numerous <em>P2P</em> applications available on the web for instance –</p>
<ol data-id="1380f44b78d2fb791efcd4bdc00de902">
<li>
<p><em>Tradepal</em></p>
</li>
<li>
<p>Peer to Peer digital cryptocurrencies like <em>Bitcoin</em>, <em>Peercoin</em>.</p>
</li>
<li>
<p><em>GitTorrent</em> (a decentralized <em>GitHub</em> which uses <em>BitTorrent</em> and <em>Bitcoin</em>).</p>
</li>
<li>
<p><em>Twister</em> (a decentralized microblogging service, which uses <em>WebTorrent</em> for media attachments).</p>
</li>
<li>
<p><em>Diaspora</em> (a decentralized social network implementing the <em>federated architecture</em>).</p>
</li>
</ol>
<p data-id="879b1d7ee93bd188faef582c90b2fbd0"><em>Federated architecture</em> is an extension of the decentralized architecture, used in <em>decentralized social networks</em>, which I am going to discuss up next.</p>
</div></div></div></div></div></div></div></div></div>