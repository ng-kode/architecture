---
id: reasons-for-system-failures-gk0wvggr78l
title: Reasons For System Failures
sidebar_label: Reasons For System Failures
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss the common reasons for system failure.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#software-crashes">Software Crashes</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#hardware-failures">Hardware Failures</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#human-errors">Human Errors</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#planned-downtime">Planned Downtime</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="18e19470a5f03eeb36909cb9ed366b2d">Before delving into the HA system design, fault-tolerance and redundancy. I’ll first talk about the common reasons why systems fail.</p>
<h2 id="software-crashes" data-id="a1d5620c27ec4e230fdb316d1eadce3f">Software Crashes <a class="markdownIt-Anchor" href="#software-crashes"><span class="anchor-link">#</span></a></h2>
<p data-id="72ba82f12e23ee0ce1e0ace1ea63188c">I am sure you are pretty familiar with software crashes. Applications crash all the time, be it on a mobile phone or a desktop.</p>
<p data-id="5286fbc4a518dc742d968c1f251d8ce1">Corrupt software files. Remember the BSOD blue screen of death in windows? OS crashing, memory-hogging unresponsive processes.  Likewise, software running on cloud nodes crash unpredictably, along with it they take down the entire node.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="hardware-failures" data-id="6ded70d5af0c6edd4ad5d230b8c95768">Hardware Failures <a class="markdownIt-Anchor" href="#hardware-failures"><span class="anchor-link">#</span></a></h2>
<p data-id="21201af871f68355486043f67f0c0575">Another reason for system failure is hardware crashes. Overloaded CPU, RAM, hard disk failures, nodes going down. Network outages.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="human-errors" data-id="a79a73f7c898c3191ba42c38252c2af2">Human Errors <a class="markdownIt-Anchor" href="#human-errors"><span class="anchor-link">#</span></a></h2>
<p data-id="8074cf21533525e55c085c3483b7e134">This is the biggest reason for system failures.
Flawed configurations &amp; stuff.</p>
<p data-id="c79f67d8aaa78add49a1e29cc6d396d0">Google made a tiny network configuration error &amp; it took down almost half of the internet in Japan. <a href="https://thenextweb.com/google/2017/08/28/google-japan-internet-blackout/" target="_blank">This is an interesting read</a>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="planned-downtime" data-id="5ce1122f34542694448a3df1b6548c36">Planned Downtime <a class="markdownIt-Anchor" href="#planned-downtime"><span class="anchor-link">#</span></a></h2>
<p data-id="87bfc4f1ca4f807f00c412df8d61b3fd">Besides the unplanned crashes, there are planned down times which involve routine maintenance operations, patching of software, hardware upgrades etc.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="9c28bc5af41f38cd027585ec02c9efc7">These are the primary reasons for system failures, now let’s talk about how HA systems are designed to overcome these scenarios of system downtime.</p>
</div></div></div></div></div></div></div></div></div>