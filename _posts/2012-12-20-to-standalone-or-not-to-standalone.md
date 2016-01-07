---
layout: post
title: To standalone or not to standalone
created: 1356018532
categories:
- semantikoha
---
<p>So this blog did not get off to a flying start (mainly due to a lack of time, of course, which has also kept me from actually working on SemantiKoha), but hey look, here is another post!</p>

<p>One of the the things I have been mulling over while I have been unable to actually work on SemantiKoha is the question of whether what I want to do is best done as a standalone "application" or as something tightly integrated into <a href="http://koha-community.org/">Koha</a>. Here's what I'm thinking:</p>

<h2>Background</h2>

<p>So, the basic question is "What do I want to do?"</p>

<p>The answer isn't that hard: I want to create a public interface for a library catalogue, that is not based on MARC data, but on MARC data transformed into Linked Data/RDF and supplemented/enhanced by new kinds of data in the same format.</p>

<p>The basic layout of the system will have 

<ul>
<li>MARC records retrieved from the ILS via OAI-PMH</li>
<li><a href="https://github.com/digibib/marc2rdf">transformed</a> to Linked Data/RDF</li>
<li>stored in a triplestore, and</li>
<li>queried in response to end user actions (searching and browsing).</li>
</ul>

<p>(And yes, I do include a step for retrieving MARC records from the ILS. Sure, we could build something that does not involve MARC right now, but would any libraries start using it? I doubt it. I think the only way to move forward is to let libraries and librarians keep their MARC for a bit longer, so we can show them the potential in Linked Data/RDF, and then, when they see how cumbersome and unfit-for-purpose MARC really is, we can also show them that we can throw that part of the system away, and just keep the Linked Data/RDF bits. That's my hypothesis, anyway.)</p>

<p>So what is the best way to do that? Here are the two extremes on the continuum of possible answers to that question: standalone or tightly integrated.</p>

<h2>Standalone</h2>

<p>This would work similar to solutions like <a href="http://vufind.org/">VuFind</a> and <a href="http://projectblacklight.org/">Blacklight</a> and <a href="http://www.extensiblecatalog.org/">XC</a>.</p>

<h3>Pros</h3>

<ul>
<li>The project will benefit all kinds of libraries, not just the ones using Koha. This will also mean attracting more developers, not just developers interested in Koha.</li>
</ul>

<h3>Cons</h3>

<ul>
<li>To be a full replacement for an existing OPAC, there will need to be integration with the existing ILS, for doing things like
  <ul>
  <li>real time availability information for physical items</li>
  <li>current loans, renewals etc</li>
  </ul> There will probably have to be plugins for different ILSes or at least for different protocols (Z39.50, SRU, ILS-DI, any system-specific protocols). 
</li>
</ul>

<h2>Tightly integrated (into Koha)</h2>

<h3>Pros</h3>

<ul>
<li>Information like real time availability can be fetched directly, not from an API</li>
<li>No need to worry about re-implementing things like renewals, that's already in place in Koha</li>
<li>It would give Koha a "unique selling point" (Yes, I do love Koha and I want it to thrive, and I think more libraries switching to Koha is a good thing)
</ul>

<h3>Cons</h3>

<ul>
<li>It would only benefit libraries using Koha, and probably only attract developers interested in Koha</li>
</ul>

<h2>Middle ground</h2>

<p>The middle ground would be to integrate the new functionality tightly into Koha, but keep the central parts of it clearly separated from other parts of Koha (e.g. as one or more Perl modules that do not rely on other Koha modules), so that other projects could reuse those parts with a minimum of extra effort.</p>

<h2>Conclusion</h2>

<p>None, yet. But if you have opinions or advice, I'm all ears (also on <a href="https://plus.google.com/109768226438090618815/posts/h5625V9VkDQ">Google+</a> and <a href="https://twitter.com/libriotech/status/281788844817412096">Twitter</a>)!</p>
