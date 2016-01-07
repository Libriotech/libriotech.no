---
layout: post
title: NORMARC og eksempeldata for Koha
created: 1301477664
categories:
- koha
---
<p>Under arbeidet med å få på plass støtte for NORMARC i <a href="http://koha-community.org/">Koha</a> gikk det etter hvert opp for meg at det også trengtes et sett med eksempeldata for å gjøre det mulig å gjennomføre en komplett installasjon på norsk. Dette arbeidet har tatt mye tid i det siste, men er nå endelig sendt inn til vurdering for inkludering i versjon 3.4:</p>
<ul>
<li>NORMARC - <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=3644">Bug 3644</a> - <a href="https://github.com/MagnusEnger/kohawork/tree/bug3644-normarc">GitHub</a> - <a href="http://lists.koha-community.org/pipermail/koha-patches/2011-March/014340.html">Request to pull</a></li>
<li>Eksempeldata - <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=6002">Bug 6002</a> - <a href="https://github.com/MagnusEnger/kohawork/tree/bug6002-sample-data">GitHub</a> - <a href="http://lists.koha-community.org/pipermail/koha-patches/2011-March/014341.html">Request to pull</a></li>
</ul>
<p>Arbeidet er ikke komplett, det mangler for eksempel XSLT-filer for den interne delen av Koha og eksempel-bibliotek og -lånere er ikke tilpasset norske forhold enda. Men forhåpentligvis er det en god start å bygge videre på. Så er det bare å krysse fingrene for at dette blir funnet verdig for innlemming i versjon 3.4...</p>
<p>Jeg har satt opp en (midlertidig) demo av koden, der poster katalogiseres og indekseres som NORMARC, og der alle eksempeldata er lastet inn:</p>
<ul>
<li><a href="http://kohanor33.bibkat.no/">OPAC</a></li>
<li><a href="http://kohanor33.bibkat.no:8080/">Internt</a> (logg på med brukernavn = demo og passord = demo)</li>
</ul>
<p>Spørsmål eller rapporter om feil og mangler kan rettes til <a href="http://libriotech.no/om">undertegnede</a>.</p>
