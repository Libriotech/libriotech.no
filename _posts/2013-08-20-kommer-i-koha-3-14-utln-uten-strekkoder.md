---
layout: post
title: 'Kommer i Koha 3.14: Utlån uten strekkoder'
created: 1376989190
categories: []
---
<p>Ikke alle bibliotek ønsker å investere i strekkoder til bøkene sine, men frem til nå har dette vært en nødvendighet for å kunne drive utlån i Koha. Det eneste tilgjengelige feltet når man skal låne ut har vært et for strekkode. Fra og med versjon 3.14 (som kommer 22. november) vil dette derimot endre seg. Da blir det mulig å slå på systempreferansen <a href="http://manual.koha-community.org/3.14/en/administration.html#itemBarcodeFallbackSearch">itemBarcodeFallbackSearch</a> og så vil Koha gjøre et søk etter nøkkelord, dersom systemet ikke finner en strekkode som matcher det man har skrevet inn i "utlånsfeltet":</p>

<p><img src="/files/2013/itemBarcodeFallbackSearch.png"/></p>

<p>Her ønsker jeg å låne ut boka "Code" av Lawrence Lessig, og har skrevet inn "code" i feltet for strekkode. Når jeg trykker "Enter" på tastaturet eller klikker på "Check Out" kommer det opp en melding om at strekkoden ikke ble funnet, og jeg får et forslag om å låne ut nettopp "Code".</p>

<p>(Det kan se ut som det er <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=10768">rom for forbedringer</a> i grensesittet knyttet til denne funksjonaliteten, men det viktigste er at selve funksjonen kommer på plass.)</p> 
