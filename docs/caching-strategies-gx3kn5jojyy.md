---
id: caching-strategies-gx3kn5jojyy
title: Caching Strategies
sidebar_label: Caching Strategies
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss some of the commonly used caching strategies.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li>
<ul>
<li><a href="#cache-aside">Cache Aside</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#read-through">Read-Through</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#write-through">Write-Through</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li>
<ul>
<li><a href="#write-back">Write-Back</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="2a64d4ceadd90ade823526a423b0b77a">There are different kinds of caching strategies which serve specific use cases. Those are <em>Cache Aside</em>, <em>Read-through cache</em>, <em>Write-through cache</em> &amp; <em>Write-back cache</em></p>
<p data-id="3fb3d5f449cc9b2e8bf477e86eb6f7c5">Let’s find out what they are &amp; why do we need different strategies when implementing caching.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="cache-aside" data-id="6bca99288e55db7f836b08a19947b5ac">Cache Aside <a class="markdownIt-Anchor" href="#cache-aside"><span class="anchor-link">#</span></a></h3>
<p data-id="30c6251b68ec048479d7c51c9bb590e9">This is the most common caching strategy. In this approach, the cache works along with the database trying to reduce the hits on it as much as possible.</p>
<p data-id="321c8bb786b9682971e80d64c7429d28">The data is <em>lazy-loaded</em> in the cache.
When the user sends a request for particular data, the system first looks for it in the cache. If present, then it is simply returned from it. If not, the data is fetched from the database, the cache is updated and is returned to the user.</p>
<p data-id="9726d2700c9ea756e51d28b244a992bc">This kind of strategy works best with <em>read-heavy</em> workloads. This includes the kind of data which is not much frequently updated, for instance, user profile data in a portal. User’s name, account number etc.</p>
<p data-id="2adc158fa49b7348794e8c13710c13d2">The data in this strategy is written directly to the database. This means that the data present in the cache and the database could get inconsistent. To avoid this data on the cache has a TTL “Time to Live”. After that stipulated period the data is invalidated from the cache.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="read-through" data-id="c312fdf9f1dd65033fd1e6cd1a242a5a">Read-Through <a class="markdownIt-Anchor" href="#read-through"><span class="anchor-link">#</span></a></h3>
<p data-id="fc5c749f0179507d76ebd5977ed5ee2e">This strategy is pretty similar to the <em>Cache Aside</em> strategy. A subtle difference from the <em>Cache Aside</em> strategy is that in the <em>Read-through</em> strategy, the cache always stays consistent with the database.</p>
<p data-id="a3a4540b32eddbde7d871498c632443f">The cache library or the framework takes the onus of maintaining the consistency with the backend;
The information in this strategy too is <em>lazy-loaded</em> in the cache, only when the user requests it.</p>
<p data-id="559b495bc64840a1cd60fbea87669aac">So, for the first time when information is requested, it results in a cache miss. Then the backend has to update the cache while returning the response to the user.</p>
<p data-id="345260af187f03bcfce60f1134309881">However, the developers can always pre-load the cache with the information which is expected to be requested most by the users.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="write-through" data-id="2c4ec1f66e15abff9eaa99636e3bd474">Write-Through <a class="markdownIt-Anchor" href="#write-through"><span class="anchor-link">#</span></a></h3>
<p data-id="46a655105220eefbb33a091fe19f4947">In this strategy, each &amp; every information written to the database goes through the cache. Before the data is written to the DB, the cache is updated with it.</p>
<p data-id="0bff810fc7bc97f9c6de184314d2cafb">This maintains high consistency between the cache and the database though it adds a little latency during the write operations as data is to be updated in the cache additionally. This works well for write-heavy workloads like online massive multiplayer games.</p>
<p data-id="c1d30eff62b12ee5cd3ad6e0ff4b7976">This strategy is generally used with other caching strategies to achieve optimized performance.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h3 id="write-back" data-id="9213ad8d51120b8c390300f361f3e5cb">Write-Back <a class="markdownIt-Anchor" href="#write-back"><span class="anchor-link">#</span></a></h3>
<p data-id="f2afbaf95fb096590d7dfc57f7d79998">This strategy helps optimize costs significantly.
In the <em>Write-back</em> caching strategy the data is directly written to the cache instead of the database. And the cache after some delay as per the business logic writes data to the database.</p>
<p data-id="2c5c8ec923f4531f7d8951d2c8a21054">If there are quite a heavy number of writes in the application. Developers can reduce the frequency of database writes to cut down the load &amp; the associated costs.</p>
<p data-id="6d418e2bde99379c0bce16cc2b390ded">This is the strategy which I talked about in the previous lesson.</p>
<p data-id="8244c633ca438bc378dc71c8f3050028">A risk in this approach is if the cache fails before the DB is updated, the data might get lost. Again, this strategy is used with other caching strategies to make the most out of these.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="5b3b5ec49081118257f958ac5c9e3e03">Guys!! With this, we are done with the caching mechanism of web applications. Now let’s move on to the world of message queues.</p>
</div></div></div></div></div></div></div></div></div>