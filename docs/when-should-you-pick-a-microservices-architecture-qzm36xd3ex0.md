---
id: when-should-you-pick-a-microservices-architecture-qzm36xd3ex0
title: When Should You Pick A Microservices Architecture?
sidebar_label: When Should You Pick A Microservices Architecture?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn about the pros and cons of the Microservice Architecture &amp; when should we pick it for our project.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#pros-of-microservice-architecture">Pros of Microservice Architecture</a>
<ul>
<li><a href="#no-single-points-of-failure">No Single Points Of Failure</a></li>
<li><a href="#leverage-the-heterogeneous-technologies">Leverage the Heterogeneous Technologies</a></li>
<li><a href="#independent-continuous-deployments">Independent &amp; Continuous Deployments</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li><a href="#cons-of-microservices-architecture">Cons Of Microservices Architecture</a>
<ul>
<li><a href="#complexities-in-management">Complexities In Management</a></li>
<li><a href="#no-strong-consistency">No Strong Consistency</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li><a href="#when-should-you-pick-a-microservices-architecture">When Should You Pick A Microservices Architecture?</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="pros-of-microservice-architecture" data-id="8d21012158d22d1b54c8f5cef39fa10b">Pros of Microservice Architecture <a class="markdownIt-Anchor" href="#pros-of-microservice-architecture"><span class="anchor-link">#</span></a></h2>
<h3 id="no-single-points-of-failure" data-id="1fee2a0b61d145ee08dcc9e75bf23089">No Single Points Of Failure <a class="markdownIt-Anchor" href="#no-single-points-of-failure"><span class="anchor-link">#</span></a></h3>
<p data-id="2d34ba6fc3e2269501d1c119a7d61b84">Since microservices is a loosely coupled architecture, there is no single point of failure. Even if a few of the services go down, the application as a whole is still up.</p>
<h3 id="leverage-the-heterogeneous-technologies" data-id="f320401a673106a62ba9ce9b96a25fcc">Leverage the Heterogeneous Technologies <a class="markdownIt-Anchor" href="#leverage-the-heterogeneous-technologies"><span class="anchor-link">#</span></a></h3>
<p data-id="091fdd8217100fb8acdd39c2d870f0e7">Every component interacts with each other via a <em>REST API Gateway interface</em>. The components can leverage the polyglot persistence architecture &amp; other heterogeneous technologies together like <em>Java</em>, <em>Python</em>, <em>Ruby</em>, <em>NodeJS</em> etc.</p>
<p data-id="f9f80c3cce5a6e7901e433f9105a0293"><em>Polyglot persistence</em> is using multiple databases types like <em>SQL</em>, <em>NoSQL</em> together in an architecture. I’ll discuss it in detail in the database lesson.</p>
<h3 id="independent-continuous-deployments" data-id="46ae166afb1cd39060f82e2aee8c318a">Independent &amp; Continuous Deployments <a class="markdownIt-Anchor" href="#independent-continuous-deployments"><span class="anchor-link">#</span></a></h3>
<p data-id="5dcf29c414f4f8182734f658f4d5c198">The deployments can be independent and continuous.
We can have dedicated teams for every microservice, it can be scaled independently without impacting other services.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="cons-of-microservices-architecture" data-id="8b0bdd78bc81c1d52120d0a5727d4970">Cons Of Microservices Architecture <a class="markdownIt-Anchor" href="#cons-of-microservices-architecture"><span class="anchor-link">#</span></a></h2>
<h3 id="complexities-in-management" data-id="ffdabe0de8162988ab6f633c38e61447">Complexities In Management <a class="markdownIt-Anchor" href="#complexities-in-management"><span class="anchor-link">#</span></a></h3>
<p data-id="26dff3cca9e884e65595e4ca53517453">Microservices is a distributed environment, where there are so many nodes running together. Managing &amp; monitoring them gets complex.</p>
<p data-id="6d5303ba7f0386ef18440020866e658d">We need to setup additional components to manage microservices such as a node manager like <em>Apache Zookeeper</em>, a <em>distributed tracing</em> service for monitoring the nodes etc.</p>
<p data-id="0d1c4dfbc0ff03fc91f8c0b07c7c19f0">We need more skilled resources, maybe a dedicated team to manage these services.</p>
<h3 id="no-strong-consistency" data-id="234bc0138109951360c83288651541c9">No Strong Consistency <a class="markdownIt-Anchor" href="#no-strong-consistency"><span class="anchor-link">#</span></a></h3>
<p data-id="5acfdb19306124af507f9f028197421e"><em>Strong consistency</em> is hard to guarantee in a distributed environment. Things are <em>Eventually consistent</em> across the nodes. And this limitation is due to the distributed design.</p>
<p data-id="6c6695cffa6712d841d4c5f822d59ba0">I’ll discuss both Strong and eventual consistency in the database chapter.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="when-should-you-pick-a-microservices-architecture" data-id="d0ac178f827a57799bb120dcaac1dec9">When Should You Pick A Microservices Architecture? <a class="markdownIt-Anchor" href="#when-should-you-pick-a-microservices-architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="5caeb766485fb29031dd0792f4196385">The microservice architecture fits best for complex use cases and for apps which expect traffic to increase exponentially in future like a fancy social network application.</p>
<p data-id="0d345877733881646d81559b2a30551e">A typical social networking application has various components such as messaging, real-time chat, LIVE video streaming, image uploads, Like, Share feature etc.</p>
<p data-id="0250afee90b65ce081e741a228e90c71">In this scenario, I would suggest developing each component separately keeping the <em>Single Responsibility</em> and the <em>Separation of Concerns</em> principle in mind.</p>
<p data-id="3c3d86147c8dc0b0c0d20aa646ab5167">Writing every feature in a single codebase would take no time in becoming a mess.</p>
<p data-id="049f96424be8fea8ef40c443c9e79386">So, by now, in the context of monolithic and microservices, we have gone through three approaches:</p>
<ol data-id="7ee4ef89bb0057acb3f1d805e41bbdd9">
<li>Picking a monolithic architecture</li>
<li>Picking a microservice architecture</li>
<li>Starting with a monolithic architecture and then later scale out into a microservice architecture.</li>
</ol>
<p data-id="2bfb6d32312c53d6585a222fc5ed22ac">Picking a monolithic or a microservice architecture largely depends on our use case.</p>
<p data-id="08b923d981b2e1b64b42f9f42e4681f0">I’ll suggest, keep things simple, have a thorough understanding of the requirements. Get the lay of the land, build something only when you need it &amp; keep evolving the code iteratively. This is the right way to go.</p>
</div></div></div></div></div></div></div></div></div>