---
id: what-is-a-rest-api-qadazx6yorr
title: What Is A REST API?
sidebar_label: What Is A REST API?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson we will have an insight into the REST API</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-rest">WHAT IS REST?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#rest-api">REST API</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#rest-endpoint">REST Endpoint</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#decoupling-clients-the-backend-service">Decoupling Clients &amp; the Backend Service</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#application-development-before-the-rest-api">Application Development Before the REST API</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#api-gateway">API Gateway</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-rest" data-id="d1635ff32672ad702e6706eee97a97be">WHAT IS REST? <a class="markdownIt-Anchor" href="#what-is-rest"><span class="anchor-link">#</span></a></h2>
<blockquote data-id="025fafb81cb78f2f10b63bf70332a3f0">
<p>REST stands for Representational State Transfer. It’s a software architectural style for implementing web services. Web services implemented using the REST architectural style are known as the RESTful Web services.</p>
</blockquote>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="rest-api" data-id="96e09e9d3cc41d1772145309a6d4c168">REST API <a class="markdownIt-Anchor" href="#rest-api"><span class="anchor-link">#</span></a></h2>
<p data-id="a0c832ed57a3ab13a1af3a6a195916cb">A <em>REST API</em> is an <em>API</em> implementation that adheres to the REST architectural constraints. It acts as an interface. The communication between the client &amp; the server happens over <em>HTTP</em>. A <em>REST API</em> takes advantage of the <em>HTTP</em> methodologies to establish communication between the client and the server. <em>REST</em> also enables servers to cache the response that improves the performance of the application.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/courses_web-application-software-architecture-101_assets_api_collection_6064040858091520_6411938009448448_page_6353247012913152_image_6125166331428864.jpeg" alt=""></p>
<p data-id="372a9e62afcb2773969703e80b7831a9">The communication between the client and the server is a stateless process. And by that, I mean every communication between the client and the server is like a new one.</p>
<p data-id="02baf08fa7a5bfa3b11853e535f57e4c">There is no information or memory carried over from the previous communications. So, every time a client interacts with the backend, it has to send the authentication information to it as well. This enables the backend to figure out that the client is authorized to access the data or not.</p>
<p data-id="b7284236d4f389ab366fedbc07abd4e9"><em>With the implementation of a <em>REST API</em> the client gets the backend endpoints to communicate with. This entirely decouples the backend &amp; the client code.</em></p>
<p data-id="c98cea333a14a96fddd08ed956080ee4"><strong>Let’s understand what this means.</strong></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="rest-endpoint" data-id="e21d85f847384353de9024d48e91b0ee">REST Endpoint <a class="markdownIt-Anchor" href="#rest-endpoint"><span class="anchor-link">#</span></a></h2>
<p data-id="9902408b60c22d2d532210322f4c9f7d">An <em>API/REST/Backend</em> endpoint means the <em>url</em> of a service. For example, <code>https://myservice.com/getuserdetails/{username}</code> is a backend endpoint for fetching the user details of a particular user from the service.</p>
<p data-id="b8ee56fb384a6b8b7d904d8e4d09ddb8">The <em>REST-based</em> service will expose this <em>url</em> to all its clients to fetch the user details using the above stated <em>url</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="decoupling-clients-the-backend-service" data-id="c2f731c2440d68b6a38c307e7c543f65">Decoupling Clients &amp; the Backend Service <a class="markdownIt-Anchor" href="#decoupling-clients-the-backend-service"><span class="anchor-link">#</span></a></h2>
<p data-id="491ba7054f1778920b093cb5a6e4ae40">With the availability of the endpoints, the backend service does not have to worry about the client implementation. It just calls out to its multiple clients &amp; says “<em>Hey everyone, here is the url address of the resource/information you need. Hit it when you need it. Any client with the required authorization to access a resource can access it</em>”.</p>
<p data-id="2c46083d1402970f15ee24e99450babf">Developers can have different implementations with separate codebases, for different clients, be it a mobile browser, a desktop browser, a tablet or an API testing tool. Introducing new types of clients or modifying the client code has no effect on the functionality of the backend service.</p>
<p data-id="29f7ef15bb5b38e1de925135e0d39a8f"><em>This means the clients and the backend service are decoupled</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="application-development-before-the-rest-api" data-id="b2f3d0208d8aad6fa94b65fc571bee53">Application Development Before the REST API <a class="markdownIt-Anchor" href="#application-development-before-the-rest-api"><span class="anchor-link">#</span></a></h2>
<p data-id="fc6ddc167b9b1e75ef1ecc8a37d50152">Before the <em>REST-based API</em> interfaces got mainstream in the industry. We often tightly coupled the backend code with the client. <em>JSP (Java Server Pages)</em> is one example of it.</p>
<p data-id="82c2682535429b22377c53769b8de1ed">We would always put business logic in the <em>JSP</em> tags. Which made code refactoring &amp; adding new features really difficult as the logic got spread across different layers.</p>
<p data-id="2c5f877be3c8970604395d0225c082de">Also, in the same codebase, we had to write separate code/classes for handling requests from different types of clients. A different servlet for a mobile client and a different one for a web-based client.</p>
<p data-id="5c7eb6d7c48d276c98ecfddd2961af35">After the <em>REST APIs</em> became widely used, there was no need to worry about the type of the client. Just provide the endpoints &amp; the response would contain data generally in the <em>JSON</em> or any other standard data transport format. And the client would handle the data in whatever way they would want.</p>
<p data-id="226e3bf8f07500cc776ea0cabcf6d113">This cut down a lot of unnecessary work for us. Also, adding new clients became a lot easier. We could introduce multiple types of new clients without considering the backend implementation.</p>
<p data-id="3397ace198cc433649bc5d653baf4825">In today’s industry landscape, there is hardly any online service without a <em>REST API</em>. Want to access public data of any social network? Use their <em>REST API</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="api-gateway" data-id="67c4fe4d1c8aaa5ab7c07c41a705b28c">API Gateway <a class="markdownIt-Anchor" href="#api-gateway"><span class="anchor-link">#</span></a></h2>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/courses_web-application-software-architecture-101_assets_api_collection_6064040858091520_6411938009448448_page_6353247012913152_image_6649249657782272.jpeg" alt=""></p>
<p data-id="5e7adaee6a42140c38a02a2b58c48c53">The <em>REST-API</em> acts as a gateway, as a single entry point into the system. It encapsulates the business logic. Handles all the client requests, taking care of the authorization, authentication, sanitizing the input data &amp; other necessary tasks before providing access to the application resources.</p>
<p data-id="1b63e8b8ea45a917aac91da2f5767475">So, now we are aware of the client-server architecture, we know what a <em>REST API</em> is. It acts as the interface &amp; the communication between the client and the server happens over HTTP.</p>
<p data-id="0751733f8d69fc17444a9a5dc018a685">Let’s look into the HTTP Pull &amp; Push-based communication mechanism.</p>
</div></div></div></div></div></div></div></div></div>
