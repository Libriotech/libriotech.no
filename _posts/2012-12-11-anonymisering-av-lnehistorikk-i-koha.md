---
layout: post
title: Anonymisering av lånehistorikk i Koha
created: 1355220108
categories:
- koha
---
<p>Standardinnstillingen i Koha er at lånehistorikk tas vare på, noe som ikke er i tråd med norske lover og regler. For å være innenfor lovverket må en av to ting gjøres:</p>

<h3>Forberedelser</h3>

<p>Uavhengig av hvilken løsning man velger må systempreferansen <a href="http://manual.koha-community.org/3.10/en/administration.html#AnonymousPatron">AnonymousPatron</a> fylles med lånernummeret (dvs "borrowernumber", ikke kortnummer eller strekkode) til en fiktiv låner. Ved anonymisering vil de faktiske lånernummerne bli byttet ut med nummeret fra denne systempreferansen, slik at det ikke lenger blir mulig å spore et lån tilbake til en konkret låner, samtidig som det er mulig å ta ut statistikk på hva som ble lånt når osv.</p>

<h3>Manuell løsning</h3>

<p>I det interne grensesnittet kan man gå til Hjem › Verktøy › Lånere (anonymiser, masseslett) og anonymisere lånehistorikk som er eldre enn en gitt dato:</p>

<p><img src="/files/2012/anon1.png" alt="Anonymisering av lånehistorikk i det interne grensesnittet" /></p>

<p>Du vil få et sammandrag av de endringene du er i ferd med å gjøre før du faktisk fullfører endringene:</p>

<p><img src="/files/2012/anon2.png" alt="Bekrefting av anonymisering av lånehistorikk i det interne grensesnittet" /></p>

<p>Dokumentasjon: <a href="http://manual.koha-community.org/3.10/en/tools.html#anonpatrons">1.6. Patrons (anonymize, bulk-delete)</a>.</p>

<p>Å gjøre dette manuelt med jevne mellomrom er lite hensiktmessig, og de fleste vil derfor ønske å bruke den automatiske løsningen:</p>

<h3>Autmatisk løsning</h3>

<p>Denne løsningen er basert på et skript som kjøres på serveren der Koha er installert, nemlig misc/cronjobs/batch_anonymise.pl. Dokumntasjonen for dette skriptet ser ut som følger:

<pre>
Usage: misc/cronjobs/batch_anonymise.pl  --days DAYS  [-h|--help]
   --days DAYS        (MANDATORY) anonymise patron history that is older than DAYS days.
   -v --verbose       gives a little more information
   -h --help          prints this help message, and exits, ignoring all
                      other options
</pre>

Det er altså mulig å kjøre dette skriptet slik, for å anonymisere lån som ble levert inn for mer enn 2 dager siden:

<pre>misc/cronjobs/batch_anonymise.pl --days 2</pre>

<p>Typisk bruk av dette skriptet vil være å kjøre det fra <a href="http://en.wikipedia.org/wiki/Cron">cron</a> (eller tilsvarende) hver natt. Libriotech tilbyr denne løsningen til sine kunder, som en del av standard oppsettet av Koha.</p>

<h3>La lånerne bestemme</h3>

<p>Paralellt med løsningene ovenfor kan man la lånerne selv bestemme hvordan lånehistorikken deres skal behandles. Dette styres med systempreferansen <a href="http://manual.koha-community.org/3.10/en/administration.html#OPACPrivacy">OPACPrivacy</a>. Som standard er denne slått av, men slås den på (samtidig som systempreferansen <a href="http://manual.koha-community.org/3.10/en/administration.html#opacuserlogin">opacuserlogin</a> er slått på og brukerne faktisk har brukernavn/passord til publikumskatalogen) vil lånerne få se en ekstra fane når de logger seg på i publikumskatalogen:</p>

<p><a href="/files/2012/anon3.png" title="Klikk for full størrelse"><img height="275" width="437" src="/files/2012/anon3.png" alt="Skjermbilde i publikumskatalogen for innstillinger knyttet til lånehistorikk" /></a></p>

<p>Oversettelsen av denne siden er kanskje ikke helt gjennomarbeidet, men det det koker ned til er at lånerne får tre valg:

<ul>
<li>0 - Ubegrenset = Lånehistorikken bevares uavhengig av hva biblioteket gjør for å anonymisere gamle lån, dvs at denne innstillingen overstyrer både den manuelle og den automatiske løsningen som er beskrevet ovenfor.</li>
<li>1 - Standardvalg = Lånehistorikk anonymiseres når biblioteket utfører manuell eller automatisk anonymisering. Dette er standardvalget og det er foreløpig ikke mulig å endre hva som skal være standard for nye lånere.</li>
<li>2 - Aldri = Lånehistorikken anonymiseres ved innlevering.</li>
</ul>

<p>Det er kun lånerne selv som kan endre denne innstilingen i publikumskatalogen - den kan ikke endres av bibliotekets personale gjennom det interne grensesnittet.</p>

<p>Lånerne kan også selv velge å klikke på "Umiddelbar sletting", for å slette lånehistorikken der og da, uavhengig av valg biblioteket eller låneren ellers har gjort.</p>

<h3>Utviklingsmuligheter</h3>

<ul>
<li>Det foreligger et forslag om å gjøre det mulig å velge standard innstilling for lånehistorikk basert på låntagerkategorier: <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=6254">Bug 6254 - can't set patron privacy by default</a></li>
<li> Den innstillingen som er foreslått her vil neppe være i tråd med norske lover og regler: <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=9011">Bug 9011 - Add the ability to store the last patron to return an item</a></li>
<li>Sletting av enkelte titler fra historikken: <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=9230">Bug 9230 - selectively delete reading history</a></li>
</ul>
