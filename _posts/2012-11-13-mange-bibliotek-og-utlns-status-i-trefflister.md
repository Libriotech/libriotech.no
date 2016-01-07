---
layout: post
title: Mange bibliotek og utlåns-status i trefflister
created: 1352820522
categories: []
---
<p>Her er et spørsmpl som dukket opp under "Bli kjent med Koha"-dagen i forrige uke:</p>

<p>Spørsmål: Hvis mange bibliotek/filialer deler den samme Koha-installasjonen, hvordan vil da informasjonen om utlånt-status se ut i trefflistene i publikumskatalogen?</p>

<p>Svar: Det vil vises som en lang streng med informasjon om alle bibliotekene. Se <a href="http://catalog.nexpresslibrary.org/cgi-bin/koha/opac-search.pl?q=twilight">eksempler fra NExpess-katalogen</a></p>

<p>Jeg har lagt inn en bug (nærmere bestemt en "enhancement request") som forslår å gjøre det mulig å endre dette, slik at bare antallet ledige eksemplarer vises, og ikke navnene på alle bibliotekene: <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=9028">Bug 9028 - Optionally show only the number of available copies in result lists in OPAC</a>. Et eldre forslag som også vil påvirke dette er <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=5079">Bug 5079 - Make display of shelving location and call number in XSLT results controlled by sysprefs</a>, som foreslår å gjøre det valgfritt om plassering og hyllesignatur skal vises i trefflista. Kanskje får jeg tid til å gjøre noe med det etter hvert, om ikke noen føler seg kallet til å sponse utviklingen...</p>
