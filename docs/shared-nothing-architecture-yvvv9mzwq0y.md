---
id: shared-nothing-architecture-yvvv9mzwq0y
title: Shared Nothing Architecture
sidebar_label: Shared Nothing Architecture
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will briefly discuss the Shared Nothing Architecture.</p></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="3cbb88ed2dc64d6fcda0fef43802d403">When working with distributed systems, you’ll hear this term <em>Shared Nothing Architecture</em> often. I thought I’ll just quickly discuss it with you, though there is nothing really unique about this. I’ve already talked about it in the course.</p>
<p data-id="8327b60affddabc9c3a1808ded149fbb">When several modules work in conjunction with each other. They often share <em>RAM</em>, also known as the shared memory. They share the disk, that is sharing the database. And then they share nothing. The architecture of the system where the modules or the services sharing nothing is called the <em>Shared Nothing Architecture</em>.</p>
<blockquote data-id="46c65416862da4d442674966b5761902">
<p><em>Shared Nothing Architecture</em> means eliminating all single points of failure. Every module has its own memory, own disk. So even if several modules in the system go down, the other modules online stay unaffected. It also helps with the <em>scalability</em> and <em>performance</em>.</p>
</blockquote>
<p data-id="9a6911a2c9a00893ba6d112ee1452934">Moving on!! let’s discuss the Hexagonal Architecture in the next lesson.</p>
</div></div></div></div></div></div></div></div></div>