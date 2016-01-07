---
layout: post
title: Koha, NORMARC og autoritetsposter
created: 1352981617
categories:
- nyheter
- koha
---
<p>Da jeg gjorde hoveddelen av arbeidet med å implementere NORMARC i Koha var jeg nok usikker på hva jeg skulle gjøre med autoritetene, siden Koha er bygget opp rundt egne MARC-rammeverk for dette, noe NORMARC p.t. mangler. Utfallet ble at arbeidet med autoriteter for NORMARC ble utsatt på ubestemt tid. Dette ble jeg minnet om under "Bli kjent med Koha"-dagen i forrige uke, så nå er tiden inne for å gjøre noe med det.</p>

<p>Løsningen blir så vidt jeg kan se å bruke MARC21 sine rammeverk for autoriteter, slik at funksjonaliteten for autoriteter i NORMARC blir identisk med den man finner i MARC21. Jeg er i gang med dette arbeidet nå, og håper det skal være relativt fort gjort.</p>

<p>I mellomtiden er det altså mulig å studere autoritetsfunksjonene i MARC21, for å få et inntrykk av hvordan det vil fungere for NORMARC, når jobben med å få det på plass er gjort.</p>
<!--break-->
<h2>Demo</h2>

<p>Jeg har satt opp en ny demo-installasjon av Koha med MARC21 og rimelige innstillinger for autoriteter. Denne installasjonen kjører versjon 3.9.x (som ligger tett opp til det som blir til 3.10.0 når denne versjonen er klar 23. november), for å få med alt som er nytt når det gjelder autoriteter.</p>

<ul>
<li>OPAC: <a href="http://marc21.testing.bibkat.no/">http://marc21.testing.bibkat.no/</a></li>
<li>Internt: <a href="http://marc21.testing.bibkat.no:8080/">http://marc21.testing.bibkat.no:8080/</a> logg inn med brukernavn = demo og passord = demo.</li>
</ul>

<h2>Screencast</h2>

<p>Her er en screencast som veldig enkelt viser hvordan man legger til en autoritetspost for en person, og så bruker denne bosten ved katalogisering av en bok:</p>

<p><a href="http://bywatersolutions.com/2012/09/26/cataloging-with-authorities-in-koha-3-8/">Cataloging with Authorities in Koha 3.8</a></p>

<h2>Eksempler</h2>

<p>Jeg har laget et bittelite hierarki med geografiske emneord:</p>

<pre>
Norge
|------Buskerud
       |-----------Drammen
       |-----------Kongsberg
</pre>

<p>Se "Drammen" <a href="http://marc21.testing.bibkat.no/cgi-bin/koha/opac-authoritiesdetail.pl?authid=625062">i OPACen</a> og <a href="http://marc21.testing.bibkat.no:8080/cgi-bin/koha/authorities/detail.pl?authid=625062">i det interne grensesnittet</a> for å se hvordan dette tar seg ut.</p>

<p>For geografiske emneord er hierarkiet basert på "lenker"/henvisninger mellom emneordene i feltet 551. For eksempel: I autoritetsposten for <a href="http://marc21.testing.bibkat.no:8080/cgi-bin/koha/authorities/detail.pl?authid=625062">Drammen</a> ligger det en henvisning til Buskerud som "broader term" i 551 (klikk på "5"-fanen for å se detaljene i den forrige lenka), mens for <a href="http://marc21.testing.bibkat.no:8080/cgi-bin/koha/authorities/detail.pl?authid=624908">Buskerud</a> ligger det en henvisning til Drammen som "narrower term" i 551.</p>

<h3>Legge til et nytt emneord</h3>

<p>Se screencasten her: <a href="http://div.libriotech.no/kohacast/3.10/autoriteter-legge-til-hierarkisk/">http://div.libriotech.no/kohacast/3.10/autoriteter-legge-til-hierarkisk/</a></p>

<h2>Dokumentasjon</h2>

<p>Det har skjedd en del forbedringer i støtten for autoriteter, som kommer med i versjon 3.10, men som ikke er i versjon 3.8. Nedenfor lenker jeg derfor til dokumentasjonen for 3.10 (som er under arbeid).</p>

<ul>
<li><a href="http://manual.koha-community.org/3.10/en/administration.html#authprefs">1.3. Authorities</a> - syspeminnstillingene som påvirker hvordan autoriteter vises og oppfører seg</li>
<li><a href="http://manual.koha-community.org/3.10/en/catadmin.html#authoritiesadmin">4.5. Authority Types</a> - muligheten for å definere nye autoritetstyper ut over de som er definert som standard i Koha</li>
<li><a href="http://manual.koha-community.org/3.10/en/catauthorities.html">3. Authorities</a> - hvordan legge til, søke etter og redigere autoriteter</li>
<li><a href="http://manual.koha-community.org/3.10/en/impauthorities.html">7. Authorities Configuration</a> - mer om konfigurasjon av autoriteter</li>
<li><a href="http://manual.koha-community.org/3.10/en/catalogtools.html#stagemarc">2.7. Stage MARC Records for Import</a> - MARC21 autoritetsposter kan importeres via web-grensesnittet, på samme måte som bibliografiske poster. Dersom det er store mengder poster som skal importeres bør dette gjøres direkte på serveren, ikke gjennom grensesnittet.</li> 
</ul>

<h2>MeSH</h2>

<p>MeSH i MARC21-format er tilgjenglig for <a href="http://www.nlm.nih.gov/mesh/marc.html">nedlasting</a>. Bruken er fri, men man må registrere seg for å få laste ned dataene. Jeg har lastet inn de mer enn 600.000 autoritetspostene i Koha-installasjonen det er lenker til ovenfor, slik at man kan se hvordan disse vil fungere i praksis.</p>

<p>Se for eksempel "Common cold" i <a href="http://marc21.testing.bibkat.no/cgi-bin/koha/opac-authoritiesdetail.pl?authid=72012">publikumskatalogen</a> og i <a href="http://marc21.testing.bibkat.no:8080/cgi-bin/koha/authorities/detail.pl?authid=72012">det interne grensesnittet</a>.</p>

<h2>VIAF</h2>

<p>Det finnes en JavaScript-snutt som det skal være mulig å legge inn i systempreferansen "intranetuserjs" for å slå opp navn i VIAF, men det ser ikke ut som denne uten videre fungerer i nyere versjoner av Koha.</p>

<ul>
<li><a href="http://koha-community.org/koha-newsletter-volume-3-issue-6-june-2012/#viaf">Adding VIAF Autosuggest for New NAME Authorities by Stefano Bargioni</a> - omtale i Koha Newsletter</li>
<li><a href="">Add VIAF autosuggest for new NAME authorities</a> - JavaScript-snutten som er tilgjengelig fra Koha sin wiki</li>
</ul>
