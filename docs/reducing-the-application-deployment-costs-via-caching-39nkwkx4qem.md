---
id: reducing-the-application-deployment-costs-via-caching-39nkwkx4qem
title: Reducing the Application Deployment Costs Via Caching
sidebar_label: Reducing the Application Deployment Costs Via Caching
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss a real-world example of how the deployment cost of an application can be reduced by using a cache.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#real-life-use-case">Real Life Use Case</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#conclusion">Conclusion</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-life-use-case" data-id="3d00863f4fd5c47b900d45a728299b7f">Real Life Use Case <a class="markdownIt-Anchor" href="#real-life-use-case"><span class="anchor-link">#</span></a></h2>
<p data-id="fe92b52d6044ae49d30210b8b153183f">In this lesson, I am going to share an insight from a stock market-based gaming app that I developed and deployed on the cloud.</p>
<p data-id="33264825c45c1da7e949cd6ced71011b">The game had several stocks of companies listed on the stock market and the algorithm would trigger the price movement of the stocks every second, if not before that.</p>
<p data-id="5c5f94eacb2cc7f7da47b5c97ef05500">Initially, I persisted the updated prices of the stocks in the database as soon as the prices changed, to create a stock price movement timeline at the end of the day. But so many database writes cost me a fortune. The number of writes every hour was just crazy.</p>
<p data-id="b2cddbed0a9b54653102f327eaf60b8b">Eventually, I decided to not persist the updated price every second in the database rather use <em>Memcache</em> to persist the stock prices. And then run a batch operation at regular intervals to update the database.</p>
<p data-id="9c534e5f0c599579160b8c9e4432e974"><em>Memcache</em> was comparatively a lot cheaper than the disk-based database access. The cache served all the stock price requests, &amp; the database did not have the updated values until the batch operation ran.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="conclusion" data-id="7b60c55327cebd578968d1ed3b5dd77e">Conclusion <a class="markdownIt-Anchor" href="#conclusion"><span class="anchor-link">#</span></a></h2>
<p data-id="e3bf083928fd471376b30d563bd6f6c1">This tweak may not be ideal for a real-life Fintech app but it helped me save a truck-load of money &amp; I was able to run the game for a longer period of time.</p>
<p data-id="8f802cabdd9ae8ff2a29626145b8f482">So, Guys!! This is one instance where you can leverage the caching mechanism to cut down costs. You might not want to persist each and every information in the database rather use cache to store not so mission-critical information.</p>
<p data-id="2a3588f8ff0e7f70afc81e1d140e1f49">Now let’s look into some of the caching strategies we can leverage to further enhance the performance of our apps.</p>
</div></div></div></div></div></div></div></div></div>