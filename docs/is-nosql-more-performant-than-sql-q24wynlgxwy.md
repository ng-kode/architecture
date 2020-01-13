---
id: is-nosql-more-performant-than-sql-q24wynlgxwy
title: Is NoSQL More Performant than SQL?
sidebar_label: Is NoSQL More Performant than SQL?
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will learn if the NoSQL database is more performant than the SQL databases.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#why-do-popular-tech-stacks-always-pick-nosql-databases">Why Do Popular Tech Stacks Always Pick NoSQL Databases?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-world-case-studies">Real World Case Studies</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#using-both-sql-nosql-database-in-an-application">Using Both SQL &amp; NoSQL Database In An Application</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="95e22033de7a3f8f97ab523cc1bc6ec3"><em>Is NoSQL more performant than SQL?</em> This question is asked all the time. And I have a one-word answer for this.</p>
<p data-id="65df116fd53533becff043ca89f6b1fb">No!!</p>
<p data-id="647ea74cdf7db724b4920915cad8204b">From a technology benchmarking standpoint, both <em>relational</em> and <em>non-relational</em> databases are equally performant.</p>
<p data-id="274448991b3a675ff8c2e54360130142">More than the technology, it’s how we design our systems using the technology that affects the performance.</p>
<p data-id="39375eefe7d5897ae08760225f3cb519">Both <em>SQL</em> &amp; <em>NoSQL</em> tech have their use cases. We have already gone through them in the lessons <a href="https://www.educative.io/collection/page/6064040858091520/6411938009448448/6652931912761344" target="_blank"><em>When to pick a relational database?</em></a> &amp; <a href="https://www.educative.io/collection/page/6064040858091520/6411938009448448/4828109427703808" target="_blank"><em>When to pick a NoSQL database?</em></a></p>
<p data-id="37aba3a95cec0cd5fdf30ca64e9595fd">So, don’t get confused with all the hype. Understand your use case and then pick the technology accordingly.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="why-do-popular-tech-stacks-always-pick-nosql-databases" data-id="a2d99aee7c5f8ad997eb6f63ffb7283c">Why Do Popular Tech Stacks Always Pick NoSQL Databases? <a class="markdownIt-Anchor" href="#why-do-popular-tech-stacks-always-pick-nosql-databases"><span class="anchor-link">#</span></a></h2>
<p data-id="21bb23d1dc4ffaa76c50c78bd2c50629"><em>But why do the popular tech stacks always pick NoSQL databases?</em> For instance, the <em>MEAN</em> (<em>MongoDB</em>, <em>ExpressJS</em>, <em>AngularJS/ReactJS</em>, <em>NodeJs</em>) stack.</p>
<p data-id="5f4d7cfdc42b7ebcdb0d3d5661fbb521">Well, most of the applications online have common use cases. And these tech stacks have them covered. There are also commercial reasons behind this.</p>
<p data-id="3cad6e11c11abd7e5dd8e9676246ddcf">Now, there are a plethora of tutorials available online &amp; a mass promotion of popular tech stacks. With these resources, it’s easy for beginners to pick them up and write their applications as opposed to running solo research on other technologies.</p>
<p data-id="5887015307e18f45ea504bb556028163">Though, we don’t always need to stick with the popular stacks. We should pick what fits best with our use case. There are no ground rules, pick what works for you.</p>
<p data-id="b00dccd1bc7bd2aa42750f0ac01db0c2">We have a separate lesson on how to pick the right tech stack for our app further down the course. We will continue this discussion there.</p>
<p data-id="7daf1ece2fd0cd811687ad0f2fc7066e">Coming back to the performance, it entirely depends on the application &amp; the database design. If we are using more <em>Joins</em> with <em>SQL</em>. The response will inevitably take more time.</p>
<p data-id="f793289dde42c2c73e6c1762db41ef57">If we remove all the relationships and joins, <em>SQL</em> becomes just like <em>NoSQL</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-world-case-studies" data-id="5686166c0f95e34154bdd62843c69e10">Real World Case Studies <a class="markdownIt-Anchor" href="#real-world-case-studies"><span class="anchor-link">#</span></a></h2>
<p data-id="1f5456a9cdbb99e2288a50fe763fc7f5"><a href="https://www.8bitmen.com/what-database-does-facebook-use-a-1000-feet-deep-dive/" target="_blank">Facebook uses MySQL for storing its social graph of millions of users.</a> Though it did have to change the DB engine and make some tweaks but MySQL fits best for its use case.</p>
<p data-id="1b05e9bcf61ce718559a46cba00dd7d8">Quora uses MySQL pretty efficiently by partitioning the data at the application level. <a href="https://www.quora.com/Why-does-Quora-use-MySQL-as-the-data-store-instead-of-NoSQLs-such-as-Cassandra-MongoDB-or-CouchDB-Are-they-doing-any-JOINs-over-MySQL-Are-there-plans-to-switch-to-another-DB" target="_blank">This is an interesting read on it.</a></p>
<blockquote data-id="a18b357b9b93af718f7bbfccd88e4385">
<p><strong>Note:</strong> A well-designed SQL data store will always be more performant than a not so well-designed NoSQL store.</p>
</blockquote>
<p data-id="0216e990dacecf491c4597d00a7f3469">Hmmm…. Ok!! Alright</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="using-both-sql-nosql-database-in-an-application" data-id="d7c18d7095b499ceb8e0ed8f3713c63d">Using Both SQL &amp; NoSQL Database In An Application <a class="markdownIt-Anchor" href="#using-both-sql-nosql-database-in-an-application"><span class="anchor-link">#</span></a></h2>
<p data-id="e42d236ba519f37189d65cef3ac21a32"><em>Can’t I use both in my application? Both SQL &amp; a NoSQL datastore. What if I have a requirement fitting both?</em></p>
<p data-id="06e59437eac3544309340afc9058fe97">You can!! As a matter of fact, all the large-scale online services use a mix of both to implement their systems and achieve the desired behaviour.</p>
<p data-id="3f3f64afa2b4fa3b025817960e8d6948">The term for leveraging the power of multiple databases is called <em>Polyglot Persistence</em>. Let’s know more about it in the next lesson.</p>
</div></div></div></div></div></div></div></div></div>