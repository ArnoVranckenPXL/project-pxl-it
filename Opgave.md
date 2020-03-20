# Zeeslag
In dit project maken jullie een versie van het bekende bordspel **Zeeslag**. In dit spel is het de bedoeling om alle schepen van je tegenstander tot zinken te brengen, voordat je tegenstander dat bij jou doet.

De regels van het spel kan je o.a. op [Wikipedia](https://nl.wikipedia.org/wiki/Zeeslag_(spel)) vinden.

In eerste instantie maken jullie in team een versie waarbij je tegen een computerspeler kan spelen.
Als eventuele extra kunnen jullie er in een latere fase voor zorgen dat het spel ook tegen een andere menselijke speler gespeeld kan worden.

Om dit geheel te realiseren, moeten er twee grote componenten ontwikkeld worden: de **frontend** en de **backend**

## Backend

De backend moet ervoor zorgen dat alle nodige data beschikbaar is voor de frontend. Enkele zaken waarvoor de backend zorgt: gebruikers registreren, gebruikers bijhouden in de database, checken van login gegevens, actieve spelletjes bijhouden, het communiceren van acties tijdens deze spelletjes, ...

Jullie moeten deze component in .NET ontwikkelen. We hebben al een groot stuk van de backend voor jullie voorzien, waarbij jullie het vervolg zelf moeten uitwerken. In deze git repository (zie 'Source') vinden jullie een skelet waarin jullie _**enkele gaten**_ moeten opvullen. 
In deze Wiki geven wat [uitleg over de werking die we verwachten van de backend](Backend). Je vindt alle guides op de [Home pagina](Home).

De backend zal in eerste instantie lokaal gehost worden. Als extra kunnen jullie er eventueel voor zorgen dat de applicatie ook online gespeeld kan worden.

## Frontend

De frontend zal gemaakt worden met webtechnologie. (HTML, CSS, JavaScript) Jullie hebben hiervoor de nodige kennis opgedaan in de vakken **Web Essentials** en **Web Scripting**.
Jullie bepalen als team zelf hoe de applicatie er precies uit zal zien. Houd hierbij rekening dat de applicatie intuïtief en gebruiksvriendelijk moet zijn voor de spelers. Ga bijvoorbeeld eens kijken bij andere online versies van het spel om wat inspiratie op te doen. Overleg met je team welke elementen er in de layout moeten zitten en waar die best geplaatst worden.

Pas zo goed mogelijk de aangeleerde methoden uit de twee bovenstaande vakken toe om een robuuste applicatie te bouwen. De code moet leesbaar en makkelijk uitbreidbaar zijn, zodat je teamgenoten er steeds aan kunnen verder werken.

## Het spel

Een speler kan een account maken en hiermee inloggen. Eens ingelogd, kan de speler een spel starten wanneer hij daar klaar voor is. Voorzie dus een scherm waarop de speler terecht komt na inloggen. Vanop deze pagina kan het spel gestart worden, al dan niet met een aantal opties i.v.m. de regels die toegepast zullen worden tijdens het spel.

Bij de start van een spel moet de speler eerst al zijn schepen plaatsen. Hierbij moeten bepaalde regels gerespecteerd worden, afhankelijk van welke regels en opties er gekozen zijn. Het is de backend die deze checks zal moeten uitvoeren.
Slechts wanneer alle schepen op een correcte manier geplaatst zijn, kan het spel effectief van start gaan. In het spel komen de speler en de computerspeler (backend) om de beurt aan zet en schieten ze een torpedo af op een bepaald vakje in de grid. De basisimplementatie van de computerspeler is een 'domme' implementatie: deze schiet op een willekeurig leeg vakje, zonder voorkennis van de eerder geraakt boten. Een slimmere tegenstander implementeren levert [extra](#extras) punten op.

Wanneer alle vakjes waarin een boot staat, geraakt zijn, zinkt de betreffende boot. Het spel duurt tot een speler alle schepen van de andere speler heeft kunnen laten zinken.

Na afloop van het spel wordt de speler terug gebracht naar het hoofdscherm met de mogelijkheid om een nieuw spel te starten.

## <a name="minimalevereisten"></a>Minimale vereisten

We geven een overzicht van de minimale vereisten voor dit project. Als deze minimale vereisten aanwezig zijn bij de [eindpresentatie](#eindpresentatie) leveren ze 13 punten op. 3 punten hiervan zijn al te verdienen tijdens de [tussentijdse deadlines](#opvolging).

* Registratie van nieuwe gebruiker
* Inloggen met bestaande gebruiker
* Starten van nieuw spel
* Plaatsen van schepen voor menselijke speler
* Automatisch schepen plaatsen voor computer speler
* Start spel na plaatsen van alle schepen
* Schoten lossen en resultaat tonen voor menselijke speler
* Automatisch schoten lossen voor computer spelen ('domme' strategie)
* Einde van het spel: winnaar tonen

## <a name="extras"></a>Extra's

Wanneer de minimale vereisten van hierboven voldaan zijn, kunnen er extra's naar keuze toegevoegd worden. Hiermee kan je je als team onderscheiden van de rest en extra punten scoren.

**Begin pas aan de extra's als alle minimale vereisten klaar zijn.**

We geven enkele ideeën, maar jullie zijn zeker vrij om - in samenspraak met de docenten - een eigen idee als extra te implementeren.

* Implementatie van verschillende alternatieve opties voor spelregels
* Slimme computer strategie (na een hit, het schip snel zinken): 3 punten
* Spelopties:
  * Meerdere schoten per beurt (3 varianten): 3 punten
  * Niet moeten melden van een gezonken schip: 1 punt
  * Verplaatsten van schepen tijdens een spel: 3 punten
  * Vervormde schepen toestaan: 3 punten
* Multiplayer (2 mensen tegen elkaar): 4 punten
* Multiplayer (met een groep tegen een AI): 6 punten
* Eigen ideeën: te bespreken met lectoren

## Projectverloop

Aangezien jullie in team gaan werken, zullen jullie een git repository gebruiken om de laatste versie van jullie project voor iedereen beschikbaar te maken. Jullie hebben in het vak Web Essentials enkele opdrachten in git moeten uitvoeren, dus hebben jullie de nodige kennis hiervoor.

Voorzie ook een communicatietool waarmee jullie makkelijk met elkaar kunnen communiceren wanneer jullie niet samen zitten. De keuze is vrij, tools als Slack, Discord, Microsoft Teams, ... zijn allemaal prima opties hiervoor.

Om jullie een duidelijk overzicht te geven van de verschillende componenten die geïmplementeerd moeten worden, hebben we al een lijst met [user stories](User stories) voorzien. Neem zeker eens een kijkje, het hele project wordt opgedeeld in een aantal subtaken, om het geheel **overzichtelijk** en **opdeelbaar** te maken.

We raden zeker aan om af en toe aan pair programming te doen, waarbij één student code schrijft en de andere mee volgt om zo mee te denken en onmiddellijk fouten op te sporen. Dit is een vaak gebruikte techniek die zeker nuttig kan zijn.

## Verplichte aanwezigheid

Iedereen is **verplicht aanwezig** op alle begeleide projectsessies, voor de **volledige duur** van de sessie!

Bij gewettigde afwezigheid, moet je dit zo snel mogelijk melden aan je teamleden en de docent.
Wanneer je te vaak afwezig bent (zelfs gewettigd), kan je niet slagen voor het project.

Precieze info kan je vinden in de [studiegids](https://ibamaflexweb.pxl.be/BMFUIDetailxOLOD.aspx?b=1&c=1&a=62374).

## <a name="opvolging"></a>Opvolging

Er zullen enkele tussentijdse deadlines plaatsvinden, om jullie vooruitgang beter in te kunnen schatten. 
Jullie kunnen hier telkens al een punt mee verdienen die in het eindresultaat meegeteld zal worden.

**Deadline 1 - Week 3:** Registratie en login moet werken. (1 punt)

**Deadline 2 - Week 4:** Grid configureren (plaatsen van schepen). (1 punt)

**Deadline 3 - Week 5:** Shot lossen + feedback tonen in het spel. (1 punt)

**Finale versie - Week 7:** Eindpresentatie. Resultaat afgewerkte applicatie/game.

## <a name="eindpresentatie"></a>Eindpresentatie

Na afloop van het project wordt er een eindpresentatie gegeven door het hele team. Hierin wordt een demo gegeven van de geïmplementeerde applicatie. Er worden ook enkele inhoudelijke en technische vragen gesteld door de vaklectoren. Elk teamlid moet kunnen antwoorden op vragen uit elk component van de oplossing.

## Evaluatie

Het team krijgt een groepscijfer op 20 (grootste deel op basis van de 
 eindpresentatie, deels tussentijdse deadlines, deels backend tests). Dat cijfer kan nadien in positieve of negatieve zin bijgestuurd worden door een peer-evaluatie met een maximum verschil van 35%. Bijvoorbeeld 12/20 voor het team, kan individueel  16,2/20 worden of 7,8/20. Daarnaast kunnen de lectoren het cijfer ook bijsturen op basis van vaststellingen, zoals studenten die geen bijdrage leveren, geen *git commits* doen, ...

Zoals eerder aangehaald werd, worden de punten als volgt toegekend:
* 13/20 te behalen met minimale vereisten
  * 3 punten hiervan te verdienen tijdens tussentijdse deadlines
* Rest van de punten te verdienen met geïmplementeerde [extra's](#extras)
