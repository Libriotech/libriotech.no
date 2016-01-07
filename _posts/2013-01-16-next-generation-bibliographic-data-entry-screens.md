---
layout: post
title: Next generation bibliographic data entry screens
created: 1358321852
categories:
- semantikoha
---
<p>Here's a <a href="http://listserv.loc.gov/cgi-bin/wa?A2=ind1301&L=bibframe&T=0&P=6953">message</a> I sent to the <a href="">BIBFRAME</a> email list last night:</p>

<blockquote>

<p>On 15 January 2013 19:13, Tom Morris <[log in to unmask]> wrote:<br />
> One good path forward here might be the open source library software<br />
> systems.  Someone could prototype the data entry screen of the future<br />
> in a real-live system.</p>

<p>Thanks for bringing that up, I have been thinking along the same lines
myself for some time now. I am involved in the Koha community, and I
have been thinking specifically about adding "semantic capabilities"
to that ILS.</p>

<p>Specifically I have been thinking about:</p>

<ul>
<li>Getting records out of Koha with OAI-PMH and transforming them to
RDF, using the marc2rdf software [1]</li>
<li>Storing the RDF in a triplestore</li>
<li>Creating interfaces for enhancing and supplementing the transformed
data in the triplestore (by describing relationships between the
records, pulling in data from other sources etc etc)</li>
<li>Enhancing the OPAC with the data from the triplestore. (I think this
step is important - this shouldn't just be about creating "data entry
screens", but about how we can make the ILS and the OPAC a good
platform for mediation and a more useful tool both for librarians and
patrons.)</li>
</ul>

<p>My hypothesis is that once we start to see all the wonderful and cool
and useful things we can do with the semantic data we will one day
"wake up" and wonder why we ever bothered with MARC. ;-)</p>

<p>I actually have a half baked demo of the scenario described above
available [2]. Sadly the interface for working with the semantic data
here are command line scripts... ;-) I do hope to turn this into a
proper project with a proper interface and get it integrated into
Koha, though. The only problem is time/money... Maybe I'll team up
with some adventurous library and apply for a grant or maybe I'll
start a Kickstarter [3] campaign to raise money for it. Or both. Not
because I think I have the perfect idea for what the interfaces should
look like, mind you, but just to get the ball rolling and start the
evolution towards something useful.</p>

<p>The way forward? I think free software can be key, in that it allows
us to experiment and test things in real systems. I think the way to
do it is with "rough concensus and running code", and to iterate and
iterate and iterate, throwing away the bad ideas and holding on to the
good ones. And I think that goes *both* for creating the interfaces
and for figuring out what exactly should replace MARC...</p>

<p>Best regards,<br />
Magnus Enger<br />
libriotech.no</p>

<p>[1] <a href="https://github.com/digibib/marc2rdf">https://github.com/digibib/marc2rdf</a> - this is a project based at
the Oslo public library and they have recently got funding from the
Norwegian national library to develop it further.</p>

<p>[2] <a href="http://semantikoha.libriotech.no/">http://semantikoha.libriotech.no/</a> - a couple of examples:<br />
<a href="http://semantikoha.libriotech.no/cgi-bin/koha/opac-view.pl?uri=http://esme.priv.bibkat.no/records/id_108">http://semantikoha.libriotech.no/cgi-bin/koha/opac-view.pl?uri=http://esme.priv.bibkat.no/records/id_108</a><br />
<a href="http://semantikoha.libriotech.no/cgi-bin/koha/opac-view.pl?uri=http://data.deichman.no/person/darwin_charles">http://semantikoha.libriotech.no/cgi-bin/koha/opac-view.pl?uri=http://data.deichman.no/person/darwin_charles</a><br />
There is a somewhat old RFC for Linked Data in Koha here, outlining
some more ideas:<br />
<a href="http://wiki.koha-community.org/wiki/Linked_Data_RFC">http://wiki.koha-community.org/wiki/Linked_Data_RFC</a><br />
I hope to add some more ideas here in the not too distant future:<br />
<a href="http://libriotech.no/blogs/semantikoha/">http://libriotech.no/blogs/semantikoha/</a></p>

<p>[3] Well actually not Kickstarter, since that is limited to US and UK
residents, but something similar, at least.</p>

</blockquote>
