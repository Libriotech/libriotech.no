---
layout: post
title: Innhøsting av global statistikk fra Koha
created: 1422353318
categories:
- nyheter
- koha 3.18
---
<p>Fra og med Koha versjon 3.18.0 er det mulig å slå på (anonym) rapportering av statstikk om Koha-installasjonen din ved hjelp av systempreferansene som begynner på UsageStats*. Dataene samles og rapporteres på <a href="http://hea.koha-community.org/">hea.koha-community.org</a>.</p>

<p>Planen med dette er todelt:</p>

<ul>
<li>Å dokumentere bruken av Koha over hele verden. Man får feks ofte høre at Koha er et "lite" system som egner seg for "små" bibliotek. Med data fra Hea kan vi dokumentere at det er alle slags bibliotek som bruker Koha. Det hadde også vært kjekt å kunne se for hvor mange poster, eksemplarer og lånere Koha er med på å administrere.</li>
<li>Systemet teller også hvilke innstillinger som er i bruk for en del systempreferanser. Dette vil kunne bidra til å gi utviklerne innblikk i hvordan Koha brukes og hvilke "features" som er mye eller lite brukt.</li>
</ul>

<p>Deltagelse i denne innhøstingen av statstikk er selvsagt frivillig, og man må aktivt skru den på for å bidra.</p>

<p><a href="http://wiki.koha-community.org/wiki/KohaUsageStat_RFC">Dokumentasjon på Koha sin wiki</a>.</p>

<p>Relevante systempreferanser:</p>

<ul><li><a href="http://manual.koha-community.org/3.18/en/administration.html#UsageStats">UsageStats</a></li>
<li><a href="http://manual.koha-community.org/3.18/en/administration.html#UsageStatsCountry">UsageStatsCountry</a></li>
<li>UsageStatsID</li>
<li>UsageStatsLastUpdateTime</li>
<li><a href="http://manual.koha-community.org/3.18/en/administration.html#UsageStatsLibraryName">UsageStatsLibraryName</a></li>
<li><a href="http://manual.koha-community.org/3.18/en/administration.html#UsageStatsLibraryType">UsageStatsLibraryType</a> (med Koha 3.18.3 kommer det flere valgmuligheter her, jfr <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=13436">bug 13436</a>)</li>
<li><a href="http://manual.koha-community.org/3.18/en/administration.html#UsageStatsLibraryUrl">UsageStatsLibraryUrl</a></li>
</ul>
