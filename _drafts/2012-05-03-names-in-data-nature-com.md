---
layout: post
title: Names in data.nature.com
created: 1336074853
categories: []
---
<p>So I thought I'd take <a href="http://data.nature.com/">data.nature.com</a> for a spin and look for things written by Richard Dawkins.

<pre class='brush: plain'>
select ?doi ?title ?pubdate ?genre where { 
  ?doi <http://ns.nature.com/terms/hasContributor> ?o .
  ?o <http://xmlns.com/foaf/0.1/name> 'Richard Dawkins' .
  ?doi <http://purl.org/dc/elements/1.1/title> ?title ;
    <http://prismstandard.org/namespaces/basic/2.1/genre> ?genre ;
    <http://prismstandard.org/namespaces/basic/2.1/publicationDate> ?pubdate .
} 
</pre>
