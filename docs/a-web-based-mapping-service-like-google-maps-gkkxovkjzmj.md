---
id: a-web-based-mapping-service-like-google-maps-gkkxovkjzmj
title: A Web-based Mapping Service Like Google Maps
sidebar_label: A Web-based Mapping Service Like Google Maps
---

<div class="PageSummary__TopLeft-sc-19qsvz4-36 fwauBw"><p class="PageSummary__Description-sc-19qsvz4-13 cPWwbw">In this lesson, we will discuss a case study of a web-based mapping service like Google Maps.</p><div class="PageSummary__Toc-sc-19qsvz4-39 gUDsJM"><details open="" class="styles__PageTOCStyled-rf9d2l-0 jgnDfg"><summary role="button" tabindex="0" class="styles__HeadingWrap-rf9d2l-1 jpKLlP">We'll cover the following<div rotate="0" color="black" size="24" display="inline-flex" name="icon-button" class="styles__IconButton-sc-12pjl04-0 bLjBRS"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="18 15 12 9 6 15"></polyline></svg></div></summary><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 dZltoR" role="none"><ul>
<li>
<ul>
<li><a href="#a-little-background-on-google-maps">A Little Background On Google Maps</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#read-heavy-application">Read-Heavy Application</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#data-type-spatial">Data Type: Spatial</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#database">Database</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#architecture">Architecture</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#backend-technology">Backend Technology</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#monolith-vs-microservice">Monolith Vs Microservice</a>
<ul>
<li><a href="#apis">APIs</a></li>
</ul>
</li>
</ul>
</li>
<li>
<ul>
<li><a href="#server-side-rendering-of-map-tiles">Server-Side Rendering Of Map Tiles</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#user-interface">User Interface</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#real-time-features">Real-time Features</a></li>
</ul>
</li>
</ul>
</div></div></details></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="a3c38f476cab5cd038cbd5bfb17248d5">Before I begin talking about the architecture of the service, I would like to state that this is not a system design lesson, as it doesn’t contain any of the database design, traffic estimations or code of any sort.</p>
<p data-id="a0de5096b39312e580ca9047c276c3f2">I will just discuss the basic architectural aspects of the service and how do the concepts we’ve learned in the course apply here.</p>
<p data-id="6743fd8e86181243e8b0aa7340ae28d2">Let’s get on with it.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="a-little-background-on-google-maps" data-id="2b42b8d77654ee174ad4efb3d41ded8a">A Little Background On Google Maps <a class="markdownIt-Anchor" href="#a-little-background-on-google-maps"><span class="anchor-link">#</span></a></h2>
<p data-id="a66dfddd21e9dababfcd2347d21bf560"><em><a href="https://cloud.google.com/maps-platform/" target="_blank">Google Maps</a></em> is a web-based mapping service by <em>Google</em>. If offers satellite imagery, route planning features, real-time traffic conditions, an API for writing map-based games like <em>Pokemon Go</em> &amp; several other features.</p>
<p data-id="3bb21076266543ecbb531a2bea2c6cc0">First up, these massive successful services are a result of years of evolution and iterative development. Online services are built feature by feature and take years to perfect. <em>Google Maps</em> started as a desktop-based software written in <em>C++</em> &amp; evolved over the years to become what it is today. A beautiful mapping service used by over a billion users.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="read-heavy-application" data-id="68723848008b5e571a9412377b09c904">Read-Heavy Application <a class="markdownIt-Anchor" href="#read-heavy-application"><span class="anchor-link">#</span></a></h2>
<p data-id="2f96968fc349b52cc9c32eb53b9405a3">Let’s get down to the technicalities of it. An application like this is <em>read-heavy</em> &amp; not <em>write-heavy</em>. As the end-users aren’t generating new content in the application over time. Users do perform some write operations though it is negligible in comparison to a write-heavy application like <em>Twitter</em> or <em>Instagram</em>.
This means the data can be largely cached and there will be significantly less load on the database.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="data-type-spatial" data-id="1054faeb056650d79337fde61e87bde2">Data Type: Spatial <a class="markdownIt-Anchor" href="#data-type-spatial"><span class="anchor-link">#</span></a></h2>
<p data-id="89813cd7e8d9e84b2355351ec6064923">Speaking of the data, a mapping application like this has <em>spatial data</em>. <em>Spatial data</em> is the data with objects representing geometric information like points, lines, polygons. The data also contains alphanumeric stuff like <em><a href="https://en.wikipedia.org/wiki/Geohash" target="_blank">Geohash</a></em>, latitudes, longitudes, <em>GIS Geographical Information System</em> data etc.</p>
<p data-id="71455d46ebf80cb7bdf9771cfbcff123">There are dedicated <em>spatial databases</em> available for persisting this kind of data. Also, popular databases like <em>MySQL</em>, <em><a href="https://docs.mongodb.com/manual/core/geospatial-indexes/" target="_blank">MongoDB</a></em>, <em><a href="https://github.com/couchbase/geocouch/" target="_blank">CouchDB</a></em>, <em>Neo4J</em>, <em><a href="https://github.com/EverythingMe/geodis" target="_blank">Redis</a></em>, <em><a href="https://cloud.google.com/bigquery/docs/gis-intro" target="_blank">Google Big Query GIS</a></em> also support persistence of <em>spatial data</em>. They have additional plugins built for it.</p>
<p data-id="f4ae601fcb98d6565c00fcb0979b22de">If you want to read more about Spatial databases. <a href="https://en.wikipedia.org/wiki/Spatial_database" target="_blank">This is a good read</a>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="database" data-id="77b118cce6c1c03a436ac621c802ae98">Database <a class="markdownIt-Anchor" href="#database"><span class="anchor-link">#</span></a></h2>
<p data-id="df886a934d0c74c0411bba1e7e83935f">The coordinates of the places are persisted in the database and when the user runs a search for a specific location the co-ordinates are fetched from the database &amp; the numbers are converted into a map image.</p>
<p data-id="692275e99db261a82e05673efdab75b5">We can expect the surge in traffic on the service during the peak office hours, during festivals or major events in the city. We need dynamic <em>horizontal scalability</em>, to manage the traffic spikes. The app needs to be <em>elastic</em> to scale up and down on the fly.</p>
<p data-id="3da3eeb49a82034bcb0adcb7c0cb2154">As I brought this up earlier, we have the option of picking from multiple databases as both <em>relational</em> and <em>non-relational</em> support persistence of <em>spatial data</em>. I will be more inclined to pick a <em>non-relational NoSQL</em> one as the map data doesn’t contain many relationships. It’s a direct fetch of the co-ordinates &amp; the processing of them based on the user request. Also, a <em>NoSQL</em> database is inherently <em>horizontally scalable</em>.</p>
<p data-id="30cf2c20d310992f4b99f412b981c7f1">Though, we can scale well with a <em>relational database</em> too with <em>caching</em> as the application is read-heavy. But in <em>real-time</em> use cases with a lot of updates, it will be a bit of a challenge.</p>
<p data-id="75bf3af80844982809a65204c9ceca24"><em>Real-time</em> features like <em>LIVE</em> traffic patterns, information on congested routes, the suggestion of alternative routes as we drive in real-time etc. are pretty popular with the users of <em>Google Maps</em>.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="architecture" data-id="79f6472b555855dfe2403a20cb660d11">Architecture <a class="markdownIt-Anchor" href="#architecture"><span class="anchor-link">#</span></a></h2>
<p data-id="25669f739a5b86d837100758480a852c">Naturally, to set up a service like this we will pick a <em>client-server</em> architecture as we need control over the service. Else we could have thought about the <em>P2P</em> architecture.
But <em>P2P</em> won’t do us any good here.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="backend-technology" data-id="df5c37480ffa42a427a710fc5595d964">Backend Technology <a class="markdownIt-Anchor" href="#backend-technology"><span class="anchor-link">#</span></a></h2>
<p data-id="8d014e13e251c52358a625560ab376d3">Speaking of the server-side language we can pick <em>Java</em>, <em>Scala</em>, <em>Python</em>, <em>Go</em>. Any of the mature backend technology stack will do. My personal pick will be <em>Java</em>, since it is performant, heavily used for writing scalable distributed systems, as well as for the enterprise development.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="monolith-vs-microservice" data-id="d37ab6d1e84e565c11bf26f692067c76">Monolith Vs Microservice <a class="markdownIt-Anchor" href="#monolith-vs-microservice"><span class="anchor-link">#</span></a></h2>
<p data-id="e33f44c608b7661e03aee3a4c0834dfe">Speaking of <em>monolithic architecture</em> vs <em>microservice</em>, which one do you think we should pick for writing the app?</p>
<p data-id="8ed315a8bb0066ef7ec40ca1b318ae50">Let’s figure this out by going through the features of the service. The core feature is the map search. The service also enables us to plan our routes based on different modes of travel, by car, walking, cycling etc.</p>
<p data-id="55a1cb98d58a6dc4b8ef21328f71cebb">Once our trip starts, the map offers alternative route locations in real-time. The service adjusts the map based on the user’s real-time location &amp; the destination.</p>
<h3 id="apis" data-id="96365b5fe0a052c0262048938a78a261">APIs <a class="markdownIt-Anchor" href="#apis"><span class="anchor-link">#</span></a></h3>
<p data-id="86f8a9884fd89606b6902e639c39fd67">For the third-party developers, <em>Google</em> offers different <em>APIs</em> such as the <em>Direction API</em>, <em>Distance Matrix</em>, <em>Geocoding</em>, <em>Places</em>, <em>Roads</em>, <em>Elevation</em>, <em>Time zone</em>, <em>Custom search API</em>.</p>
<p data-id="5fbd873951ce3ddf426807aedcc2da7b">The <em>Distance matrix API</em> tells us how much time will it take to reach a destination depending on the mode of travel walking, flying, driving. <em>Real-time</em> alternative routes are displayed with the help of predictive modelling based on machine learning algorithms. The <em>Geocoding API</em> is about converting numbers into actual places &amp; vice versa.</p>
<p data-id="3a69ee4085651b2af5144662dfbe5861"><em>Google Maps</em> also has a <em>Gaming API</em> for building map-based games.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5062370525184000_image_5239449292111872.jpeg" alt=""></p>
<p data-id="b7d3e4e9dcc37a4e6f67fca8470c0a72">Though we may not have to implement everything in the first release. But this gives us a clue that a <em>monolithic architecture</em> is totally out of the picture.</p>
<p data-id="09760ac2273329c5f5566177b3a1d5d7">We need <em>microservices</em> to implement so many different functionalities. Write a separate service for every feature. This is a cleaner approach, helps the service scale and stay highly available. If a few services like real-time traffic, elevation API etc. go down, the core search remains unaffected.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="server-side-rendering-of-map-tiles" data-id="c3e161c6119a754f417d96de278f8c0d">Server-Side Rendering Of Map Tiles <a class="markdownIt-Anchor" href="#server-side-rendering-of-map-tiles"><span class="anchor-link">#</span></a></h2>
<p data-id="4d668688cf1a43d38fbe4596bd754085">Speaking of the core location search service, when the user searches for a specific location. The service has to match the search text with the name of the location in the database and pull up the coordinates of the place.</p>
<p data-id="ba126e792bdca554f646ec5c84246135">Once the service has the co-ordinates how do we convert those into an image? Also, should we render the image on the client or the server?</p>
<p data-id="76ccc84c4a07ea74eb7fe7e85f71e5a8"><em>Server-side rendering</em> is a preferable option in this scenario as we can cache the rendered image for future requests, as the image is kind of a static content &amp; will be same for all the users.</p>
<p data-id="06d1e4ddc861ab1fcaa602ff50d1419d">Also, as opposed to generating a single image of the map for the full web page, the entire map is broken down into tiles that enable the system to generate only the part of the map user engages with.</p>
<p data-id="cf6c5eddf79ed17c1f3797c3b5c23cc7">Smaller tiles help with the zoom in &amp; out operations. You might have noticed this when using <em>Google Maps</em>, that instead of the entire web page being refreshed, the map is refreshed in sections or tiles. Rendering the entire map instead of tiles every time would be very resource-intensive.</p>
<p data-id="abb9aec44469132de73b211e0a47fb85">We can create the map in advance by rendering it on the server &amp; caching the tiles. Also, we need a dedicated map server to render the tiles on the backend.</p>
<p data-id="d41d8cd98f00b204e9800998ecf8427e"><img src="assets/api_collection_6064040858091520_6411938009448448_page_5062370525184000_image_5101856206356480.jpeg" alt=""></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="user-interface" data-id="35b3e99244601321f151cf6e6b8d0473">User Interface <a class="markdownIt-Anchor" href="#user-interface"><span class="anchor-link">#</span></a></h2>
<p data-id="19db521765cff7f3225f5164ca90a1d9">Speaking of the <em>UI</em>, we can write that using <em>JavaScript</em>, <em>Html5</em>. Simple <em>JavaScript</em>, <em>Jquery</em> serves me well for simple requirements. But if you want to leverage a framework, you can look into <em>React</em>, <em>Angular</em> etc.</p>
<p data-id="0ab06749fd19d5fb1ff8a905426eefe3">The <em>UI</em> having <em>JavaScript</em> events enable the user to interact with the map, pin locations, search for places, draw markers and other vectors on the map etc.</p>
<p data-id="0b8e416a0f9143dd2a77f44a63a652a0"><em><a href="https://openlayers.org/" target="_blank">OpenLayers</a></em> is a popular open-source <em>UI</em> library for making maps work with web browsers. You can leverage it if you do not want to write everything from the ground up.</p>
<p data-id="c20f34857fa7dafb3b6219fe86dae8cb">Okay!! So, the user runs a search for a location, on the backend, the request is routed to the tile cache. The cache which has all the pre-generated tiles. It sits between the UI and the map server. If the requested tile is present in the cache it is sent to the UI. If not, the map server hits the database fetches the co-ordinates and related data &amp; generates the tile.</p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><h2 id="real-time-features" data-id="1c68bc2dd67a19458980d65e625f3a6f">Real-time Features <a class="markdownIt-Anchor" href="#real-time-features"><span class="anchor-link">#</span></a></h2>
<p data-id="4b629a3d6815f6b50adabaf0a3fcd339">Coming to the <em>real-time</em> features. To implement it we have to establish a <em>persistent connection</em> with the server. We’ve been through the <em>persistent connections</em> in detail in the course.</p>
<p data-id="efd53eb00e13cf37d9311695cbef56cb">Though <em>real-time</em> features are cool, they are very resource-intensive. There is a limit to the number of <em>concurrent connections</em>, servers can handle. So, I’ll advise implementing real-time features only when it’s really required.</p>
<p data-id="5c896f1365d3c0a7c60fa418f31e19e5">This is a good read on the topic, <a href="https://www.8bitmen.com/how-hotstar-scaled-with-10-3-million-concurrent-users-an-architectural-insight/" target="_blank">how Hotstar a video streaming service scaled with over 10 million concurrent users</a></p>
</div></div></div></div></div></div></div></div></div><div class="styles__ViewerComponentViewStyled-sc-1xosrua-0 cvzEyH"><div><div><div><div><div class=""><div class=""><div class="markdown-container-div"><div class="markdownViewer Markdown__Viewer-sc-7qtuee-1 zJKNA" role="none"><p data-id="bc9381c8648506e566dcfe9199eeeedf">Well, this is pretty much it on a web-based mapping service. We’ve covered the backend, database, caching and the UI &amp; a fundamental understanding of how a service like <em>Google Maps</em> works.</p>
<p data-id="a7c45581fffe6100b73661de5d5b4b3a">I’ll see you in the next lesson, where we will discuss a baseball game online ticket booking service.</p>
</div></div></div></div></div></div></div></div></div>