---
id: key-things-to-remember-when-picking-the-tech-stack-rlykxnwmmjq
title: Key Things To Remember When Picking the Tech Stack
sidebar_label: Key Things To Remember When Picking the Tech Stack
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson. I’ll share a few key things which we should bear in mind when researching on a technology stack for our application.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li>
<ul>
<li><a href="#be-thorough-with-the-requirements">Be Thorough with the Requirements</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#see-if-what-we-already-know-fits-the-requirements">See If What We Already Know Fits the Requirements</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#does-the-tech-we-have-picked-has-an-active-community-how-is-the-documentation-the-support">Does the Tech We Have Picked Has An Active Community? How Is the Documentation &amp; the Support?</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#is-the-tech-being-used-by-big-guns-in-production">Is the Tech Being Used by Big Guns in Production?</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#check-the-license-is-it-open-source">Check the License. Is It Open Source?</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#availability-of-skilled-resources-on-the-tech">Availability Of Skilled Resources on the Tech</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="6264d89498e8be89d6fee6cf1d0dda9f">I’ve written numerous projects from the ground up, spent countless hours scavenging the web, browsing through technologies, frameworks to pick the right tech that would align with my requirements.</p>
<p data-id="c7b63c4fac39af4c5efc4963535e3b32">I have wasted days, if not months, trying to implement stuff with a not so fitting technology. I have implemented stuff with tech having no support and community and have later cried for days into a pillow.</p>
<p data-id="d737b637572e395ab0b4a66341f5b4a5">Picking the right tech stack is crucial for the success of our business. There is no way around it. I think we all understand this fact pretty well. Once we pick the tech &amp; get down to coding there should be no looking back. We naturally can’t afford it.</p>
<p data-id="5c7544c05610e81069b51dd0b334b1e5">The guidelines listed below is the gist of my experience, they are the factors which hold much importance in the process of picking the right technology stack.</p>
<p data-id="c327d384774f0500f9bfcc76a8aa6658">So, without any further ado. Let’s get started.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="be-thorough-with-the-requirements" data-id="677ba43371af7f312f28a4e535b7f1ee">Be Thorough with the Requirements <a class="markdownIt-Anchor" href="#be-thorough-with-the-requirements"><span class="anchor-link">#</span></a></h3>
<p data-id="ee5daadf5325ab767dc28c7388cad48f">We should be crystal clear on what we are going to build. Things should not be hazy. We cannot pick the right tech if we are unclear on the requirements. Once we go hunting, we should be clear on what we are looking for.</p>
<p data-id="2d987b520743a87bd8227896bc1a5a71">For instance, when looking for a database, we should be clear on if we are going to store relational data or will it be document-oriented, semi-structured or with no structure at all.</p>
<p data-id="6fcd493d7acdb0d6b3b0eb1a3136a217">Are we handling quite a large amount of data which is expected to grow exponentially? Or the data is expected to grow at a manageable pace upto a certain limit?</p>
<p data-id="bec86435ad98c8d3a2f621d43c482ebb">Will a <em>monolithic architecture</em> serve our requirements well or do we need to split our app into several different modules?</p>
<p data-id="a9196d88ab63264c3c34f27963ed4663">Splitting the app into several modules, using heterogeneous tech in services, helps us bail out on a particular technology in case things don’t work out.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="see-if-what-we-already-know-fits-the-requirements" data-id="8b5abe496e81d6625409e03b881b2619">See If What We Already Know Fits the Requirements <a class="markdownIt-Anchor" href="#see-if-what-we-already-know-fits-the-requirements"><span class="anchor-link">#</span></a></h3>
<p data-id="699e6e8699398b03545f17c23d80fa36">It’s easier to build new applications with the tech we already know. We don’t have to go through the steep learning curve that comes along with the new tech.</p>
<p data-id="3fe7e217ae3914ff0157f266827ce76d">Also, things are comparatively clearer when using the tech, we are well familiar with. Being aware of the nitty-gritty, having familiarity with the errors, exceptions &amp; the knowledge to fix them helps us release the features at a quick pace.</p>
<p data-id="25ac28ec6b0abd7b61ab6c231702cf31">Avoid running for shiny new toys until you really need them. Do not fall for the hype.</p>
<p data-id="023c9360bdf898fe6f5fccf72b421643">Imagine an exception thrown by a new tech which you haven’t seen before ever in your life &amp; also cannot find the solution online. You are stranded. There is no one to help you, all you hear is crickets.</p>
<p data-id="eb47668857a93664f0662f8d7c5cf229">I’ve been there, done that. It’s frustrating, clicking through all the search result pages of Google. Finding nothing.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="does-the-tech-we-have-picked-has-an-active-community-how-is-the-documentation-the-support" data-id="c93199e6d9093bdbcee2167ab15b1138">Does the Tech We Have Picked Has An Active Community? How Is the Documentation &amp; the Support? <a class="markdownIt-Anchor" href="#does-the-tech-we-have-picked-has-an-active-community-how-is-the-documentation-the-support"><span class="anchor-link">#</span></a></h3>
<p data-id="c22e69ce8815088b48449ac057606d17">The technology we pick ought to have an active community. Check the involvement of the community on <em>GitHub</em>, <em>StackOverflow</em> etc. The documentation should be smooth, easy to comprehend.</p>
<p data-id="ea7467e6a2e3dcf2428afbb14d364758">Larger the community, the better. Having an active community means updated tools, libraries, frameworks &amp; stuff.</p>
<p data-id="8de746f302fd7b0ba58b04887fd60065">See if there is official support available for the tech? There should be some rescue available if we get stranded down the road. Right?</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="is-the-tech-being-used-by-big-guns-in-production" data-id="3c17d12ce27793f65aeca2a59023f307">Is the Tech Being Used by Big Guns in Production? <a class="markdownIt-Anchor" href="#is-the-tech-being-used-by-big-guns-in-production"><span class="anchor-link">#</span></a></h3>
<p data-id="59913bd21aecc0839ed441eca6b75d2c">If the tech we are picking is being used by big guns in the industry, then this confirms it being battle-tested. It can be used in production without any worries.</p>
<p data-id="e01bb22698a26c85b1375df69fd2ee87">We can be certain that down the line we won’t face any inherent scalability, security or any other design-related issues with the technology. Since, the codebase is continually patched with new updates, bug &amp; design fixes.</p>
<p data-id="131b9c2f994ce93b6700f83c0d42073e">We can go through the engineering blogs of the companies to get more information on how they have implemented the tech.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="check-the-license-is-it-open-source" data-id="ddaaa332ee2829feb39ab1db42dd07a1">Check the License. Is It Open Source? <a class="markdownIt-Anchor" href="#check-the-license-is-it-open-source"><span class="anchor-link">#</span></a></h3>
<p data-id="f8eeaf5964fc1a0d099131b9d3f036e4">Picking an <em>open-source</em> technology helps us write our own custom features in case the original solution does not have it. We do not have to rely on the creator of the tech for new features &amp; stuff.</p>
<p data-id="539105b9420833d2ff3bda962c1efeb2">Also, in terms of money, we don’t have to pay anyone any sort of fee to use the product.
<em>Open-source</em> tech also has a larger community since the code is open to all, anyone can fork it, start writing new features or fix the existing known bugs.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="availability-of-skilled-resources-on-the-tech" data-id="c20ce5cf0ddc2d9f6bd68eeec454952b">Availability Of Skilled Resources on the Tech <a class="markdownIt-Anchor" href="#availability-of-skilled-resources-on-the-tech"><span class="anchor-link">#</span></a></h3>
<p data-id="cef3267b0cb8f225e0eeb74f657f9c63">Once our business starts gaining traction. We would need a hand to move at a quick pace &amp; roll out new features within a stipulated time. It’s important that there are enough skilled resources available in the industry on the technology we pick.</p>
<p data-id="cd3439385a6771f18aee835083911eb3">For instance, it’s always easy to find a MySQL administrator or a Java developer as opposed to looking for a resource skilled on comparatively newer technology.</p>
<p data-id="aeada3a1de966f18901179131e994031">Well, this concludes the lesson. Moving on to the next.</p>
</div></div></div></div></div></div></div></div></div>