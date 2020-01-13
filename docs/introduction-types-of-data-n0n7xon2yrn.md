---
id: introduction-types-of-data-n0n7xon2yrn
title: Introduction & Types of Data
sidebar_label: Introduction & Types of Data
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will have an introduction to databases and the different types of data.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#what-is-a-database">What Is A Database?</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#structured-data">Structured Data</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#unstructured-data">Unstructured Data</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#semi-structured-data">Semi-structured Data</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#user-state">User state</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="what-is-a-database" data-id="a8d0fdbf757270721ffd2106d29d0e24">What Is A Database? <a class="markdownIt-Anchor" href="#what-is-a-database"><span class="anchor-link">#</span></a></h2>
<p data-id="1f07e0d999d3fd089ee450a8d1f1de53">A database is a component required to persist data. Data can be of many forms: structured, unstructured, semi-structured and user state data.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4891993308135424_image_5682420466581504.jpeg" alt=""></p>
<p data-id="f8ed2d719d277651b61950c19664c67d">Let’s quickly have an insight into the classification of data before delving into the databases.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="structured-data" data-id="b969ca95465ab09c10bd9f449c44fffb">Structured Data <a class="markdownIt-Anchor" href="#structured-data"><span class="anchor-link">#</span></a></h2>
<p data-id="4881c5bd1cc01f9fc9235c3441e90a46">Structured data is the type of data which conforms to a certain structure, typically stored in a database in a <em>normalized</em> fashion.</p>
<p data-id="a7e4ade0fb7952f527e614a5e61e4491">There is no need to run any sort of data preparation logic on structured data before processing it. Direct interaction can be done with this kind of data.</p>
<p data-id="19421483f863f4b27ae1c6db857067a3">An example of structured data would be the personal details of a customer stored in a database row. The customer id would be of <em>integer</em> type, the name would be of <em>String</em> type with a certain character limit etc.</p>
<p data-id="653ba0d3b6203edfdd239b1a645e9261">So, with structured data, we know what we are dealing with. Since the customer name is of String type, without much worry of errors or exceptions, we can run String operations on it.</p>
<p data-id="5548c4ac4e74a7aa9e1e0b15b763b153">Structured data is generally managed by a query language such as <em>SQL (Structured query language)</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="unstructured-data" data-id="f8d810dc8f329d9720c2f5c2ef831992">Unstructured Data <a class="markdownIt-Anchor" href="#unstructured-data"><span class="anchor-link">#</span></a></h2>
<p data-id="a37e9d7609c108d0e7a35026d5b69f8b">Unstructured data has no definite structure. It is generally the heterogeneous type of data comprising of text, image files, video, multimedia files, pdfs, Blob objects, word documents, machine-generated data etc.</p>
<p data-id="d6e12692d8027d53d040ea8e2d4927ae">This kind of data is often encountered in data analytics. Here the data streams in from multiple sources such as IoT devices, social networks, web portals, industry sensors etc. into the analytics systems.</p>
<p data-id="0d22423fd776778c843280131472c0b0">We cannot just directly process unstructured data. The initial data is pretty raw, we have to make it flow through a data preparation stage which segregates it based on some business logic &amp; then runs the analytics algorithms on it.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="semi-structured-data" data-id="020d8354b5f87a728ff949ca8f2b1112">Semi-structured Data <a class="markdownIt-Anchor" href="#semi-structured-data"><span class="anchor-link">#</span></a></h2>
<p data-id="6faf26864bc703e378557bac2fc55b6c">Semi-structured data is a mix of structured &amp; unstructured data. Semi-structured data is often stored in data transport formats such as XML or JSON and is handled as per the business requirements.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="user-state" data-id="6265824a0d63a286231db280bee64ed3">User state <a class="markdownIt-Anchor" href="#user-state"><span class="anchor-link">#</span></a></h2>
<p data-id="27bfbf62109d4d50d22e1d6f3f15e0c9">The data containing the user state is the information of activity which the user performs on the website.</p>
<p data-id="e5b119deb544a276e732d64172c93913">For instance, when browsing through an e-commerce website, the user would browse through several product categories, change the preferences, add a few products to the reminder list for the price drops.</p>
<p data-id="571cf588015db2cf2e3d580e60d9cf30">All this activity is the user state. So next time, when the user logs in, he can continue from where he left off. It would not feel like that one is starting fresh &amp; all the previous activity is lost.</p>
<p data-id="ddfd443af475ad445d51f05b9c58bd1b">Storing user state improves the browsing experience &amp; the conversion rate for the business.<br>
So, now we are clear on the different types of data. Let’s have a look into different types of databases.</p>
<p data-id="24e91c5bb5d2c9f03e3b8a7c3d0d2a48">There are multiple different types of databases with specific use cases. We’ll quickly go through each of them in order to have a bird’s eye view of the database realm.</p>
</div></div></div></div></div></div></div></div></div>