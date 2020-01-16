---
id: notification-systems-real-time-feeds-with-message-queues-myj404mrxvp
title: Notification Systems & Real-time Feeds with Message Queues
sidebar_label: Notification Systems & Real-time Feeds with Message Queues
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss how notification systems and real-time feeds are implemented using message queues.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#real-world-use-case">Real-World Use Case</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#pull-based-approach">Pull-Based Approach</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#push-based-approach">Push-Based Approach</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="f3e755ac6b2f8dcd3ddc63922463ab39">This is the part where we get an insight into how notification systems and real-time feeds are designed with the help of message queues. However, these modules are really complex in today’s modern Web 2.0 applications. They involve machine learning, understanding the user behaviour, recommending new relevant information &amp; integration of other modules with them etc. We won’t get into that level of complexity, simply because that’s not required.</p>
<p data-id="d4904c0220c56f115ae9ddae3fa4982d">I present a very simple use case so that we can wrap our heads around it.</p>
<p data-id="e388ed1cdb0b65ea90f4a3e14c41581e">Also, as we discuss this use case, I would like you to think from your own perspective. Imagine, how you would implement such a notification system from the bare bones. This will help you understand the concept better.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-world-use-case" data-id="558de4e2ca7a02b7074c03f6f337122f">Real-World Use Case <a class="markdownIt-Anchor" href="#real-world-use-case"><span class="anchor-link">#</span></a></h2>
<p data-id="680be653230e675d9b2ea3517993ebdd">Alright!! So, imagine we are writing a social network like Facebook using a relational database and we would use a message queue to add the asynchronous behaviour to our application.</p>
<p data-id="969caff661f91a0da93d3182aee71fe4">In the application, a user will have many friends and followers. This is a <em>many to many</em> relationship like a social graph. One user has many friends, and he would be a friend of many users. Just like as we discussed in the graph database lesson. Remember?</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4659342001307648_image_5871941837651968.jpeg" alt=""></p>
<p data-id="cc8f063704f87bdb84b6f9f348aa0072">So, when a user creates a post on the website, we would persist it in the database. There will be one <em>User</em> table and another <em>Post</em> table. Since one user will create many posts, it will be a <em>one to many</em> relationship between the user and his posts.</p>
<p data-id="0b1d391edab341d97bf7057b7acdb745">Also, at the same time, as we persist the post in the database, we have to show the post created by the user on the home page of his friends and followers, even send the notification if needed.</p>
<p data-id="8210c692fcd3a502f02f8edfddaf54ff">How would you implement this? Pause &amp; think… before you read further.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="pull-based-approach" data-id="fa21649c99f66ce305728831ab6c2c30">Pull-Based Approach <a class="markdownIt-Anchor" href="#pull-based-approach"><span class="anchor-link">#</span></a></h2>
<p data-id="085386264aef755d5524757cf8b06b43"><em>Alright!!</em></p>
<p data-id="43bda96c3110b88d6934e894b9d7c64b">One simple way to implement this without the message queue would be, for every user on the website, at regular short intervals poll the database if any of his connections have a new update.</p>
<p data-id="5f8c37fe416e62d65e78802a3ee80053">For this, first, we will find all the connections of the user and then run a check for every connection one by one if there is a new post created by them.</p>
<p data-id="9c33d7fb7e3105d95784862b6f49e440">If there are, the query will pull up all the new posts created by the connections of a user and display on his home page. We can also send the notifications to the user about the same, tracking the count of those with the help of a notification counter column in the <em>User</em> table &amp; adding an extra <em>AJAX</em> poll query from the client for new notifications.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4659342001307648_image_6667990026158080.jpeg" alt=""></p>
<p data-id="95484997f7334a83c70d5f7b4ae7fcce"><em>What do you think of this approach? Pretty simple &amp; straight forward right?</em></p>
<p data-id="b98a4e913df7ceab85da42a9832c792f">There are two major downsides to this approach.</p>
<p data-id="bb3edbdd0ffe9c45f97757936ca909dd">First, we are polling the database so often, this is expensive. It will consume a lot of bandwidth &amp; will also put a lot of unnecessary load on the database.</p>
<p data-id="ee4ddc51b1aab3b0b7ea6b99a6d893c2">The second downside is, the display of the user post on the home page of his connection will not be in real-time. The posts won’t display until the database is polled. We may call this as real-time but is not really real-time.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="push-based-approach" data-id="0a9a8d1f5d90cb13de10d4ef845f4d8e">Push-Based Approach <a class="markdownIt-Anchor" href="#push-based-approach"><span class="anchor-link">#</span></a></h2>
<p data-id="d10f9287de759b2990b5707e26bc09f1">Let’s make our system more performant, instead of polling the database every now and then we will take the help of a message queue.</p>
<p data-id="166f15b02319b1fbfa8b54ee11a80779">So, this time when a user creates a new post, it will have a <em>distributed transaction</em>. One transaction will update the database, and the other transaction will send the post payload to the message queue. <em>Payload</em> means the content of the message posted by the user.</p>
<p data-id="c91efcb47a2b4f5898591cac95449e81">Notification systems and real-time feeds establish a <em>persistent connection</em> with the database to facilitate real-time streaming of data. We have already been through this.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4659342001307648_image_6540836621778944.jpeg" alt=""></p>
<p data-id="9e60316fb5fdd1c5552224169edc7111">The message queue on receiving the message will asynchronously immediately push the post to the connections of the user which are online. There is no need for them to poll the database at regular intervals to check if the user has created a post.</p>
<p data-id="8d54a7b19c23ff4163ba71bed68fc836">We can also use the message queue temporary storage with a <em>TTL Time to wait</em> for the connections of the user to come online &amp; then push the updates to them. We can also have separate <em>Key-value</em> database to store the details of the user required to push the notifications to his connections. Like the ids of his connections and stuff. This would avert the need to even poll the database to get the connections of the user.</p>
<p data-id="89dd068bbc0c41357ced2c720f4a583d">So, did you see how we transitioned from a <em>pull-based</em> mechanism to a <em>push-based</em> mechanism with the help of message queues? This would certainly spike the performance of the application and cut down a lot of resource consumption, thus saving truckloads of our hard-earned money.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_4659342001307648_image_6581126971785216.jpeg" alt=""></p>
<p data-id="548d4aad032b3645031aa44d4040b340">Regarding the <em>distributed transactions</em>, it entirely depends on how we want to deal with it. Though the transactions are distributed, they can still work as a single unit.</p>
<p data-id="e602e2f8c14c33df87cbb345eb465dfd">If the database persistence fails, naturally, we will roll back the entire transaction. There won’t be any message push to the message queue either.</p>
<p data-id="6f6664510672eac018627628ea6d0245">What if the message queue push fails? Do you want to roll-back the transaction? Or do you want to proceed? The decision entirely depends on you. How you want your system to behave.</p>
<p data-id="5ab1f10a1ef34ff5c59546964654bf27">Even if the message queue push fails, the message isn’t lost. It can still be persisted in the database.</p>
<p data-id="d3a0c63f09e514a031a4a3178e069906">When the user refreshes his home page you can write a query where he can poll the database for new updates. Take the polling approach, we discussed initially, as a backup.</p>
<p data-id="94c3c2f9ace376b8b83eb9721515b4d7">Or you can totally rollback the transaction, even if the database persistence transaction is a success but the message queue push transaction fails. The post still hasn’t gone into the database yet as it is generally a two-phase commit. We can always write custom distributed transaction code or leverage the distributed transaction managers which the frameworks offer.</p>
<p data-id="4b3dc635d75eb3d61f1254e775da0837">I can go on and on about it, till the minutest of the details. But it would just make the lesson unnecessarily lengthy. For now, I have just touched the surface, to help you understand how notification systems &amp; real-time feeds work.</p>
<p data-id="df582997e4be668a308b850a99525e57">Just like the post creation process, the same process or the flow repeats itself when the users trigger events like visiting a public place, eating at a restaurant etc. And the message queues push the events to the connections of the user.</p>
<p data-id="1d935909c28099b6b15a29f2d791e243">When designing scalable systems, I would want to assert this fact that there is no perfect or best solution. The solution should serve us well, fulfil our business requirements. Optimization is an evolutionary process, so don’t sweat about it in the initial development cycles.</p>
<p data-id="9b5c78831c83e6f29f25be3838c5494a">First, get the skeleton in place and then start optimizing notch by notch.</p>
<p data-id="f213f848f813cc7aeab8aa03bad29bb1">Recommended read - <a href="https://www.8bitmen.com/linkedin-real-time-architecture-how-does-linkedin-identify-its-users-online/" target="_blank">How Does LinkedIn Identify Its Users Online?</a></p>
</div></div></div></div></div></div></div></div></div>