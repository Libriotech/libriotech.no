---
layout: post
title: LOADing data from GeoNames
created: 1337066668
categories:
- semantikoha
---
<p>Let's say I have a book about <a href="http://en.wikipedia.org/wiki/Kapiti_Island">Kapiti Island</a> in my collection, and I want to express this aboutness in a Semantic Web way. One source I could relate to would of course be DBpedia but another interesting one is <a href="http://www.geonames.org/">GeoNames</a>. Here's the drill:</p>

<p>1. Do a search for <a href="http://www.geonames.org/search.html?q=kapiti&country=">kapiti</a> in GeoNames.</p>

<p>2. Find <a href="http://www.geonames.org/maps/google_-40.867_174.9.html">Kapiti Island</a> in the result list</p>

<p>3. Click on the red marker for Kapiti Island in the list below the map, and see that "GeoNameId : 2189083"</p>

<p>4. Read about the <a href="http://www.geonames.org/ontology/documentation.html">Geonames Ontology</a> and figure out that the URI for Kapiti Island should look like this:</p>

<pre>
http://sws.geonames.org/2189083/
</pre>

<p>5. Construct and run the appropriate (for Virtuoso) LOAD in the triplestore:</p>

<pre>
LOAD &lt;http://sws.geonames.org/2189083/&gt; INTO &lt;http://sws.geonames.org/2189083/&gt;
</pre>

<p>6. <a href="http://data.libriotech.no:8890/sparql/?default-graph-uri=&should-sponge=&query=SELECT+*+WHERE+{+GRAPH+%3Chttp%3A%2F%2Fsws.geonames.org%2F2189083%2F%3E+{+%3Fs+%3Fp+%3Fo+.+}+}+&format=text%2Fhtml&debug=on&timeout=">Et voila!</a></p>

<p>(And keep in mind that GeoNames data is licensed as CC-BY...)</p>
