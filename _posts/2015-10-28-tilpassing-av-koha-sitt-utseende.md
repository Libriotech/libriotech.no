---
layout: post
title: Tilpassing av Koha sitt utseende
created: 1446023842
categories:
- nyheter
- koha
---
<p>Koha er et fleksibelt system, som i stor grad kan tilpasses behovene til det enkelt bibliotek ved hjelp av systempreferanser, og uten at man endrer selve koden til Koha. Dette gjelder også utseendet på særlig publikumskatalogen. Her kommer noen tips for de som vil komme i gang med å tilpasse Koha.</p>
<p>Innledningsvis kan vi skille mellom noen ulike former for tilpasning:</p>
<ul>
<li>Det finnes diverse funksjoner som kan skrus av og på. Eksempler på dette kan være tagger, kommentarer og stjerner i publikumskatalogen. Denne introduksjonen kommer ikke til å ta for seg slike endringer. (Se feks <a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#impopac">OPAC Configuration</a> og <a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#impenhanced">Enhanced Content Configuration</a> i dokumentasjonen for detaljer.)</li>
<li>Særlig på forsiden av publikumskatalogen finnes det felter der man kan  legge inn egen HTML-formatert tekst og lenker.</li>
<li>Eksisterende elementer i grensesnittet kan fjernes eller endres med teknikker som CSS og JavaScript.</li>
</ul>
<!--break-->
<h2>Din egen HTML</h2>
<p>Koha sin publikumskatalog har en rekke steder der det er mulig å legge inn egne HTML-koder. Dette kan være feks tekst, bilder eller lenker. Den beste måten å å oversikt over mulighetene på er ved å se på avsnittet <a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#editableopac">Editable OPAC Regions</a> i Koha sin dokumentasjon. Her finnes det et bilde som viser hvor de redigerbare områdene befinner seg og hva den aktuelle systempreferansen heter.</p>
<ul>
<li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#opacheader">opacheader</a></li>
<li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#OpacNav">OpacNav</a></li>
<li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#OpacNavBottom">OpacNavBottom</a></li>
<li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#OpacMainUserBlock">OpacMainUserBlock</a></li>
<li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#OpacNavRight">OpacNavRight</a></li>
<li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#opaccredits">opaccredits</a></li>
</ul>
<p>Opp til og med Koha versjon 3.20 må man selv skrive inn HTML-koder i en tekst-boks for å redigere disse systempreferansene. Fra og med versjon 3.22 vil det bli mulig å bruke en innebygget editor (se <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=11584">Bug 11584</a>).</p>
<h2>CSS</h2>
<p>CSS er en uunnværlig del av moderne HTML-standarder, som gjør det mulig å spesifisere hvordan HTML skal se ut. Se <a href="https://no.wikipedia.org/wiki/Cascading_Style_Sheets">Cascading Style Sheets</a> i Wikipedia for en introduksjon.</p>
<p>Koha kommer med et antall CSS stilark, som definerer standard utseende på systemet. Men det er fullt mulig å legge til egen CSS, som i stor eller liten grad endrer utseendet på systemet. De viktigste systemprefransene som gjør dette mulig er:</p>
<ul>
<li>Publikumskatalog
    <ul>
    <li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#OPACUserCSS">OPACUserCSS</a></li>
    <li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#opaclayoutstylesheet">opaclayoutstylesheet</a></li>
    <li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#OpacAdditionalStylesheet">OpacAdditionalStylesheet</a></li>
    </ul>
</li>
<li>Internt grensesnitt</li>
    <ul>
    <li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#IntranetUserCSS">IntranetUserCSS</a></li>
    <li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#intranetstylesheet">intranetstylesheet</a></li>
    <li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#intranetcolorstylesheet">intranetcolorstylesheet</a></li>
    </ul>
</li>
</ul>
<p>Av disse er OPACUserCSS og IntranetUserCSS helt klart de som er enklest å bruke, siden de bare krever at man limer CSS-koder inn i en tekstboks i Koha sitt grensesnitt. De øvrige krever at man har egne filer med CSS i.</p>
<p>Se <a href="http://wiki.koha-community.org/wiki/HTML_%26_CSS_Library">HTML & CSS Library</a> i Koha sin wiki for noen tips.</p>
<h2>JavaScript</h2>
<p>JavaScript er et fullverdig programmeringsspråk. Se <a href="https://no.wikipedia.org/wiki/JavaScript">JavaScript</a> i Wikipedia for en kort introduksjon. Koha inkluderer et JavaScript-bibliotek som heter <a href="https://jquery.com/">jQuery</a>, som gjør det enkelt å manipulere elementer på en HTML-side programmatisk.</p>
<p>I likhet med CSS kommer Koha med mye ferdig JavaScript, men det er også mulig å legge til egen kode. Systemprefranser som legger til rette for dette er:</p>
<ul>
<li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#opacuserjs">opacuserjs</a> - for publikumskatalogen</li>
<li><a href="http://translate.koha-community.org/manual/3.20/en/html-desktop/#intranetuserjs">intranetuserjs</a> - for det interne grensesnittet</li>
</ul>
<p>Også her er det mulig å skrive JavaScript-kode direkte inn i tekst-bokser i Koha sitt grensesnitt.</p>
<p>Se <a href="http://wiki.koha-community.org/wiki/JQuery_Library">jQuery Library</a> i Koha sin wiki for et stort antall eksempler på hvordan JavaScript og jQuery an brukes for å endre Koha sitt grensesnitt.</p>
<h2>Flere ressurser:</h2>
<ul>
<li><a href="http://www.myacpl.org/koha/">Koha Blog</a> - av Owen Leonard, som er den som har hatt mest å si for hvordan Koha ser ut i dag. Masse nyttige tips for den som vil tilpasse Koha sitt utseende.</li>
<li><a href="http://wiki.koha-community.org/wiki/Gallery_of_customized_OPACs">Gallery of customized OPACs</a> - for inspirasjon</li>
</ul>
