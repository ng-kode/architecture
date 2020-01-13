---
id: peer-to-peer-architecture-part-1-rlapnkxy84r
title: Peer to Peer Architecture – Part 1
sidebar_label: Peer to Peer Architecture – Part 1
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, which is part one of the discussion on Peer to Peer Architecture, we will take a deep dive into the architecture &amp; discuss it in detail.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-peer-to-peer-p2p-network">What Is A Peer to Peer (P2P) Network?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-does-a-central-server-mean">What Does A Central Server Mean?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#downsides-of-centralized-systems">Downsides Of Centralized Systems</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-is-a-decentralized-architecture">What Is A Decentralized Architecture?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#advantages-of-a-peer-to-peer-network">Advantages Of A Peer to Peer Network</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="ef114919cb9a39b86cdf2cb7c26c9a13"><em>P2P</em> architecture is the base of <em>blockchain</em> tech. We’ve all used it at some point in our lives to download files via <em>torrent</em>. So, I guess you have a little idea of what it is. You are probably aware of the terms like <em>Seeding</em>, <em>Leeching</em> etc. Even if you aren’t, you’ll learn everything in this lesson.</p>
<p data-id="84fff210a030f2c7e7f160de49d199b4">Let’s begin the lesson with having an understanding of what a <em>P2P</em> network is?</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-peer-to-peer-p2p-network" data-id="eff777284ed8b42b4cd5cc2fe2777346">What Is A Peer to Peer (P2P) Network? <a class="markdownIt-Anchor" href="#what-is-a-peer-to-peer-p2p-network"><span class="anchor-link">#</span></a></h2>
<p data-id="9ec8be8426b378ebbc0cc53864afefa4">A <em>P2P</em> network is a network in which computers also known as <em>nodes</em> can communicate with each other without the need of a <em>central server</em>.
The absence of a <em>central server</em> rules out the possibility of a single point of failure. All the computers in the network have equal rights. A <em>node</em> acts as a <em>seeder</em> and a <em>leecher</em> at the same time. So, even if some of the computers/nodes go down, the network &amp; the communication is still up.</p>
<p data-id="b3569c870832f891cfc6e45904a432f9">A <em>Seeder</em> is a <em>node</em> which hosts the data on its system and provides bandwidth to upload the data to the network, a <em>Leecher</em> is a node which downloads the data from the network.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/courses_web-application-software-architecture-101_assets_api_collection_6064040858091520_6411938009448448_page_5378781134979072_image_5252606806982656.jpeg.jpeg" alt=""></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-does-a-central-server-mean" data-id="57217132f468696ac02ea26642b6330f">What Does A Central Server Mean? <a class="markdownIt-Anchor" href="#what-does-a-central-server-mean"><span class="anchor-link">#</span></a></h2>
<p data-id="246fd493bd6372b83ead40b412c64366">I want you to think of a messaging app. When two users communicate, the first user sends a message from his device, the message moves on the server of the organization hosting the messaging service, from there the message is routed to the destination, that is, the device of the user receiving the message.</p>
<p data-id="666aa3ad64448043533f1b14cf3a308f">The server of the organization is the <em>central server</em>. These systems are also known as <em>Centralized systems</em>.</p>
<p data-id="21d917ceaa2bb2197c6d53f2de4a6f06"><em>Okay, so what’s the issue when communicating with my friend via a central server? I have never faced any issues.</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="downsides-of-centralized-systems" data-id="c2c03abc3622744e34b40c10dff9aeb2">Downsides Of Centralized Systems <a class="markdownIt-Anchor" href="#downsides-of-centralized-systems"><span class="anchor-link">#</span></a></h2>
<p data-id="991d6f6deef9b9d5f0d896d47d688c7e">In this scenario, there are a few important things to consider -</p>
<ul data-id="43846c8012d5da668f4b12ea12af4ac6">
<li>
<p>First, the <em>central server</em> has access to all your messages. It can read it, share it with its associates, laugh about it and so on. So, communication is not really secure. Even though the businesses say that the entire message pipeline is encrypted and stuff. But still, data breaches happen, governments get access to our data. Data is sold to third parties for fat profits. Do you think these messaging apps are really secure? Should the national security, enterprise officials sitting at the top of the food chain use these central server messaging apps for communication?</p>
</li>
<li>
<p>Second, in case of events like a natural disaster, like an earthquake, a zombie attack on the data centre, a massive infrastructural failure or the organization going out of business. We are stranded, there is no way to communicate with our friends across the globe. Think about it.</p>
</li>
<li>
<p>Third, let’s say you start creating content on social media, you have a pretty solid following on it, you spend 100+ hours a week to put out the best content ever and have worked years to reach this point of success. But then one fine day, out of the blue, the organization pokes you and says. Hey!! Good job, but, aaaaa… for some reason, which we can’t talk about, we have to let your data go. We just don’t like your content. <em>Shift + Del</em> and whoosh… all your data disappears like a Genie. <em>What are you gonna do next?</em> If you are already a content creator or is active on social media, this happens all the time, you know that.</p>
</li>
</ul>
<p data-id="677923c1f8d3f821d1322891bb71e101">Fortunately, P2P networks are resilient to all these scenarios, due to their design. They have a <em>Decentralized architecture</em>.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/courses_web-application-software-architecture-101_assets_api_collection_6064040858091520_6411938009448448_page_5378781134979072_image_6615945793503232.jpeg.jpeg" alt=""></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-decentralized-architecture" data-id="a3ef248ca2c5498a20b7af36c7d3daff">What Is A Decentralized Architecture? <a class="markdownIt-Anchor" href="#what-is-a-decentralized-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="2b29957a91d0a85264640ba8b88d0852">Nobody has control over your data, nobody has the power to delete your data as all the participating nodes in a <em>P2P</em> network have equal rights. During a zombie apocalypse when the huge corporation servers would be dead or on fire, we can still communicate with each other via a <em>peer to peer</em> connection.</p>
<p data-id="75d081b5ab7f1e372a44c853fb7e00cd">Though I’ve nothing against any of the corporations :) They’ve made our lives really easy. It’s just I am making you aware of all the possible scenarios out there.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="advantages-of-a-peer-to-peer-network" data-id="6c0a18d5397c05d9833faedbf46a4128">Advantages Of A Peer to Peer Network <a class="markdownIt-Anchor" href="#advantages-of-a-peer-to-peer-network"><span class="anchor-link">#</span></a></h2>
<p data-id="55dd86dd2fbb3b3e394e32ce54e84be2"><em>Here is another use case where a peer to peer network rocks!!</em></p>
<p data-id="fa00684ddf33189638b34b5f572932bc">Imagine this, you have finally returned home from a trekking tour. Having visited all the seven continents around the world, it couldn’t be more beautiful &amp; emotionally satisfying.</p>
<p data-id="7d9373a5fe9012e5b0f1c803888e14ec">You have documented the entire expedition with state-of-the-art cameras &amp; equipment in super ultra HD 4K quality, which has stacked up the hard drive of your computer. You are super excited to share all the videos &amp; photos, of the tour, with your friends.</p>
<p data-id="c7cca118d95c91e3ff56570b27a61751"><em>But how do you really plan to share the data, which is in several gigabytes, with your friends?</em></p>
<p data-id="f8d1b0939fa332d82ac3c7bd9f284501">Facebook messenger, Whatsapp?</p>
<p data-id="e0467651fd60051ac3af400a905d70e8">Messengers have a memory limit, so they aren’t even an option. Well, you could upload all the stuff on the cloud &amp; share the link with your folks, but, hold on, uploading that much amount of data needs some serious storage space &amp; that would mean some serious money. Would you be in the mood of spending anymore after such a long trip?</p>
<p data-id="49d7081ed0035217ff594929cbb372fe">No problemo, we can write all the files on a physical memory like a DVD or a portable hard drive &amp; share with our friends, Right?</p>
<p data-id="74530e433fe6db7385bd9c94ca1d1535">Well yes, we can but physical memory has its costs &amp; writing files to it for every friend is time-consuming, expensive &amp; resource-intensive. And I get it you are tired already. Oh!! &amp; by the way, we have to courier the disks to friends located across the globe. Do add additional courier expense &amp; of course the time it will take to reach them.</p>
<p data-id="4ad7fad618421c4e75280acf3f5987fa">We’ve got this, don’t you worry!! We’ll surely find out some way.
Okay… Alright. So, now what options do we have, remaining? Think about it.</p>
<p data-id="a7bccbb4f413eda8e680972505eab987">Hey!! Why don’t we use <em>peer to peer</em> file sharing? That would be awesome.</p>
<p data-id="ad9f54a52e04526542cc5a4174284302">With <em>P2P Peer to peer</em> file sharing, we can easily share all the content with your friends with a minimum, almost no costs &amp; fuss.</p>
<p data-id="6fc98b1b29bdbc8bea4ecd073887722a">Beautiful!!</p>
<p data-id="876ddf0eb8f782eb1891f80c4fa4dee0">We can use a <em>P2P</em> protocol like <em>BitTorrent</em> for it. It’s the most commonly used <em>P2P peer to peer</em> protocol to distribute data and large electronic files over the internet. It has approx. 25 million concurrent users at any point in time.</p>
<p data-id="f5908ef08ec4a5cc5747755e4c578a9f">So, we will create a <em>torrent</em> file of our data, share it with all our folks. They have to just put the <em>torrent</em> in their BitTorrent client &amp; start downloading the files to their systems while hosting/seeding the files simultaneously for others to download.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="cbe1a99e184af109c7740827bdd75dd6">Okay!! So, these are a few of the use cases, we discussed, where <em>P2P</em> network rocks. In the next lesson which is part 2 of the <em>P2P</em> architecture, we will take a deep dive into the architecture of it.</p>
</div></div></div></div></div></div></div></div></div>