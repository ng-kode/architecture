---
id: when-should-you-pick-a-relational-database-g7gwvml3de6
title: When Should You Pick A Relational Database?
sidebar_label: When Should You Pick A Relational Database?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss when to choose a relational database for our project.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#transactions-data-consistency">Transactions &amp; Data Consistency</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#large-community">Large Community</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#storing-relationships">Storing Relationships</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#popular-relational-databases">Popular Relational Databases</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="7ca91d91b0dfc459c12cc3414a755be6">If you are writing a stock trading, banking or a Finance-based app or you need to store a lot of relationships, for instance, when writing a social network like <em>Facebook</em>. Then you should pick a relational database. Here is why –</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="transactions-data-consistency" data-id="414e1d39ad39d8e7822c0876948e2357">Transactions &amp; Data Consistency <a class="markdownIt-Anchor" href="#transactions-data-consistency"><span class="anchor-link">#</span></a></h2>
<p data-id="f17bbf84d0d63942b756f0e704f579a0">If you are writing a software which has anything to do with money or numbers, that makes <em>transactions</em>, <em>ACID</em>, <em>data consistency</em> super important to you.</p>
<p data-id="975cb55d844ad476b17bc0abeb9a6d5a">Relational DBs shine when it comes to transactions &amp; data consistency. They comply with the ACID rule, have been around for ages &amp; are battle-tested.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="large-community" data-id="37f86ff87e0481d62302db19bd159f1f">Large Community <a class="markdownIt-Anchor" href="#large-community"><span class="anchor-link">#</span></a></h2>
<p data-id="4711e00026ef828a97f3d1810019b78a">Also, they have a larger community. Seasoned engineers on the tech are easily available, you don’t have to go too far looking for them.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="storing-relationships" data-id="15ed4cf210ead040eb7d3efa546c4eef">Storing Relationships <a class="markdownIt-Anchor" href="#storing-relationships"><span class="anchor-link">#</span></a></h2>
<p data-id="c83c65c56a8ac87ef5b1b1a94f82cdd0">If your data has a lot of relationships like which friends of yours live in a particular city? Which of your friend already ate at the restaurant you plan to visit today? etc. There is nothing better than a relational database for storing this kind of data.</p>
<p data-id="3032364474d39be1e9939833fc5fafde">Relational databases are built to store relationships. They have been tried &amp; tested &amp; are used by big guns in the industry like <a href="https://www.8bitmen.com/what-database-does-facebook-use-a-1000-feet-deep-dive/" target="_blank">Facebook as the main user-facing database.</a></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="popular-relational-databases" data-id="eff3d3cf8ff9f14baa5f91c32075ae89">Popular Relational Databases <a class="markdownIt-Anchor" href="#popular-relational-databases"><span class="anchor-link">#</span></a></h2>
<p data-id="dac4be96d0feb31781ac6978a8b40095">Some of the popular relational databases used in the industry are <em>MySQL</em> - it’s an open-source relationship database written in <em>C</em>, <em>C++</em> been around since 1995.</p>
<p data-id="5a4dc9dc0ee6e6b54eeea1ed1a4eac01">Others are <em>Microsoft SQL Server</em>, a proprietary RDBMS written by Microsoft in C, C++. <em>PostgreSQL</em> an open-source RDBMS written in C. <em>MariaDB</em>, <em>Amazon Aurora</em>, <em>Google Cloud SQL</em> etc.</p>
<p data-id="e4fc424be3552bb7b211da0dc666b1c2">Well, that’s all on the relational databases. Moving on to non-relational databases.</p>
</div></div></div></div></div></div></div></div></div>