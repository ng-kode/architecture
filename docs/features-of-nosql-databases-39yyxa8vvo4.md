---
id: features-of-nosql-databases-39yyxa8vvo4
title: Features Of NoSQL Databases
sidebar_label: Features Of NoSQL Databases
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss the features of NoSQL databases.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#pros-of-nosql-databases">Pros Of NoSQL Databases</a></li>
<li><a href="#gentle-learning-curve">Gentle Learning Curve</a></li>
<li><a href="#schemaless">Schemaless</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#cons-of-nosql-databases">Cons Of NoSQL Databases</a></li>
<li><a href="#inconsistency">Inconsistency</a></li>
<li><a href="#no-support-for-acid-transactions">No Support For ACID Transactions</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#conclusion">Conclusion</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#popular-nosql-databases">Popular NoSQL Databases</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="68cac332dea7a0f8c577b34052e1643b">In the introduction we learned that the <em>NoSQL</em> databases are built to run on clusters in a distributed environment, powering Web 2.0 websites.</p>
<p data-id="daef3a54b15559a7a4ee9342e9d3bdaa">Now, let’s go over some features of <em>NoSQL</em> databases.</p>
<h2 id="pros-of-nosql-databases" data-id="333f032c3056d0dc199cc11465ff601b">Pros Of NoSQL Databases <a class="markdownIt-Anchor" href="#pros-of-nosql-databases"><span class="anchor-link">#</span></a></h2>
<p data-id="35a80970edcd5c5fb213970c614d127b">Besides the design part, <em>NoSQL</em> databases are also developer-friendly. What do I mean by that?</p>
<h2 id="gentle-learning-curve" data-id="0d32d1174cf55a3cacc1338db0dc7152">Gentle Learning Curve <a class="markdownIt-Anchor" href="#gentle-learning-curve"><span class="anchor-link">#</span></a></h2>
<p data-id="c216ccfb26dd4bd7ac5fbb3c31908465">First, the learning curve is less than that of relational databases. When working with relational databases a big chunk of our time goes into learning how to design well-normalized tables, setting up relationships, trying to minimize joins and stuff.</p>
<h2 id="schemaless" data-id="1d4eaf979c1855ad32292ce4c56c3b90">Schemaless <a class="markdownIt-Anchor" href="#schemaless"><span class="anchor-link">#</span></a></h2>
<p data-id="7aa5455bb2d179f45d080de216af8887">One needs to be pretty focused when designing the schema of a relational database to avoid running into any issues in the future.</p>
<p data-id="946301f84bcf037d8ccb28d40f7f5c8a">Think of relational databases as a strict headmaster. Everything has to be in place, neat and tidy, things need to be consistent.
But <em>NoSQL</em> databases are a bit of chilled out &amp; relaxed.</p>
<p data-id="1a23b334bdcfba191381de7c7d310a65">There are no strict enforced schemas, work with the data as you want. You can always change stuff, spread things around. Entities have no relationships. Thus, things are flexible &amp; you can do stuff your way.</p>
<p data-id="a9fb2a7cc122391ce8c01aef9473e3f2"><em>Wonderful Right?</em></p>
<p data-id="401747e09ac091beef4d768f9938b799">Not always!! This flexibility is good and bad at the same time. Being so flexible, developer-friendly, having no joins and relationships etc. makes it good.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="cons-of-nosql-databases" data-id="a87c2c7c784ac3b9c7924ed7d8cc38dd">Cons Of NoSQL Databases <a class="markdownIt-Anchor" href="#cons-of-nosql-databases"><span class="anchor-link">#</span></a></h2>
<h2 id="inconsistency" data-id="70b10f12004b8c1f91274b1f17dc7c50">Inconsistency <a class="markdownIt-Anchor" href="#inconsistency"><span class="anchor-link">#</span></a></h2>
<p data-id="f9cda46d9e506fcc0a0a5a0051e4f026">But it introduces a risk of entities being inconsistent at the same time. Since an entity is spread throughout the database one has to update the new values of the entity at all places.</p>
<p data-id="11ee231fd65d54002dd2344cc9f3c70d">Failing to do so, makes the entity inconsistent.
This is not a problem with relational databases since they keep the data normalized. An entity resides at one place only.</p>
<h2 id="no-support-for-acid-transactions" data-id="19af19db9c8e1aa5f274a8e895ee726a">No Support For ACID Transactions <a class="markdownIt-Anchor" href="#no-support-for-acid-transactions"><span class="anchor-link">#</span></a></h2>
<p data-id="db6f053e82d4fdc3c24231f899fb3633">Also, <em>NoSQL</em> distributed databases don’t provide <em>ACID transactions</em>. A few that claim to do that, don’t support them globally. They are just limited to a certain entity hierarchy or a small region where they can lock down nodes to update them.</p>
<blockquote data-id="c0928f2ef250bb92557e9c3bc733c5c8">
<p><strong>Note:</strong> <em>Transactions in distributed systems come with terms and conditions applied.</em></p>
</blockquote>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="conclusion" data-id="7b60c55327cebd578968d1ed3b5dd77e">Conclusion <a class="markdownIt-Anchor" href="#conclusion"><span class="anchor-link">#</span></a></h2>
<p data-id="7a14be0ccbad92a3fece9255544a6984">My first experience with a <em>NoSQL</em> datastore was with the <em>Google Cloud Datastore</em>.</p>
<p data-id="5b8738f99e4d393c3ecdfc463e12771f">An upside I felt was that we don’t have to be a pro in database design to write an application.
Things were comparatively simpler, as there was no stress of managing joins, relationships, n+1 query issues etc.</p>
<p data-id="62bcbfa276d59d6b96a90f968f591584">Just fetch the data with its Key. You can also call it the id of the entity. This is a <em>constant O(1)</em> operation, which makes <em>NoSQL</em> Dbs really fast.</p>
<p data-id="4ae1e5b74f79d40740ee7c064fd45934">I have designed a lot of <em>MySQL</em> DB schemas in the past with complex relationships. And I would say working with a <em>NoSQL</em> database is a lot easier than working with relationships.</p>
<p data-id="7ed556ba06e85325dcf7ffb0c50b4833">It’s alright if we need to make a few extra calls to the backend to fetch data in separate calls that doesn’t make much of a difference. We can always cache the frequently accessed data to overcome that.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="popular-nosql-databases" data-id="6a6a2bb4d78207ae0e33840304281dcb">Popular NoSQL Databases <a class="markdownIt-Anchor" href="#popular-nosql-databases"><span class="anchor-link">#</span></a></h2>
<p data-id="e270058ca66342b3cb3ef0385188aca7">Some of the popular NoSQL databases used in the industry are <em>MongoDB</em>, <em>Redis</em>, <em>Neo4J</em>, <em>Cassandra</em>.</p>
<p data-id="f6763e4d51bed696bae4dc3b62f0834a">So, I guess, by now we have a pretty good idea of what NoSQL databases are. Let’s have a look at some of the use cases which fit best with them.</p>
</div></div></div></div></div></div></div></div></div>