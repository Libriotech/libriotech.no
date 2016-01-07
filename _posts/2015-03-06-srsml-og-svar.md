---
layout: post
title: Sørsmål og svar
created: 1425668812
categories:
- koha
---
<p>For en tid tilbake ble jeg stilt noen spørsmål om Koha. Her er svarene, under mottoet "bedre sent enn aldri":</p>

<p><strong>Autoritetsregister: Hvilke muligheter har man for å importere? Kan man operere med et felles autoritetsregister for folkebibliotek/samarbeidsbibliotek? Navn og emneord eks.</strong></p>

<p>Innledningsvis kan det være verdt å bemerke at Koha forholder seg til <a href="http://manual.koha-community.org/3.18/en/catauthorities.html">autoritetsposter</a> i MARC-format. NORMARC har ikke støtte for dette, men det ville være relativt enkelt å sette opp en NORMARC-basert katalog til å bruke MARC21-poster for autoritetene.</p>

<p>Det er mulig å <a href="http://manual.koha-community.org/3.18/en/catauthorities.html">importere autoritetsposter via Z39.50</a>. P.t. finnes det vel ikke noen kilder for norske autoritetsposter som er tilgjengelig via Z39.50. Men om flere bibliotek ønsket å samarbeide om et felles autoritetsregister kunne man se for seg at man satte opp en egen Koha-installasjon der alle de deltagene de bibliotekene samarbeidet om å vedlikeholde registeret, og at poster så ble overført til de enkelte bibliotekenes installasjoner, enten via Z39.50 eller ved at poster ble eksportert (til fil) fra "autoritets-installasjonen" og så importert i de ulike lokale installasjonene.</p>

<p><strong>Kan man endre admininnstillinger for bare filial og ikke alle bibliotekene? (Eks ikke fuzzy query i publikumskatalogen?)</strong></p>

<p>Nei, systempreferansene er globale.</p>

<p><strong>Vi trenger å få treff i sambok/samsøk/tilsvarende i z39.50-søk. Hva skal til for å få opp igjen dette?</strong></p>

<p>Dette er vel tjenester som er på vei ut, til fordel for Biblioteksøk. Generelt sett kan Koha importere poster fra alle kilder som er tilgjengelig via Z39.50 eller SRU. Den beste kilden for å hente poster er BIBSYS, som også omfatter Nasjonalbiblioteket sine samlinger.</p>

<p><strong>Mulighet for å søke på dewey i publikumskatalogen - gjøre dewey klikkbart i trefflisten.</strong></p>

<p>Å legge til flere indekser i nedtrekksmenyen til venstre for søkeboksen kan man få til ved hjelp av en liten JavaScript-snutt: <a href="http://wiki.koha-community.org/wiki/JQuery_Library#Add_additional_searches_to_OPAC">Add additional searches to OPAC</a>.</p>

<p>Å gjøre Dewey klikkbar kan sannsynligvis også oppnås med litt JavaScript. Ellers må man lage spesialtilpassede XSLT-stilark, noe som slettes ikke er umulig. Eller man kan argumentere for at dette bør være standard i Koha, og endre de standard stilarkene, slik at alle andre også drar nytte av denne endringen.</p>

<p><strong>Er det mulig å få opp søkehistorikk? </strong></p>

<p><a href="http://manual.koha-community.org/3.18/en/opacmyaccount.html#opacmysearchistory">Ja</a>.</p>

<p><strong>Pin-mulighet ved store bibliotek - mange lånere med samme navn, har en pinkode ved glemt lånekort for å sikre at det er rett låntaker (eks Stavanger)</strong></p>

<p>Koha har selvsagt mulighet for å gi brukerne passord, og det er ikke noe i veien for å bruke en PIN-kode som passord. Men Koha har p.t. ikke muligheter for å sjekke at det bare er PIN-koder som legges inn som passord. På den annen side er jo PIN-koder elendinge passord...</p>

<p><strong>Savnede felt fra Normarc - eks 096 599 691 etc. Kan man få inn felter? Hvordan går man frem for å ta vare på funksjonalitet man har i gammel katalog via bruk av disse feltene?</strong></p>

<p>Alle de feltene som nevnes er lokale felter, dvs at NORMARC har satt av plass til dem, men ikke definert hva de skal brukes til. Det er det nok de ulike norske biblioteksystemene og -leverandørene som har gjort. Hvert enkelt bibliotek kan definere nye MARC-felter i Koha sine rammeverk etter behov, så å kunne lagre data i disse feltene er ikke noe problem. For å vise dataene i katalogen må man gjøre tilpasninger i XSLT stilark. Jeg er skeptisk til om Koha bør adpotere sær-felter fra andre systemer, men er gjerne med på å diskutere det. :-)</p>
