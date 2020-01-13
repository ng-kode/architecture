---
id: primary-bottlenecks-that-hurt-the-scalability-of-our-application-yvb7azlkgdo
title: Primary Bottlenecks that Hurt the Scalability Of Our Application
sidebar_label: Primary Bottlenecks that Hurt the Scalability Of Our Application
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw"></p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#database">Database</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#application-architecture">Application Architecture</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#not-using-caching-in-the-application-wisely">Not Using Caching In the Application Wisely</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#inefficient-configuration-setup-of-load-balancers">Inefficient Configuration &amp; Setup of Load Balancers</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#adding-business-logic-to-the-database">Adding Business Logic to the Database</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#not-picking-the-right-database">Not Picking the Right Database</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#at-the-code-level">At the Code Level</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="b1d1b854e84f31ba55a77349cdee8252">There are several points in a web application which can become a bottleneck &amp; can hurt the scalability of our application. Let’s have a look at them.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="database" data-id="77b118cce6c1c03a436ac621c802ae98">Database <a class="markdownIt-Anchor" href="#database"><span class="anchor-link">#</span></a></h2>
<p data-id="b8848e1d851b4d8d07bfaa165086b82b">Consider that, we have an application that appears to be well architected. Everything looks good. The workload runs on multiple nodes &amp; has the ability to horizontally scale.</p>
<p data-id="1d65b6736c45e28dd7c75b62d4393e52">But the database is a poor single monolith, just one server been given the onus of handling the data requests from all the server nodes of the workload.</p>
<p data-id="4234401d49f18c6c791380e499f68a17">This scenario is a bottleneck. The server nodes work well, handle millions of requests at a point in time efficiently, still, the response time of these requests &amp; the latency of the application is very high due to the presence of a single database. There is only so much it can handle.</p>
<p data-id="afbf0d67d026f39d6777d45266aea1ea">Just like the workload scalability, the database needs to be scaled well.</p>
<p data-id="1a57c95850a579f8ce3b1dc0b19cf1fe">Make wise use of database partitioning, sharding, use multiple database servers to make the module efficient.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="application-architecture" data-id="5326f5db7b1a8699083ecb32560c18d8">Application Architecture <a class="markdownIt-Anchor" href="#application-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="e0b49fb8479902f9a22be8043889af10">A poorly designed application’s architecture can become a major bottleneck as a whole.</p>
<p data-id="f2b4a7477cd627b8b9238065a8325303"><em>A common architectural mistake is not using asynchronous processes &amp; modules where ever required rather all the processes are scheduled sequentially.</em></p>
<p data-id="287da499daa6a5c618dbba80dfcf8bba">For instance, if a user uploads a document on the portal, tasks such as sending a confirmation email to the user, sending a notification to all of the subscribers/listeners to the upload event should be done asynchronously.</p>
<p data-id="3cb2b07c6f71baa6f71281747488a97f">These tasks should be forwarded to a messaging server as opposed to doing it all sequentially &amp; making the user wait for everything.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="not-using-caching-in-the-application-wisely" data-id="18eef3706b2ff5ba917e1b81f7cf70fd">Not Using Caching In the Application Wisely <a class="markdownIt-Anchor" href="#not-using-caching-in-the-application-wisely"><span class="anchor-link">#</span></a></h2>
<p data-id="da185249a451a6972f4930e1e72f2df7">Caching can be deployed at several layers of the application &amp; it speeds up the response time by notches. It intercepts all the requests going to the database, reducing the overall load on it.</p>
<p data-id="ce333bc0644b1c348999f07e214dfb01">Use caching exhaustively throughout the application to speed up things significantly.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="inefficient-configuration-setup-of-load-balancers" data-id="c319027e80273641abdb0138f1d4d0ad">Inefficient Configuration &amp; Setup of Load Balancers <a class="markdownIt-Anchor" href="#inefficient-configuration-setup-of-load-balancers"><span class="anchor-link">#</span></a></h2>
<p data-id="0449ef14cea6d797a862032a78bdfe10">Load balancers are the gateway to our application. Using too many or too few of them impacts the latency of our application.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="adding-business-logic-to-the-database" data-id="4bba8ee497c35b96cc144840bebe0702">Adding Business Logic to the Database <a class="markdownIt-Anchor" href="#adding-business-logic-to-the-database"><span class="anchor-link">#</span></a></h2>
<p data-id="9da060da009c118bd61c98fb6fbe286b">No matter what justification anyone provides, I’ve never been a fan of adding business logic to the database.</p>
<p data-id="0ffd0756a309e4ed4d8f31cf5ad7cee4">The database is just not the place to put business logic. Not only it makes the whole application tightly coupled. It puts unnecessary load on it.</p>
<p data-id="31a4bb16624e916921da238a61e858ae">Imagine when migrating to a different database, how much code refactoring it would require.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="not-picking-the-right-database" data-id="b8c2705138ae7a3b48d85092b43205f6">Not Picking the Right Database <a class="markdownIt-Anchor" href="#not-picking-the-right-database"><span class="anchor-link">#</span></a></h2>
<p data-id="5ed5eedea42e6ca723999c5e5e1479b0">Picking the right database technology is vital for businesses. Need transactions &amp; strong consistency? Pick a <em>Relational Database</em>. If you can do without strong consistency rather need horizontal scalability on the fly pick a <em>NoSQL</em> database.</p>
<p data-id="f9f1c485432fa13868e349eb5f073b5b">Trying to pull off things with a not so suitable tech always has a profound impact on the latency of the entire application in negative ways.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="at-the-code-level" data-id="3c9f65ec96da32461c99c22aa58f1abc">At the Code Level <a class="markdownIt-Anchor" href="#at-the-code-level"><span class="anchor-link">#</span></a></h2>
<p data-id="5cd5a66ba4020e0f3968e03b9fb29754">This shouldn’t come as a surprise but inefficient &amp; badly written code has the potential to take down the entire service in production, which includes:</p>
<ul data-id="c71005a1816eb99c9a853fcd5d4fa11d">
<li>Using unnecessary loops, nested loops.</li>
<li>Writing tightly coupled code.</li>
<li>Not paying attention to the <em>Big-O complexity</em> while writing the code. Be ready to do a lot of firefighting in production.</li>
</ul>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="ca096af3f891b20662af5b0dff44d376">In this lesson, if a few of the things are not clear to you such as Strong consistency, how message queue provides an asynchronous behaviour, how to pick the right database. I’ll discuss all that in the upcoming lessons, stay tuned.</p>
</div></div></div></div></div></div></div></div></div>