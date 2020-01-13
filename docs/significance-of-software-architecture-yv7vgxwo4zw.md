---
id: significance-of-software-architecture-yv7vgxwo4zw
title: Significance Of Software Architecture
sidebar_label: Significance Of Software Architecture
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we'll cover the significance of web application &amp; software architecture &amp; the reasoning behind learning it.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#importance-of-getting-the-application-architecture-right">Importance Of Getting The Application Architecture Right</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#an-overview-of-the-software-development-process">An Overview Of The Software Development Process</a>
<ul>
<li><a href="#proof-of-concept">Proof Of Concept</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li><a href="#course-design">Course Design</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="importance-of-getting-the-application-architecture-right" data-id="835fad8879f748ce4f6d3203ebf4288e">Importance Of Getting The Application Architecture Right <a class="markdownIt-Anchor" href="#importance-of-getting-the-application-architecture-right"><span class="anchor-link">#</span></a></h2>
<p data-id="3c5a89c7ea3f55884fd8f392c57ca190">The key element in successfully creating anything is getting the base right. Now whether it is constructing a building or making a pizza. If we don’t get the base right, we have to start over. Yeah!!.. I know, but there is no other way around.</p>
<p data-id="14b297e4a78234fd9329fc02413b8c93">Building a web application is no different. The architecture is it’s base &amp; has to be carefully thought, to avoid any major design changes &amp; code refactoring at a later point in time.</p>
<p data-id="4893c7bad93ab425a082308f658874cb">Speaking with experience, you don’t want to delve into re-designing stuff. It eats up your time like a black hole. It has the potential to push your shipping date further down the calendar by months, if not longer. And I won’t even bring up the wastage of engineering &amp; financial resources which is caused due to this. No, I won’t!!</p>
<p data-id="2420d717dae8ffabd85221219595901a">It also depends on what stage of the development process we hit an impasse due to the hasty decisions taken during the initial design phases.
So, before we even touch the code &amp; get our hands dirty, we have to make the underlying architecture right.</p>
<p data-id="8d33fa75242c1598c6990e2fb6c10a6f">A look at the architecture of our app should bring a smile to everyone’s face.</p>
<p data-id="9513594fe225d7587d6b5eceee2d7dc1">Though software development is an iterative and evolutionary process, we don’t always get things perfect at the first go. Still, this can’t be an excuse for not doing our homework.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="an-overview-of-the-software-development-process" data-id="faad1200f531c32a5013a538c554006f">An Overview Of The Software Development Process <a class="markdownIt-Anchor" href="#an-overview-of-the-software-development-process"><span class="anchor-link">#</span></a></h2>
<p data-id="2e63209e06083e6fe438acfb35683a82">In the industry, architects, developers and product owners spend a lot of time studying &amp; discussing business requirements. In software engineering jargon, this is known as the <em>Requirement Gathering &amp; Analysis</em>.</p>
<p data-id="f75ac171625be22be2a73ac2a953fa9b">Once we are done with the business requirements, we sit down &amp; brainstorm the use cases which we have to implement. This involves figuring out the corner cases as early as possible &amp; fitting the Lego blocks together.</p>
<p data-id="912e0fff1992ffd0592db401f807af25">If you’re a fan of documentation, you might also want to write a <em>high-level design document</em>.</p>
<p data-id="e60ee242b991372df6d69e3e3edcaea7">Now, we have an understanding of the business requirements, use cases, corner cases and all. It’s time to start the research on picking the right technology stack to implement the use cases.</p>
<h3 id="proof-of-concept" data-id="a388763274b56505d62632f96056db5a">Proof Of Concept <a class="markdownIt-Anchor" href="#proof-of-concept"><span class="anchor-link">#</span></a></h3>
<p data-id="a606e71a3d6536bb81844ca076c897f3">After we pick the fitting tech stack, we start writing a <em>POC (Proof of Concept)</em></p>
<p data-id="492f0c299082ef0f16cec67375838a0a"><em>Why a POC?</em></p>
<p data-id="0d81d0e29949136b0d8bc1ce62744604">A <em>POC</em> helps us get a closer, more hands-on view of the technology &amp; the basic use case implementation. We get an insight into the pros and cons of the tech, performance or other technical limitations if any.</p>
<p data-id="6849131dfb8c98bcbd931067e7b7b771">It helps with the learning curve if we’re working with completely new tech, also the non-technical people like the product owners, stakeholders have something concrete to play with &amp; to base their further decisions on.</p>
<p data-id="6bd1574b79dc028bbdb74bb6211d8b92">Now, this is only for an industry scale product. If you are a solo indie developer or a small group, you can always skip the <em>POC</em> part and start with the main code.</p>
<p data-id="e92b4cfe320634cf16b50d96cefd4bdf">So, we showcase the <em>POC</em> to the stakeholders &amp; if everyone is satisfied, we finally get down to creating the main repo &amp; our first dev branch on <em>GitHub</em>, or any other similar code hosting service which the business prefers.</p>
<p data-id="5603ed57996d2e593ee43aebc2fe7c52">Phew!!</p>
<p data-id="baaa19ca2233b1d05392f9d28f2663d9">So, by now you would have realized how important it is to get the architecture right at the first time &amp; the knowledge of web architecture to developers.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="course-design" data-id="3e1e41497bd013fca01b352183b45ad0">Course Design <a class="markdownIt-Anchor" href="#course-design"><span class="anchor-link">#</span></a></h2>
<p data-id="47e6b7d2fcf3dd267b3444db29434671">Hmmm…. Alright, this being said. Now speaking of this course. It is divided into two parts. In the first, we will discuss the concepts &amp; the architectural components involved in designing web applications.</p>
<p data-id="80d3d2944ba0a6f1b20188d575790000">We will get insights into different tiers of software applications, <em>monolithic</em> repos, <em>microservices</em>, <em>peer to peer</em> architecture &amp; a lot more.</p>
<p data-id="03820ba19c8a6f0216c161a98169fb68">In the second part, we will go through some of the use cases of designing the architecture for applications which we use in our day to day lives &amp; are well familiar with.</p>
<p data-id="359b04c285aa5320c1a779812319230b">We will also understand how applications are designed from the bare bones. What is the thought process of picking the right technology stack for our use case &amp; so forth?</p>
<p data-id="130ec72fb77b37fbe8ce1ba0afd56c60">So, without further ado. Let’s get started.</p>
</div></div></div></div></div></div></div></div></div>