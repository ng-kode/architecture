---
id: relational-database-n8p9977x4p2
title: Relational Database
sidebar_label: Relational Database
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss the relational databases.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-relational-database">What Is A Relational Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#what-are-relationships">What Are Relationships?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#data-consistency">Data Consistency</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#acid-transactions">ACID Transactions</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-relational-database" data-id="885ad3acb327e51d188aeab49cbf45c8">What Is A Relational Database? <a class="markdownIt-Anchor" href="#what-is-a-relational-database"><span class="anchor-link">#</span></a></h2>
<p data-id="46486d31cdaead00747089485badc4d2">This is the most common &amp; widely used type of database in the industry. A relational database saves data containing relationships. <em>One to One</em>, <em>One to Many</em>, <em>Many to Many</em>, <em>Many to One</em> etc. It has a relational data model. <em>SQL</em> is the primary data query language used to interact with relational databases.</p>
<p data-id="65d27b925b1f7567aae51b1729c8acbf"><em>MySQL</em> is the most popular example of a relational database. Alright!! I get it but what are relationships?</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-are-relationships" data-id="60b80d60e4b405005d6784db3d95391d">What Are Relationships? <a class="markdownIt-Anchor" href="#what-are-relationships"><span class="anchor-link">#</span></a></h2>
<p data-id="bfc2fc637667911dde0ba36467c28faa">Let’s say you as a customer buy five different books from an online book store. When you created an account on the book store you would have been assigned a customer id say C1. Now that C1[You] is linked to five different books B1, B2, B3, B4, B5.</p>
<p data-id="4542336ca2e95304bc4bcc9ce32068d3">This is a <em>one to many</em> relationship. In the simplest of forms, one table will contain the details of all the customers &amp; another table will contain all the products in the inventory.</p>
<p data-id="8484c343d986813602e1978a578a96e1">One row in the customer table will correspond to multiple rows in the product inventory table.</p>
<p data-id="8b8765cf7ff7de2fe052305b6f97744c">On pulling the user object with id C1 from the database we can easily find what books C1 purchased via the relationship model.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="data-consistency" data-id="f288b7f4b8fccc8ed63ae4435322ab22">Data Consistency <a class="markdownIt-Anchor" href="#data-consistency"><span class="anchor-link">#</span></a></h2>
<p data-id="d28b600570de0a9eee2608feed28e0e4">Besides, the relationships, relational databases also ensure saving data in a normalized fashion.
In very simple terms, normalized data means a unique entity occurs in only one place/table, in its simplest and atomic form and is not spread throughout the database.</p>
<p data-id="b33c4936665592d121146303043cee47">This helps in maintaining the consistency of the data. In future, if we want to update the data, we just update at that one place and every fetch operation gets the updated data.</p>
<p data-id="dfe74ce79235a3ea6d2180c8f48de608">Had the data been spread throughout the database in different tables. We would have to update the new value of an entity everywhere. This is troublesome and things can get inconsistent.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="acid-transactions" data-id="8494fa422bca22f56059df808a69030f">ACID Transactions <a class="markdownIt-Anchor" href="#acid-transactions"><span class="anchor-link">#</span></a></h2>
<p data-id="445e3c6358c377d56b672c7f70bf2c93">Besides normalization &amp; consistency, relational databases also ensure <em>ACID</em> transactions.</p>
<p data-id="3ca7b4a65dd74b0b73d97f195e573d3c"><em>ACID – Atomicity, Consistency, Integrity, Durability</em>.</p>
<p data-id="0052763ce8ed24bb33dd32fb33cb1bd1">An acid transaction means if a transaction in a system occurs, say a financial transaction, either it will be executed with perfection without affecting any other processes or transactions.</p>
<p data-id="c414c333720400b3180cfb5345dfbd64">The system will have a new state after the transaction which is durable &amp; consistent. Or if anything, amiss happens during the transaction, say a minor system failure, the entire operation is rolled back.</p>
<p data-id="360eb6a8b881191d42ba9e58c85e6c2e">When a transaction happens, there is an initial state of the system <em>State A</em> &amp; then there is a final state of the system <em>State B</em> after the transaction. Both the states are consistent and durable.</p>
<p data-id="cdc90912e9df98e5b222a75bf3758684">A relational database ensures that either the system is in <em>State A</em> or <em>State B</em> at all times. There is no middle state. If anything fails, the system goes back to <em>State A</em>.</p>
<p data-id="941409163a4bc14caec48b2fb0ebb021">If the transaction is executed smoothly the system transitions from <em>State A</em> to <em>State B</em>.</p>
</div></div></div></div></div></div></div></div></div>