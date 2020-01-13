---
id: document-oriented-database-bnkapnov2oo
title: Document Oriented Database
sidebar_label: Document Oriented Database
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will get to know about the Document Oriented database and when to choose it for our projects.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-document-oriented-database">What Is A Document Oriented Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#popular-document-oriented-databases">Popular Document Oriented Databases</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#when-do-i-pick-a-document-oriented-data-store-for-my-project">When Do I Pick A Document Oriented Data Store for My Project?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-life-implementations">Real Life Implementations</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-document-oriented-database" data-id="f273c9f8061f4d49cdcfd343f6f66953">What Is A Document Oriented Database? <a class="markdownIt-Anchor" href="#what-is-a-document-oriented-database"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="962f16315139b7834757f60ca936471d">
<p><em>Document Oriented databases</em> are the main types of <em>NoSQL</em> databases. They store data in a document-oriented model in independent documents. The data is generally <em>semi-structured</em> &amp; stored in a <em>JSON</em>-like format.</p>
</blockquote>
<p data-id="841f545d4ad49eee79bf6d0b917eec80">The data model is similar to the data model of our application code, so it’s easier to store and query data for developers.</p>
<p data-id="d1a636eee45d4a503956de29c8b54130">Document oriented stores are suitable for <em>Agile software development methodology</em> as it’s easier to change things with evolving demands when working with them.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="popular-document-oriented-databases" data-id="a39580505eda607e7aaae5ac7ac93bcb">Popular Document Oriented Databases <a class="markdownIt-Anchor" href="#popular-document-oriented-databases"><span class="anchor-link">#</span></a></h2>
<p data-id="8430ec709ca5e6c3e6519a5569ccd588">Some of the popular document-oriented stores used in the industry are <em>MongoDB, CouchDB, OrientDB, Google Cloud Datastore, Amazon Document DB</em></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="when-do-i-pick-a-document-oriented-data-store-for-my-project" data-id="e2e6be23489ff8b9c72637af2619c2a9">When Do I Pick A Document Oriented Data Store for My Project? <a class="markdownIt-Anchor" href="#when-do-i-pick-a-document-oriented-data-store-for-my-project"><span class="anchor-link">#</span></a></h2>
<p data-id="bc1375cfe7a9db90925158929f13be3f">If you are working with <em>semi-structured</em> data, need a flexible schema which would change often. You ain’t sure about the database schema when you start writing the app. There is a possibility that things might change over time. You are in need of something flexible which you could change over time with minimum fuss. Pick a <em>Document-Oriented</em> data store.</p>
<p data-id="393d766932a25a91feba932b79ffb1e6">Typical use cases of Document oriented databases are the following:</p>
<ul data-id="4ef9e0ec01be6f7b822a475519ac5438">
<li>Real-time feeds</li>
<li>Live sports apps</li>
<li>Writing product catalogues</li>
<li>Inventory management</li>
<li>Storing user comments</li>
<li>Web-based multiplayer games</li>
</ul>
<p data-id="1c1b879ec882974c4b6b0bf3b7945a8f">Being in the family of <em>NoSQL</em> databases these provide horizontal scalability, performant read-writes as they cater to <em>CRUD</em> - <em>Create Read Update Delete</em> use cases. Where there isn’t much relational logic involved &amp; all we need is just quick persistence &amp; retrieval of data.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-life-implementations" data-id="4a3328dc5b6d054ca0d10e3f5b389a32">Real Life Implementations <a class="markdownIt-Anchor" href="#real-life-implementations"><span class="anchor-link">#</span></a></h2>
<p data-id="8997f05fda4140677eadef25cfaaa82b"><em>Here are some of the good real-life implementations of the tech below -</em></p>
<ul data-id="84cf1ebf781177bd37d197200fe697de">
<li>
<p><a href="https://www.mongodb.com/blog/post/sega-hardlight-migrates-to-mongodb-atlas-simplify-ops-improve-experience-mobile-gamers" target="_blank">SEGA uses Mongo-DB to improve the experience for millions of mobile gamers</a></p>
</li>
<li>
<p><a href="https://www.mongodb.com/customers/coinbase" target="_blank">Coinbase scaled from 15k requests per min to 1.2 million requests per minute with MongoDB</a></p>
</li>
</ul>
</div></div></div></div></div></div></div></div></div>