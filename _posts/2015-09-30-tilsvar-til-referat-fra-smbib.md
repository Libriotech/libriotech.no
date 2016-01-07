---
layout: post
title: Tilsvar til referat fra Småbib
created: 1443609217
categories:
- koha
---
<p><a href="https://sites.google.com/site/smaabib/">Forum for bibliotekarer i små fagbibliotek (Småbib)</a> hadde nylig et møte hos STAMI (som er et ferskt Koha-bibliotek og kunde hos Libriotech). På hjemmesiden til Småbib ligger det et <a href="https://sites.google.com/site/smaabib/home/moetereferater-1/moeter-2015/moete-15-09-2015">referat</a> fra møtet, som kan være verdt noen kommentarer:</p>
<blockquote><p>Overgang til Koha ved STAMI ble presentert av vertskapet. Koha er et gratis biblioteksystem som bygger på Open Source, altså åpen kildekode, og kan installeres på egen server eller kjøres på server hos den norske kontakten, Libriotech ved Magnus Enger.</p></blockquote>
<p>Libriotech er ikke "den norske kontakten" for Koha. Koha er som det sies fri programvare, som hvem som helst kan ta i bruk, både bibliotek og firma. Foreløpig er Libriotech den eneste leverandøren i Norden, men det er ingen ting i veien for flere selskaper kan tilby de samme tjenestene som det Libriotech gjør, i det samme markedet. Internasjonalt finnes det et 50-talls firmaer som tilbyr tjenester i tilknytning til Koha. Det finnes ingen form for godkjenning av disse, og ingen offisiell status som leverandør for et gitt område.</p>
<blockquote><p>Ved STAMI tok de konverteringen i sommer og har gode erfaringer med det. Det som for tiden mangler er en modul for fjernlån, men den vil bli tilpasset den nye internasjonale standarden for fjernlån, NCIP, som skal avløse NILL-standarden.</p></blockquote>
<p>Det stemmer at den sær-norske NILL-standarden for fjernlån skal erstattes av den internasjonale NCIP-standarden. Det engelske Koha-firmaet PTFS Europe jobber for tiden med å utvikle en fjernlånsmodul for Koha, og Libriotech jobber med å tilpasse denne til NCIP (eller norsk NCIP-profil, NNCIPP, for å være helt nøyaktig) og norske forhold.</p>
<blockquote><p>Flere mindre bibliotek og enkeltsamlinger bruker Koha i dag, men det mest omtalte akkurat nå er Deichmans prosjekt. Ulempene for vanlige brukere er at utviklingen av systemet er dugnadsbasert, det kan derfor ta tid med oppgraderinger.</p></blockquote>
<p>Det stemmer at utviklingen av Koha skjer på dugnad, og at det derfor kan være vanskelig å forutsi når en gitt ny funksjon kommer seg gjennom Koha sine systemer for kvalitetskontroll og inn i en offisiell versjon. Men Koha har nå i mange år kommet med svært regelmessige oppdateringer: Nye vedlikeholdsversjoner (som kun inneholder feilrettinger) den 22. i hver måned. Nye hovedversjoner (som inneholder feilrettinger og nye funksjoner) 22. mai og 22. november hvert år. Libritoech sine kunder oppgraderes til vedlikeholdsversjonene fortløpende og til de nye hovedversjonene etter hvert som det blir klart at disse er klare for å settes i drift.</p>
<blockquote><p>Kjøres systemet på ekstern server (Libriotech), er man også avhengig av Magnus Engers tid til support.</p></blockquote>
<p>Sant nok. Det har vært et beklagelig etterslep fordi undertegnede hadde en 80% stilling hos Deichmanske bibliotek i 2014. Dette medførte at flere større prosjekter hopet seg opp, og det har tatt tid å få tatt disse unna. Dette er endelig i ferd med å løse seg opp, og responstidene på support skal nå bli bedre. Et langsigktig mål er at Libriotech skal kunne utvide med flere ansatte, noe som vil avhjelpe situasjonen ytterligere. Forhåpentligvis kan ansatt nummer 2 være på plass i løpet av 2016.</p>
<blockquote><p>Kjører man det selv er LINUX et krav. STAMI framhever at prisen for drift er lavere enn med Mikromarc, som de har forlatt. Koha er også enkelt håndterbart og selvinstruerende. Særlig framheves katalogiseringen som enkel. Grensesnittet slik det ble vist er enkelt og oversiktlig. Mer spissfindige spørsmål viste nok at "grunnversjonen" kanskje vil ha svakheter i visse sammenhenger [...]</p></blockquote>
<p>Jeg vil veldig gjerne vite hva disse "spissfindige spørsmålene" handlet om!</p>
<blockquote><p>og at prosjektet Deichman nå har i gang, bekrefter at en lokal tilpassing av systemet i større drift er nødvendig.</p></blockquote>
<p>Her er det flere ting å gripe fatt i:</p>
<p>Det aller viktigste er at tilpasninger av Koha bare er en liten del av det utviklingsarbeidet som nå gjøres ved Deichmanske bibliotek. Det er verdt å merke
seg at Deichmanske hovedsakelig kommer til å bruke Koha til sirkulasjon av fysiske objekter, dvs registrering av lånere, lån, utsending av purringer osv.</p>
<p>Katalogisering vil skje i form av RDF og Linked Data, noe som i seg selv er banebrytende, for ikke å si revolusjonerende, og utvikling av grensesnitt og "katalogiseringsregler" for dette utgjør en stor del av utviklingsprosjektet. RDF-dataene vil bli "redusert" til MARC-poster, slik at Koha har noe å "tygge på", som et grunnlag for sirkulasjon. Grensesnittene mot publikum vil være basert på RDF-dataene, og Deichmanske vil ikke bruke Koha sin publikumskatalog i det hele tatt. Arbeidet med katalogisering i RDF er et nybrottsarbeid, også i internasjonal sammenheng.</p>
<p>Når dette er sagt så stemmer det også at Deichmanske gjør en del tilpasninger i Koha. Men disse er først og fremst knyttet til kommunikasjon med eksterne systemer. Det kan være RFID-lesere, eller kommunikasjon med eksterne tjenester som kemner (i forbindelse med gebyrer og andre krav) og Posten (for utsending av purringer osv). Jeg tviler på at det er mange norske bibliotek (og særlig mindre fagbibliotek) som har et antall integrasjoner mellom biblioteksystem og eksterne tjenester som kan måle seg med det Deichmanske har. Men motbevis meg gjerne! :-)</p>
<p>Det som er viktig å få frem her er at den betydelige utviklingsinnsatsen Deichmanske nå legger ned ikke først og fremst handler om nødvendige tilpasninger for å få Koha til å fungere i en norsk sammenheng, men om nybrottsarbeid som i liten grad berører Koha.</p>
<p>En del norske tilpasninger har allerede blitt en del av Koha: Oversettelser (det er for tiden bare oversettelsen til bokmål som vedlikeholdes aktivt), støtte for NORMARC, kommunikasjon med Nasjonalt lånekort, høsting til Biblioteksøk via OAI-PMH. Fjernlån basert på NNCIPP er som tidligere sagt under utvikling.</p>
<blockquote><p>Magnus Enger er da også engasjert i utviklingsarbeidet der.</p></blockquote>
<p>Jeg var som tidligere nevnt ansatt på Deichman i 2014, men dette engasjementet opphørte ved slutten av 2014.</p>