# User stories

 

| Story  ID            | 1                                                            |
| :------------------- | :----------------------------------------------------------- |
| Naam                 | Als gebruiker kan ik mij registreren zodat ik toegang krijg met mijn credentials (username en paswoord) tot de spelomgeving waarin ik een spel kan opstarten en spelen. |
| Screen               | Registration  screen                                         |
| Type                 | Frontend (backend is reeds volledig)                         |
| Script               | Als gebruiker die zich wenst te registreren vul ik de volgende informatie in:<br />-    E-mailadres  <br/>-    Username <br/>-    Wachtwoord  <br />-    Wachtwoord verificatie<br />Wanneer de gebruiker klikt op de "Registreer"-knop wordt gecontroleerd of alle velden ingevuld zijn. Daarna wordt gecontroleerd of beide ingevulde wachtwoorden identiek zijn en voldoen aan volgende regels:<br />TODO paswoord regels<br />De ingevulde gegevens worden vervolgens verstuurd naar de backend. Indien de registratie succesvol is verlopen, wordt het login-scherm getoond zodat de gebruiker kan inloggen. Indien er een fout is opgetreden wordt de foutboodschap getoond. |
| Deadline             |                                                              |
| Acceptance  criteria | - Er wordt een foutboodschap getoond indien er gegevens ontbreken.<br />- Er wordt een foutboodschap getoond indien beide paswoorden niet overeenkomen.<br />- Er wordt een foutboodschap getoond indien er een fout is opgetreden in de backend bij het registeren van de gebruiker.<br />- Het login-scherm wordt getoond indien de registratie van de gebruiker correct is verlopen. Het e-mailadres van de geregistreerde gebruiker is reeds ingevuld zodat hij enkel zijn wachtwoord moet invullen. |
| Backend URL          | http://{host}:{port}/api/Authentication/register             |

| Story  ID           | 2                                                            |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Als geregistreerde speler kan ik inloggen zodat ik een spel kan starten en spelen. |
| Screen              | Login  screen                                                |
| Type                | Frontend (Backend is reeds volledig)                         |
| Script              | Als geregistreerde speler kan ik op de login pagina mijn e-mailadres en wachtwoord invullen. Wanneer ik op de "Inloggen"-knop druk worden mijn inloggegevens gecontroleerd door de backend. Indien de inloggegevens correct zijn wordt de lobby pagina getoond. |
| Deadline            |                                                              |
| Acceptatie criteria | - Er wordt een foutmelding getoond indien er gegevens niet zijn ingevuld.<br />- Er wordt een foutmelding getoond indien de inloggevens niet correct zijn.<br />- De lobby pagina wordt getoond indien de speler correct is ingelogd. |
| Backend URL         | http://{host}:{port}/api/Authentication/token                |

| Story  ID           | 3                                                            |
| ------------------- | ------------------------------------------------------------ |
| Naam                | Als ingelogde speler kan ik op de lobby pagina een nieuw spel starten. |
| Screen              | Lobby pagina                                                 |
| Trigger             |                                                              |
| Script              | Als ingelogde speler kan ik op de lobby pagina op een knop drukken waarmee een nieuw spel wordt gestart. De configuratie van het default spel wordt naar de backend verstuurd en het response van de backend bevat o.a. een unieke identificatie voor het aangemaakte spel. |
| Deadline            |                                                              |
| Acceptatie criteria | - De spel pagina wordt getoond als de creatie van het spel is gelukt en de frontend de unieke identificatie (id) van het spel heeft ontvangen. |
| Backend URL         | http://{host}:{port}/api/games                               |

| Story  ID           | 4                                                            |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Als speler kan ik mijn schepen in het spelbord plaatsen.     |
| Screen              | Spel  pagina                                                 |
| Type                | Frontend + Backend                                           |
| Script              | Een 10x10 spelbord wordt getoond waar de speler zijn schepen kan plaatsen. Volgende schepen moeten op het scherm geplaatst worden:<br />- carrier (5 cellen)<br />- battleship (4 cellen)<br />- destroyer (3 cellen)<br />- submarine (3 cellen)<br />- patrolboat (2 cellen)<br />Ieder schip kan maar 1 keer op het spelbord geplaatst worden. Schepen kunnen wel nog verplaatst worden. Schepen mogen niet overlappen. Schepen mogen elkaar wel raken. Zodra de speler alle schepen op hun gewenste positie op het spelbord geplaatst heeft, kan het spel effectief gestart worden. |
| Deadline            |                                                              |
| Acceptatie criteria | - Wanneer een schip met 1 of meerdere cellen overlapt met een ander reeds geplaatst schip, zal er door de backend een foutboodschap gegeven worden en wordt het schip niet op de gevraagde positie geplaatst.<br />- Wanneer een schip op een geldige positie geplaatst is, is dit zichtbaar waar ik het schip heb geplaatst. Het schip kan verplaatst worden naar een andere geldige positie. |
| Backend URL         | http://{host}:{port}/api/games/{id}/positionship             |

 

| Story  ID           | 5                                                            |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Als speler krijg ik tijdens het plaatsen van de schepen en het effectief spelen van het spel steeds voldoende informatie. |
| Screen              | Spel pagina                                                  |
| Type                | Frontend + Backend                                           |
| Script              | Op iedere ogenblik vanaf het starten van een nieuw spel kunnen de actuele gegevens van een spel opgevraagd worden en indien nodig aan de speler getoond worden. <br />Deze gegevens bevatten o.a. een boolean isReadyToStart, die aangeeft of alle schepen van de speler correct geplaatst zijn, de posities van de eigen schepen, de status van het spelbord van de tegenstander en status van het eigen spelbord. |
| Deadline            |                                                              |
| Acceptatie criteria | - Tijdens het spelen van het spel ziet de speler hoeveel schoten hij en de tegenstander reeds hebben afgeschoten.<br />- Tijdens het spelen van het spel ziet de speler welke en hoeveel schepen reeds tot zinken zijn gebracht bij de tegenstander.<br />- Tijdens het spelen van het spel ziet de speler welke en hoeveel schepen de tegenstander reeds tot zinken heeft gebracht bij de speler.<br />- Wanneer alle schepen van de speler tot zinken zijn gebracht krijgt de speler een mededeling dat hij verloren is en is het spel afgelopen.<br />- Wanneer de speler alle schepen geplaatst door de backend tot zinken heeft gebracht krijgt de speler de melding dat hij het spel heeft gewonnen en is het spel afgelopen. |
| Backend URL         | http://{host}:{port}/api/games/{id}                          |

 

| Story  ID           | 6                                                            |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Als speler kan ik het spel effectief beginnen spelen zodra ik al mijn schepen op een geldige positie heb staan. |
| Screen              | Spel pagina                                                  |
| Type                | Frontend + Backend                                           |
| Script              | Zodra alle schepen door de speler op een geldige positie zijn geplaatst, kan de speler beslissen om het spel effectief te starten. In de backend wordt ook een spelbord met schepen voor de speler aangemaakt. In de basisversie van het spel zal de backend de schepen willekeurig op een geldige positie plaatsen. |
| Deadline            |                                                              |
| Acceptatie criteria | - De knop om het spel te starten wordt beschikbaar zodra alle schepen op een geldige positie staan.<br />- Zolang het spel niet gestart is, kunnen er geen schoten gelost worden. Vanaf het ongeblik dat het spel gestart is kan de speler een schot lossen. |
| Backend URL         | http://{host}:{port}/api/games/{id}/start                    |

 

| Story  ID           | 7                                                            |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Als speler kan ik, zodra het spel gestart is, een schot aflossen om zo proberen de schepen van mijn tegenstander tot zinken te brengen. |
| Screen              | Spel pagina                                                  |
| Type                | Frontend + Backend                                           |
| Script              | De speler selecteert een positie op het spelbord waar hij het schot wil lossen. De coördinaten van het schot worden naar de backend verstuurd, die vervolgens antwoord of het raak was of niet. Indien het schot ervoor zorgt dat het volledige schip geraakt is zal dit ook in het antwoord van de backend staan. |
| Deadline            |                                                              |
| Acceptatie criteria | - De speler kan een coördinaat selecteren en een schot lossen.<br />- De speler ziet duidelijk of zijn schot raak is of niet.<br />- De speler ziet duidelijk wanneer hij een volledig schip tot zinken heeft gebracht. |
| Backend URL         | http://{host}:{port}/api/games/{id}/shoot                    |


# User stories - Extra's

Deze optionele user stories specifiëren het gewenste gedrag bij het implementeren van extra's in de applicatie.

| Story  ID           | 8                                                            |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Slimme computer strategie |
| Screen              | Spel pagina                                                  |
| Type                | Backend                                           |
| Script              | Wanneer de computerspeler aan zet is, wordt er niet langer een willekeurige vrije cel geselecteerd om op te schieten. De computerspeler bekijkt eerdere schoten die een schip geraakt hebben en selecteert op basis daarvan een logische zet. |                                                            |
| Acceptatie criteria | - De computerspeler selecteert geen willekeurige cel indien er een betere zet mogelijk is.<br />- De computerspeler probeert steeds een eerder geraakt schip tot zinken te brengen.<br />[- De computerspeler schiet niet op plaatsen waar een schip niet meer *kan* staan. (door te weinig ruimte) |

| Story  ID           | 9                                                        |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Meerdere schoten per beurt |
| Screen              | Spelopties, Spel pagina                                                  |
| Type                | Frontend + Backend                                           |
| Script              | De speler kan kiezen om het spel te starten met deze optie. In deze variant kan een speler meerdere schoten per beurt afvuren. Het precieze aantal schoten kan ook variëren, naargelang de optie die gekozen wordt: 
   * Het aantal niet gezonken schepen van de aanvallende speler
   * De grootte van het grootste niet gezonken schip van de aanvallende speler
   * Een vooraf gedefinieerd aantal schoten |                                                            
| Acceptatie criteria | - De speler kan een spel starten met de optie om elke beurt meerdere schoten tegelijk af te vuren.<br /> - De speler kan kiezen welke regel er gebruikt wordt voor het bepalen van dit aantal.<br /> - De speler kan het betreffende aantal schoten in zijn beurt afvuren.<br /> - De computerspeler kan dit op dezelfde manier.<br /> - Het resultaat van dit salvo wordt correct getoond in het spel.<br /> - Het aantal af te vuren schoten wordt correct aangepast tijdens het spel, indien van toepassing. |

| Story  ID           | 10                                                            |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Niet moeten melden van een gezonken schip |
| Screen              | Spel pagina                                                  |
| Type                | Frontend + Backend                                         |
| Script              | Wanneer een schip zinkt, moet dit niet gemeld worden door de betreffende speler. De aanvallende speler moet dit zelf achterhalen door nog extra torpedo's af te vuren. |                                                            |
| Acceptatie criteria | - Bij opstart van het spel kan deze optie meegegeven worden.<br /> - Spelers melden hun gezonken schepen niet aan de andere speler |

| Story  ID           | 11                                                            |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Verplaatsen van schepen tijdens het spel |
| Screen              | Spel pagina                                                  |
| Type                | Frontend + Backend                                         |
| Script              |  |                                                            |
| Acceptatie criteria |  |

| Story  ID           | 12                                                     |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Vervormde schepen toestaan |
| Screen              | Spel pagina                                                  |
| Type                | Frontend + Backend                                         |
| Script              |  |                                                            |
| Acceptatie criteria |  |

| Story  ID           | 13                                                    |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Multiplayer (2 menselijke spelers) |
| Screen              | Spel pagina, Lobby pagina                                                 |
| Type                | Frontend + Backend                                         |
| Script              |  |                                                            |
| Acceptatie criteria |  |

| Story  ID           | 14                                                |
| :------------------ | :----------------------------------------------------------- |
| Naam                | Multiplayer (Groep spelers tegen AI) |
| Screen              | Spel pagina, Lobby pagina                                                  |
| Type                | Frontend + Backend                                         |
| Script              |  |                                                            |
| Acceptatie criteria |  |
 