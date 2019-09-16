#### create a link within the same page
```
[[#topic 1]]

=== topic 1
```

#### create an External link
```
[[http://nos.nl|nieuws]]
```



#### dokuwikiw exchange ####

{{tag>dokuwiki }}

~~CLOSETOC~~

~~TOC:1-4~~

====== Gebruik van de DokuWiki ======

Deze pagina heeft ook een //[[#tag|tag]]// "werkinstructie" omdat vooral over het gebruik van DokuWiki gaat en niet over de [[installatie]] of configuratie van [[dokuwiki:installatie|animals]].


===== Begin =====
Als je nog nooit met Dokuwiki gewerkt hebt, bekijk dan eerst
  * de [[wiki:dokuwiki|Introductiepagina]]
  * het [[wiki:dokuwiki|overzicht]] met koppelingen naar diverse informatie
  * en de //[[wiki:syntax|Dokuwiki-syntax]]// voor het gebruik van de ingebouwde //editor//, er is ook een //[[https://www.dokuwiki.org/plugin:ckgedit|grafische editor]]// maar die kan niet met alle syntax van sommige plugins overweg!


===== Navigatie =====
  * **Pagina's openen:** Als je in de navigatiekolom de rechtermuisknop gebruikt krijg je een menu. Wil je gewoon een pagina openen in een nieuw tab blad gebruik dan **''Ctrl''** plus de linkermuisknop!
  * [[#tag|Tags]] gebruiken
  * Zie ook de [[#tips]] o.m. om snelkoppelingen te gebruiken om naar boven of een bepaald onderwerp op de pagina te springen, bijvoorbeeld:

[[dokuwiki:gebruik|Naar boven]]

===== Bewerken ======

==== Editor ====

De Dokuwiki komt standaard met een eenvoudige //editor// waarme tekst met //[[:wiki:syntax|DokuWiki opmaak-codes]]//kan worden ingevoerd. Alternatieven:

  * Hier onder staan tips voor het bewerken van de [[#tekst|tekst]] met met, bijvoorbeeld, ''vi''  of een //browser plugin//  als alternatief voor het venster in de browser (alleen van toepassing voor //[[:wiki:syntax|DokuWiki syntax]]//)
  * Als alternatief is de //WYSIWYG editor// [[https://www.dokuwiki.org/plugin:ckgedit|ckgedit]] beschikbaar (in de //Farmer versie//), die is standaard ingesteld en kan in een //Farm// configuratie niet standaard vervangen worden door DWedit, je moet dus zelf via ''Edit'' en ''DWedit'' je voorkeur in een ''cookie'' zetten als je ''DWedit'' wil!
      * Met deze editor kunnen de meest gebruikte tekst-eigenschappen grafisch worden ingesteld zoals:
        * Koppen (zie ook [[https://www.dokuwiki.org/plugin:ckgedit#short-cut_keys|toetsencombinaties]])
        * Teksteigenschappen zoals [[https://www.dokuwiki.org/plugin:ckgedit#short-cut_keys|vet, cursief en onderstreept]]
        * [[https://www.dokuwiki.org/plugin:ckgedit#footnotes|Voetnoten]]
        * Niet ondersteunde eigenschappen, met name notatie voor andere [[#extensies_voor_algemeen_gebruik|plugins]], zullen in (hun eigen) [[:wiki:syntax|opmaak-codes]] worden weergegeven.
  * **Editor kiezen:**
      * Gebruiers die een andere editor willen gebruiken:
        * Open een //edit sessie//  en klik de knop ''[[:wiki:syntax|[DW edit]]]'' // of ''[[https://www.dokuwiki.org/plugin:ckgedit|[CKG edit]]]''- dit sluit de sessie * Open een nieuwe //edit sessie met ''[Edit]''  en de gekozen //editor//  start
        * In de volgende sessies wordt de laatste gekozen editor gebruikt (zolang je dezelfde browser met bijbehorend //cookie//  gebruikt)
      * Gebruikers die permanent een andere editor willen zullen lid van een andere groep gebruikers moeten worden.

^  [[dokuwiki:gebruik|Terug naar boven]]   |

\\


==== Nieuwe pagina maken ====
Behalve door de URL te manipuleren kun je ook een menu invoegen om een nieuwe pagina ergens in de bestaande hierarchie aan te maken: ''[[https://www.dokuwiki.org/plugin:addnewpage|addnewpage]]'', zie [[:start#nieuwe_pagina_maken|startpagina]].

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

==== Illustraties invoegen ====
De plugin [[https://www.dokuwiki.org/plugin:imgpaste|imgpaste]] maakt het in <color red>**uitsluitend Chrome en Opera**</color> mogelijk om met **''Ctrl+V''** plaatjes rechtstreeks van het klembord in de Wiki-pagina die je bewerkt te plakken.

^  [[dokuwiki:gebruik|Terug naar boven]]  ^


===== Extensies voor algemeen gebruik =====
Een aantal van de beschikbare plugins en eventuele tips voor het gebruik er van.

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

==== Inhoudsopgaven, dynamisch gegenereerde koppelingen, .. ====
Een aantal plugins kan inhoudsopgaven of lijsten met koppelingen naar paginas dynamisch genereren.
=== Tag ===
Aangezien, bijvoorbeeld werkinstructies, in verschillende takken voorkomen is het handig om deze als zodanig te "markeren". Dat kan met een z.g.n. //[[https://www.dokuwiki.org/plugin:tag|tag]].//
  * **Gebruik:** 
    * Bij voorkeur **alleen enkelvoud**, dus "werkinstructie", ''uid'', .. enz (er is helaas al een uitzondering: {{tagpage>componenten}})
    * Zo min mogelijk samenstellingen van losse woorden, dus "proxy" i.p.v. "proxy server" (maar weer wel {{tagpage>"reverse proxy"}} omdat dat echt iets anders is).
      * Begrippen van meer dan een woord kunnen wel (tussen aanhalingstekens) maar verdienen dus niet de voorkeur

Markeer pagina's met een "[[https://www.dokuwiki.org/plugin:tag|tag]]" die gebruikt kan worden om pagina's met diezelfde tag bijelkaar te zoeken. 
  * Markeer de pagina door helemaal bovenaan, voor de titel, inhoudsopgave, .. een of meer //tags// toe te voegen, bij voorkeur enkele woorden of anders tussen aanhalingstekens:<code>
{{tag>wiki "linux wiki" dokuwiki}}
</code>Om meteen pagina's met dezelfde tag te vinden klik je er op na opslaan (rechtsbovenin).
  * Gebruik die informatie als volgt: Maak bijvoorbeeld een koppeling die - dynamisch - een overzicht genereert van alle pagina's met de //tags// <color green>''**wiki**''</color> of <color green>''**dokuwiki**''</color><code>{{tagpage>wiki dokuwiki&dynamic|Wiki-informatie}}\\</code> Het resultaat is de volgende link: {{tagpage>wiki dokuwiki&dynamic|Wiki-informatie}}

Zie voor alle gebruikte tags [[:tags|deze pagina]]

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

=== Gewijzigde pagina's ===
De plugin ''[[https://www.dokuwiki.org/plugin:changes|changes]]'' kan dynamisch een lijst van recente wijzigingen, al dan niet beperkt tot een bepaalde //name space//, genereren, bijvoorbeeld binnen "algemeen":
  {{changes>ns=algemeen}}

=== Flexibele inhoudsopgave ===
[[https://www.dokuwiki.org/plugin:toctweak|Toctweak]] levert een flexibele inhoudsopgave. Bijvoorbeeld, vervang de standaard inhoudsopgave door een (uitklapbare) inhoudsopgave van niveau 1 t/m 4:<code>
~~CLOSETOC~~

~~TOC:1-4~~
</code>

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

=== Indices ===
Met ''[[https://www.dokuwiki.org/plugin:nspages|nspages]]'' kun je indices van een deel van de wiki maken. Bijvoorbeeld, start-pagina met "Mooie naam" en alle sub-pagina's<code>
====== Mooie naam ======
<nspages -subns -h1 -simpleList -exclude:start -textPages="" -textNS="">
</code>

=== Nstoc ===
[[https://www.dokuwiki.org/plugin:nstoc|nstoc]]

=== Pagelist ===
[[https://www.dokuwiki.org/plugin:pagelist|pagelist]] 


==== Export ====

=== Exporteer als PDF ===
Hiervoor zijn twee plugins beschikbaar:
  * [[https://www.dokuwiki.org/plugin:bookcreator|bookcreator]]
  * [[https://www.dokuwiki.org/plugin:dw2pdf|dw2pdf]], bijvoorbeeld om deze pagina <nowiki>[[?do=export_pdf|als PDF af te drukken]]</nowiki>!

De laatste is te gebruiken door 
  * met de knop in de Dokuwiki-sjabloon //Arctic//
  * of door handmatig het volgende aan de pagina-URL toe te voegen: **''&do=export_pdf''**

/* Voor niet ondersteunde Dokuwiki-sjablonen:
  * of een speciale koppeling te maken, bijvoorbeeld [[#uitlijning|rechts uitgelijnd]]:<code>
;;#
[[?do=export_pdf|PDF export]]
;;#
</code>
*/

Het is niet erg snel en, mogelijk, geeft deze uitbreiding het ueberhaupt op met wat langere pagina's of //namespaces//, dus een geschikte browser om meteen als PDF af te drukken is vooral sneller en misschien ook betrouwbaarder.

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

==== Tekstweergave ====

=== Waarschuwingen, opmerkingen ===
Met de [[https://www.dokuwiki.org/plugin:note|note]] plugin kun je bijvoorbeeld mensen waarschuwen voor e.e.a.:<code>
<note warning>
Belangrijke mededeling!
</note></code>

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

=== Gekleurde tekst ===
Naast de mogelijkheden die HTML, de [[https://www.dokuwiki.org/wiki:syntax#text_to_image_conversions|wiki syntax]] en de diverse //"code tags"// bieden, zijn der de nodige plugins:
  * [[https://www.dokuwiki.org/plugin:color|Color]]: Markeer tekst in standaard [[https://www.dokuwiki.org/plugin:color|html-kleuren]]. Bijvoorbeeld: ''<nowiki><color red></nowiki><color red>**rode tekst**</color><nowiki></color></nowiki>''
  * [[https://www.dokuwiki.org/plugin:cellbg|Cell background]]: Zet voor je cel-tekst de gewenste kleur tussen **'''@'''** en **''':'''**, bijvoorbeeld **''@lightgreen:mijn tekst''**
  * [[https://www.dokuwiki.org/plugin:highlight|Highlight]]: Vergelijkbaar met ''color'': ''<nowiki><hi yellow></nowiki><hi yellow>**geel gemarkeerde tekst**</hi><nowiki></hi></nowiki>''

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

=== Commentaar en verborgen tekst ===
Als je bepaalde tekst niet wil weggooien maar ook niet wil tonen (bijvoorbeeld kladversies, achterhaalde tekst, lange uitvoer, ...) kun je die tussen C-stijl [[https://www.dokuwiki.org/plugin:comment|commentaar-tekens]]  zetten: **''<nowiki>/* ... */</nowiki>''**

Als je een deel van de pagina standaard wil verbergen maar wel oproepbaar will houden, gebruik dan ''[[https://www.dokuwiki.org/plugin:hidden|hidden]]''. Maak een stuk van de tekst "uitklapbaar" tussen - op nieuwe regels geplaatste - opening en afsluiting van het verborgen gedeelte: <code>
<nowiki><hidden Klik om te tonen>
 ... 
</hidden></nowiki></code>
<hidden Bijvoorbeeld!>
Dit is een verstopt stukje tekst met wat code.<code html>
<html>
<body>
<h1>Kop</h1>
  <p>Staart</p>
</body>
</html>
</code>
</hidden>

=== Inspringen, lijsten, uitlijning ===
Zolang je een (genummerde) lijst met ingesprongen punten niet onderbreekt loopt de nummering keurig door. Om toch zaken als plaatjes, code, .. tussen de punten weer te geven zonder het inspringen teniet te doen of een nummering te verstoren zie:
  * [[https://www.dokuwiki.org/faq:lists|FAQ lists]]
  * Het gebruik van de ''[[https://www.dokuwiki.org/plugin:wrap|wrap]]'' plugin, bijvoobeeld, voor een tabel tussen de punten:<code>
  * Dit is een heel belangrijk punt
    * met een ingeprongen punt \\ en doe er maar een tabel bij<div>
^Mijn  ^tabel  ^Kop  ^
|met  |een  |regel  |
</div>
</code>En met als resultaat o.m. de volgende tabel<div>
^Mijn  ^tabel  ^Kop  ^
|met  |een  |regel  |
</div>


/*
=== Uitlijning ===
Met de [[https://www.dokuwiki.org/plugin:divalign2|divalign2]] plugin ontstaan wat meer mogelijkheden voor de positionering van tekst. Bijvoorbeeld, aan de rechterkantlijn plaatsen van een alinea:<code>
;;#
Dit is een alinea langs de rechterkantlijn. 
;;#</code>

*/



^  [[dokuwiki:gebruik|Terug naar boven]]  ^


=== Kolommen ===
Door middel van de plugin [[https://www.dokuwiki.org/plugin:columns|columns]] kunnen kolommen aangemaakt worden. Bijvoorbeeld voor drie kolommen, even breed en links uitgelijnd:<code>
<columns - - ->

<newcolumn>

<newcolumn>

<newcolumn>

</columns>
</code>

=== Text-plugin ===
[[https://www.dokuwiki.org/plugin:text|text]]

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

==== Beeld ====
  * [[https://www.dokuwiki.org/plugin:a2s|a2s]] Ascii to SVG (diagrammen maken van ASCII versie)
===== Tips =====
  * [[https://www.dokuwiki.org/tips|Tips op de DokuWiki web-site]]
  * Blokken met //code// laten inspringen met de tekst:<code>
  * Blokken met //code// laten inspringen met de tekst:<code>
Blokken met //code// laten inspringen met de tekst:</ code>
</code>(uiteraard zonder die spatie).
  * Plaatjes mee laten inspringen met de tekst:<code>
  * Plaatjes mee laten inspringen met de test: \\ {{plaatje.png|Naam}} \\  
</code>NB: voeg één of meer spapties to achter de laatste "<nowiki>\\</nowiki>"
  * Uitvullen of niet? Net als in cellen van een tabel wordt ook tekst zonder spaties aan het eind uitgevuld!
  * **Navigatie:** Maak "het verkennen van de pagina" wat makkelijker door bijvoorbeeld:
    * [[#Flexibele inhoudsopgave]]
    * of de inhoudsopgave uitzetten<code>~~NOTOC~~</code> en vervangen door je "eigen versie" (koppelingen naar secties in de pagina bijvoorbeeld).
    * Alle secties, met name lange, te voorzien van een knop "Terug naar boven", bijvoorbeeld zo:<code>
^  [[namespace:subnamespace:pagename|Terug naar boven]]  ^
</code>Resultaat staat onderaan deze sectie. Of gebruik een minder opvallende koppeling, bijvoorbeeld:<code>
[[namespace:subnamespace:pagename|Top]]</code>Je kan de paginaam weglaten maar dat levert dan fouten op als je de pagina later verhuist met de "move" extensie. Resultaat: \\ [[dokuwiki:gebruik|Top]]
    * Genereer een "alfabetische lijst koppelingen" voor gebruik in je paginacode<code bash>
echo {A..Z}|sed 's/\([A-Z]\)/\[\[#\1\]\]/g'
</code>
    * URL manipulatie: gebruik de Wiki-syntax om je pagina met bepaalde parameters opnieuw te laden, bijvoorbeeld met de [[https://www.dokuwiki.org/plugin:dw2pdf|dw2pdf]] plugin:<code>
[[?do=export_pdf|Druk deze pagina af als PDF!]]
</code>
    * Zoek meteen op Google naar "dokuwiki syntax cheat sheet" en open met de knop //I feel lucy!//<code>
[[do>dokuwiki+syntax+cheat+sheet]]
</code>

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

==== Nieuwe wiki-takken ====
Een nieuwe map in de wiki-structuur aanmaken is het eenvoudigste te doen door de URL te manipuleren:
  * Ga naar de //name space//, ofwel wiki-tak, waar de nieuwe map moet komen
  * Open een willekeurige pagina in deze tak
  * Verander nu de paginanaam in de URL in het volgende<code xml>
<mijn_map>:start
</code><color red>**NB:** gebruik kleine letters en "_", geen spaties!</color>
  * Kies de knop ''**[Create this page]**''
  * Als het goed is wordt ongeveer de volgende [[https://www.dokuwiki.org/namespace_templates#template_files|sjabloon]] geopend. Wijzig de titel voor een mooie paginanaam (komt in het menu en verwijzinen) en dynamische inhoud:<code>

====== Nieuwe Wikitak ======
Met het volgende formulier kun je een nieuwe pagina toevoegen binnen deze tak:
{{NEWPAGE}}

\\
Verder is hier het volgende te vinden:
<nspages -subns -h1 -simpleList -exclude:start -textPages="" -textNS="">

====== Recent gewijzigd ======
{{changes>ns=algemeen}}
</code>
  * Je zou nu op de VM zelf handmatig een [[https://www.dokuwiki.org/namespace_templates#template_files|sjabloon]] kunnen maken. Je kan ook een dag wachten dan gebeurt het vanuit de ''crontab'' (''/etc/cron.d/dokuwiki'')

<hidden Handmatig sjabloon aanmaken>
  * Voeg achteraf nog een [[https://www.dokuwiki.org/namespace_templates#template_files|sjabloon]] voor gewone pagina's binnen de betreffende tak toe
    * Log in op de wiki server (''nwr-ipvl-wki001'') met je IPA account (zelfde als waarmee je op de Wiki inlogt)
    * Wordt root om een shell als gebruiker apache te kunnen starten:<code bash>
$ sudo su - 
[root@nwr-ipvl-wki001 ~]# sudo -s -u apache
bash-4.1$ 
</code>
    * Maak een sjabloon aan, bijvoorbeeld door een bestaande te kopieren:<code>
cd /var/www/html/dokuwiki2/data/pages
cp -pi _template.txt mijn/nieuwe/mapje/
</code>Inhoud van ''_template.txt'' is bijvoorbeeld:<code>
{{tag>@PAGE@}}
~~CLOSETOC~~

~TOC:1-4~~

====== @!FILE@ ======


[[linux:dokuwiki:gebruik|Terug naar boven]] \\ 
<sub>
Aangemaakt: %Y-%m-%d door @NAME@
</sub>
</code>
</hidden>
==== Verhuizing wiki-pagina's ====


=== Pagina verhuizen binnen de wiki ===
**Voor beschrijving met plaatjes zie <nowiki>[[move_page|deze pagina]]</nowiki>**

Er zijn meerdere mogelijkheden om een **pagina** te **verhuizen**:
  - Met de wiki:
    * Open de oude pagina, kies bewerken, copieer de hele inhoud
    * Open de nieuwe pagina en plak de inhoud
    * Vervang de originele inhoud eventueel door een verwijzing
  - Er zijn [[https://www.dokuwiki.org/plugin:move|plugins]] die ongeveer het bovenstaande doen
    * Bijvoorbeeld ''[[https://www.dokuwiki.org/plugin:move|move]]'': **Als je admin-rechten hebt** kun je 
      * de betreffende pagina openen
      * op de ''[Admin]'' knop drukken
      * onder //"Additional plugins"// de koppeling voor deze plugin ("Move pages and namespaces") selecteren
        * Zorg dat het volgende geselecteerd is<code>
(*) Move page</code>
        * Daar onder zie je dan vet de paginanaam in de vorm "''**<namespace>:<paginanaam>**''"
        * Daar onder kun je de bovenliggende tak van de wiki - de **//parent namespace//** wijzigen
      * Klik ''**[Start]**'' (twee keer) en hoop dat alles goed gaat!
      * <hi yellow>Vraag de pagina een keer op via z'n nieuwe locatie</hi> (de pagina zit anders niet in de //"zoek-cache"// en is dus niet te vinden)
    * <nowiki>[[move_page|Voorbeeld pagina verhuizen naar andere namespace]]</nowiki> (met plaatjes).
  - **Bij voorkeur niet gebruiken** Valsspelen (nadeel, de wiki //heeft dit niet door//):
    * Login op de wiki-server
    * Verplaats de pagina op disk

<hidden Resultaat //move plugin// actie in wijzigingenoverzicht><html>
<li class="level1"><div class="li"><a href="/dokuwiki2/doku.php?id=linux:basis_infra:service:puppet:puppet_enterprise" class="wikilink1" title="linux:basis_infra:service:puppet:puppet_enterprise">Puppet Enterprise 2015 Server</a> ↷ Links adapted because of a move operation</div>
</li>
<li class="level1"><div class="li"><a href="/dokuwiki2/doku.php?id=linux:basis_infra:service:puppet_enterprise" class="wikilink2" title="linux:basis_infra:service:puppet_enterprise" rel="nofollow">puppet_enterprise</a> ↷ Page moved from linux:basis_infra:service:puppet_enterprise to linux:basis_infra:service:puppet:puppet_enterprise</div>
</li>
</html>
</hidden>

=== Pagina verwijderen ===
Bewerk de hele pagina (knop links boven), werwijder alles en sla de lege pagina op.
=== Name space verhuizen binnen de wiki ===
**Voor beschrijving met plaatjes zie <nowiki>[[move_page|deze pagina]]</nowiki>**

Analoog aan een pagina verhuizen met de //move-plugin// en **als je admin-rechten hebt** kun je 
  * een pagina binnen de betreffende wiki-tak (//name space//) openen, bijvoorbeeld **''mijn:wiki:pad:pagina''**, <hi yellow>dit werkt dus niet voor een lege //namespace// of een met uitsluitend sub-mappen!</hi>
  * op de ''[Admin]'' knop drukken
  * onder //"Additional plugins"// de koppeling voor deze plugin ("Move pages and namespaces") selecteren
    * Zorg dat het volgende geselecteerd is<code>
(*) Move namespace  mijn:wiki:pad</code>
    * Je ziet achter "Move namespace dus vet het wiki-pad ("''**mijn:wiki:pad**''") 
    * In het tekstvak daaronder staat, zodra je dit selecteert, ook **''mijn:wiki:pad''**, de geselecteerde paginanaam valt weg (**''pagina''** in dit voorbeeld)
    * Je kan in dit tekstvak de ''**mijn:wiki:pad**'' wijzigen, bijvoorbeeld:
      * Maak van **''pad nieuwpad''** als je alleen die map een andere naam wil geven
      * Maak van **''wiki''**, bijvoorbeeld **''nieuw:wiki:mapje''** om **''pad''** met inhoud en al naar "**''mijn:nieuw:wiki:mapje''**" te verplaatsen
  * Klik ''**[Start]**'' 
    * Dan kom je in een nieuwe pagina
    * Klik daar weer op ''**[Start]**'', blijf daar totdat de vorderingenbalk "vol gelopen is" en je de "OK" melding krijgt!
    * <hi yellow>Verhuisde pagina's zijn nu niet te vinden</hi> (pagina's openen of een dag wachten tot het crontab-script dat gedaan heeft!)

**Wat niet goed gaat:**
  * Dit werkt niet als een pagina en namespace dezelfde naam hebben (maar dat had je sowieso niet moeten laten gebeuren!)
  * Bij het verhuizen (van een //namespace//) worden "blanco koppelingen" als <code>[[|top]]</code> ingevuld (de uitkomst is dus niet het gewenste resultaat).


^  [[dokuwiki:gebruik|Terug naar boven]]  ^

=== Oude naar nieuwe wiki ===
<hidden Dit proces is afgerond>
Verhuis een pagina van de oude wiki bijvoorbeeld in de volgende stappen:
  * Kies bewerken van de hele pagina en kopieer de hele inhoud 
  * Plak die in de nieuw pagina
  * Als er illustraties bij zaten kun je Chrome gebruiken om de plaatjes te "knippen en plakken"
  * Voorzie de originele pagina nu van een waarschuwing:
    * Maak onder de titel de waarschuwing met de link naar de nieuwe lokatie aan
    * Zet de hele rest van de pagina tussen "commentaar-markeringen"
    * Klik "Preview" om te kijken of dit goed gaat, indien nodig spaties invoegen tussen de volgende tekens: "''*/''"<code>
===== Titel =====
<note warning>
Deze pagina is achterhaald!
</note>
/*

Resterende originele inhoud. Let op gevaalijke sterretjes! Dus eventueel een spatie invoeten tussen een "*" en een "/"

*/
</code>

^  [[dokuwiki:gebruik|Terug naar boven]]  ^
</hidden>

==== HTML en PHP ====
In de configuratiepagina kan ondersteuning voor //ingebedde HTML en/of PHP// worden aangezet. HTML staat aan, PHP staat uit. Hou er rekening mee dat je code tussen open- en sluitmarkering (op hun eigen regels?) moet staan, bijvoorbeeld:<code html>
<html>
<strong>HTML-tekst</strong>
<html>

</code>Zonder nieuwe regel na **''</html>''** zie je mogelijk alleen de code!

Vangwege de risico's kan het gebruik eventueel weer ingeperkt worden met de volgende plugins:
  * ''[[https://www.dokuwiki.org/plugin:htmlokay|htmlokay]]'': Beperk de rechten op HTML-invoegen tot bepaalde gebruikers of groepen
  * ''[[https://www.dokuwiki.org/plugin:htmlsafe|htmlsafe]]'': Negeer bepaalde "gevaarlijke" markeringen (''onmouse*'', ..).

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

=== HTML omzetten ===
Er zijn ook diverse mogelijkheden om [[https://www.dokuwiki.org/tips:htmltowiki|HTML-pagina's]] naar DokuWiki-opmaak om te zetten. Uiteraard werkt een tekst-browser ook:
   LC_ALL=C w3m -dump http://www.beurs.nl/koersen/aex/p1
   
Het tijdelijk op "C" instellen van je //locale-instellingen// voorkomt het gebruik van o.m. //line-draw characters// e.d.

^  [[dokuwiki:gebruik|Terug naar boven]]  ^

==== Tekst bewerken ====
Er zijn meerdere alternatieven voor het bewerken van tekst anders dan het gebruikelijke //Edit// venster in je browser:
  - Installeer ''[[https://www.dokuwiki.org/plugin:ckgedit|ckgedit]]'': 
    * In de instellingen kun je deze plugin configureren om al dan niet de //default// te zijn, ook kun gebruikers of groepen uitzonderen van die //default// (dus die krijgen de gebruikelijke //editor//
    * Afhankelijk van je huidige //editor// bevat een nieuwe knop in je bewerkingssessie "[CKG edit]" of "[DW edit]", druk die knop in en je bewerkingssessie wordt afgesloten en de nieuwe voorkeur in een //cookie// opgeslagen, bij de volgende keer dat je "[Edit]" kiest wordt de instelling uit dat //cookie// gebruikt (als het er nog is).
  - Valsspelen: Login op de server en pas een tekst aan naar eigen inzicht:
    * Bijvoorbeeld een kolom toevoegen aan alle tabellen van vier kolommen:<code xml>
sed -i -e 's/\^$/\^  Opmerkingen  \^/;s/\(^|.*|.*|.*|$\)/\1  |/' <mypage>.txt
</code>
    * Zorg er altijd voor dat je bestand van gebruiker en groep ''apache'' blijft!
  - Installeer een plugin, de volgende twee kunnen via een contextmenu in het bewerkingsvenster worden aangeroepen:
    * ''[[http://appsweets.net/wasavi/|wasavi]]'' voor Chrome (//vi//-achtige modus voor [[https://github.com/akahuku/wasavi|tekstbewerking in de browser]] zelf)
      * <color red>Knippen en plakken werkt helaas niet</color>
      * <color red>Punt voor herhaling laatste commando ook niet(?)</color>
    * ''[[https://addons.mozilla.org/nl/firefox/addon/its-all-text/|its-all-text]]'' voor Firefox (opent ingesteld extern grafisch programma). Je kan, uiteraard, ook ''vi'' in een //terminal emulator// gebruiken door een //wrapper script// te schrijven:
      * Op Unix/Linux: maak een script dat een X-term opent:<code bash>
#!/bin/sh
exec xterm -e /usr/bin/vim "$@"
</code>Aangezien dit een echte terminal-emulator met ''vim'' is neem ik aan dat alles werkt zoals verwacht. Gebruik "**''vi''**" i.p.v. ''vim'' voor compatibele modus.
      * Op Mac OS X kun je eventueel "[[http://blog.asyd.net/2009/09/using-its-all-text-on-mac-os-x/|iTerm]]" gebruiken, maar "[[http://apple.stackexchange.com/questions/115994/terminal-app-equivalent-of-xterm-e-cmd|Terminal]]" kan ook en wel veel [[http://apple.stackexchange.com/questions/12935/how-to-open-a-new-terminal-window-when-using-vim|eenvoudiger]]. Iets verbeterd t.o.v. het laatste voorbeeld, maak **''~/bin/alltext.sh''** met de volgende inhoud<code bash>
#!/bin/bash
if [ $1 == "" ]; then
	echo "No filename given!"
	exit 9;
fi

osascript <<END
tell app "Terminal" to do script "/usr/bin/vi ${1}" & "; exit"
END
</code>**NB:** Configureer dit script in de instellingen van ''[[https://addons.mozilla.org/nl/firefox/addon/its-all-text/|its-all-text]]'' en verander het pad voor de "Cache directory" in iets zonder spaties, bijvoorbeeld **''~/Library/Caches/itsalltext''** (anders krijgt ''vi'' twee argumenten i.p.v. een kloppend pad).
    * [[https://people.ksp.sk/~martin/firefox/extensions/EmbeddedEditor/|EmbeddedEditor]] of [[https://github.com/ardagnir/pterosaur|Pterosaur]] (//abandonware//) om ''vim'' te gebruiken in Firefox.


^  [[dokuwiki:gebruik|Terug naar boven]]  ^



<sub>
Aangemaakt: 2019-07-19 door Joachim la Poutré (adm)
</sub>
