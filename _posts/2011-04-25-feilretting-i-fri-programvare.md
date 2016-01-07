---
layout: post
title: Feilretting i fri programvare
created: 1303754422
categories:
- koha
---
<p>Hvordan fungerer egentlig fri programvare? Hvordan blir feil funnet og rettet opp? Her er et eksempel fra <a href="http://koha-community.org/">Koha</a>, som utspant seg i dag, 2. påskedag. Tidspunktene til venstre er lenket til <a href="http://stats.workbuffer.org/irclog/koha/">loggen</a> fra Koha sin <a href="http://koha-community.org/get-involved/irc/">IRC-kanal</a>:</p>
<ul>
<li><a href="http://stats.workbuffer.org/irclog/koha/2011-04-25#i_652811">15.49</a>: library_systems_guy lurer på om det er noe galt med "shelf-browseren" i Koha</li>
<li><a href="http://stats.workbuffer.org/irclog/koha/2011-04-25#i_652840">16.07</a>: nengard tester og bekrefter at det er et problem</li>
<li><a href="http://stats.workbuffer.org/irclog/koha/2011-04-25#i_652845">16.08</a>: nengard har registrert <a href="http://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=6263">Bug 6263 - shelf browser doesn't work in 3.4</a> i Bugzilla, systemet Koha bruker for å holde rede på feil og utbedringsforslag</li>
<li><a href="http://stats.workbuffer.org/irclog/koha/2011-04-25#i_652851">16.21</a>: cait rapporterer at hun har funnet en løsning på problemet</li>
<li><a href="http://stats.workbuffer.org/irclog/koha/2011-04-25#i_652864">16.30</a>: cait har lastet opp <a href="http://bugs.koha-community.org/bugzilla3/attachment.cgi?id=3998">løsningen</a> (en "patch") til Bugzilla</li>
<li><a href="http://stats.workbuffer.org/irclog/koha/2011-04-25#i_652867">16.33</a>: nengard har testet cait sin løsning og notert at den fungerer i Bugzilla (dette kalles en "sign off")</li>
</ul>
<p>Tid fra første rapport om problemet til løsningen er funnet og testet: 44 minutter. Det er også verdt å notere seg at cait befinner seg i Europa og de to andre medvirkende i USA. Det som gjenstår nå er å vente på at Koha sin Release Manager, som befinner seg på New Zealand, skal våkne og innlemme løsningen på problemet i den offisielle versjonen av Koha. Når det er gjort vil Release Maintainer'en for Koha 3.4.x sørge for at løsningen kommer med også i denne vedlikeholds-"grenen" av Koha, der neste offisielle versjon kommer 22. mai.</p>
<p>Nå skal jeg ikke påstå at alle problemer i Koha blir løst like fort som dette, men det er et slående eksempel på hva internasjonalt samarbeid og tilgang til kildekoden kan utrette!</p>
