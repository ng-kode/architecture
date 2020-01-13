---
id: graph-database-39m5gpqbj5q
title: Graph Database
sidebar_label: Graph Database
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will get to know about the Graph database and when to choose it for our projects</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-graph-database">What Is A Graph Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#features-of-a-graph-database">Features Of A Graph Database</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#when-do-i-pick-a-graph-database">When Do I Pick A Graph Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-life-implementations">Real Life Implementations</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-graph-database" data-id="85b1c9d1ec49aa243cab7d5c7560d6f9">What Is A Graph Database? <a class="markdownIt-Anchor" href="#what-is-a-graph-database"><span class="anchor-link">#</span></a></h2>
<p data-id="2b534d66d88d6f9126f73703dcd61d3d"><em>Graph</em> databases are also a part of the <em>NoSQL</em> database family. They store data in <em>nodes/vertices</em> and <em>edges</em> in the form of relationships.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5306872586305536_image_6563320641355776.jpeg" alt=""></p>
<p data-id="24292d355e0fe51f602b950a0343bf80">Each <em>Node</em> in a graph database represents an entity. It can be a person, a place, a business etc. And the <em>Edge</em> represents the relationship between the entities.</p>
<p data-id="e9367525d3c63970e09ac25f3fceb18b"><strong>But, why use a graph database to store relationships when we already have SQL based relational databases available?</strong></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="features-of-a-graph-database" data-id="f61de242740a9a04de6074dbe9fedb9a">Features Of A Graph Database <a class="markdownIt-Anchor" href="#features-of-a-graph-database"><span class="anchor-link">#</span></a></h2>
<p data-id="2b9211200b533a114b77dc12db4788e1">Hmmm… primarily, two reasons. The first is visualization. Think of that pinned board in the thriller detective movies where the pins are pinned on a board over several images connected via threads. It does help in visualizing how the entities are related &amp; how things fit together. Right?</p>
<p data-id="e3ee786dd9f9b375e356dd5ab1c94566">The second reason is the low latency. In graph databases, the relationships are stored a bit differently from how the relational databases store relationships.</p>
<p data-id="63f35ac7a16d66c743f102f7809db944">Graph databases are faster as the relationships in them are not calculated at the query time, as it happens with the help of <em>joins</em> in the relational databases. Rather the relationships here are persisted in the data store in the form of edges and we just have to fetch them. No need to run any sort of computation at the query time.</p>
<p data-id="088b6baaf812d64aa3fb6f5b0ad8bfe4">A good real-life example of an application which would fit a graph database is Google Maps. <em>Nodes</em> represent the cities and the <em>Edges</em> represent the connection between them.</p>
<p data-id="91299fb5925137eb3176941e4dacad53">Now, if I have to look for roads between different cities, I don’t need <em>joins</em> to figure out the relationship between the cities when I run the query. I just need to fetch the edges which are already stored in the database.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="when-do-i-pick-a-graph-database" data-id="4188c08b90471deb9793969f01c91e29">When Do I Pick A Graph Database? <a class="markdownIt-Anchor" href="#when-do-i-pick-a-graph-database"><span class="anchor-link">#</span></a></h2>
<p data-id="71b371dcce5ac769e7ed6fb689fbe60a">Ideal use cases of graph databases are building social, knowledge, network graphs. Writing AI-based apps, recommendation engines, fraud analysis app, storing genetic data etc.</p>
<p data-id="996fb701859e16d767c48c9e7ff0a252">Graph databases help us visualize our data with minimum latency. A popular graph database used in the industry is <em>Neo4J</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-life-implementations" data-id="4a3328dc5b6d054ca0d10e3f5b389a32">Real Life Implementations <a class="markdownIt-Anchor" href="#real-life-implementations"><span class="anchor-link">#</span></a></h2>
<p data-id="77df92bd4391617f1b976d429d0a4b4f"><em>Here are some of the real-life implementations of the tech listed below -</em></p>
<ul data-id="45f9d5b1b618dffc54cd62e067993a36">
<li>
<p><a href="https://neo4j.com/case-studies/walmart/" target="_blank">Walmart shows product recommendations to its customers in real-time using Neo4J graph database</a></p>
</li>
<li>
<p><a href="https://neo4j.com/blog/david-meza-chief-knowledge-architect-nasa/" target="_blank">NASA uses Neo4J to store “lessons learned” data from their previous missions to educate the scientists &amp; engineers.</a></p>
</li>
</ul>
</div></div></div></div></div></div></div></div></div>