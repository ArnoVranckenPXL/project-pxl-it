# User stories

 

| Story  ID            | 1                                                            |
| -------------------- | ------------------------------------------------------------ |
| Naam                 | Als gebruiker kan ik mij registreren zodat ik toegang krijg met mijn credentials (username en paswoord) tot de spelomgeving waarin ik een spel kan opstarten en spelen. |
| Screen               | Registration  screen                                         |
| Trigger              |                                                              |
| Script               | Als gebruiker die zich wenst te registreren vul ik de volgende informatie in:<br />-    E-mailadres  <br/>-    Username <br/>-    Wachtwoord  <br />-    Wachtwoord verificatie<br />Wanneer de gebruiker klikt op de "Registreer"-knop wordt gecontroleerd of alle velden ingevuld zijn. Daarna wordt gecontroleerd of beide ingevulde wachtwoorden identiek zijn en voldoen aan volgende regels:<br />TODO paswoord regels<br />De ingevulde gegevens worden vervolgens verstuurd naar de backend. Indien de registratie succesvol is verlopen, wordt het login-scherm getoond zodat de gebruiker kan inloggen. Indien er een fout is opgetreden wordt de foutboodschap getoond. |
| Deadline             |                                                              |
| Acceptance  criteria | - Er wordt een foutboodschap getoond indien er gegevens ontbreken.<br />- Er wordt een foutboodschap getoond indien beide paswoorden niet overeenkomen.<br />- Er wordt een foutboodschap getoond indien er een fout is opgetreden in de backend bij het registeren van de gebruiker.<br />- Het login-scherm wordt getoond indien de registratie van de gebruiker correct is verlopen. Het e-mailadres van de geregistreerde gebruiker is reeds ingevuld zodat hij enkel zijn wachtwoord moet invullen. |
| Backend URL          | http://{host}:{port}/api/Authentication/register             |

| Story  ID           | 2                                                            |
| ------------------- | ------------------------------------------------------------ |
| Naam                | Als geregistreerde speler kan ik inloggen zodat ik een spel kan starten en spelen. |
| Screen              | Login  screen                                                |
| Trigger             |                                                              |
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
| Acceptatie criteria | - De spel pagina wordt getoond als de creatie van het spel is gelukt en de frontend de unieke identificatie van het spel heeft ontvangen. |
| Backend URL         | http://{host}:{port}/api/games                               |

| Story  ID           | 4                                                        |
| ------------------- | -------------------------------------------------------- |
| Naam                | Als speler kan ik mijn schepen in het spelbord plaatsen. |
| Screen              | Spel  screen                                             |
| Trigger             |                                                          |
| Script              |                                                          |
| Deadline            |                                                          |
| Acceptatie criteria |                                                          |
| Backend URL         |                                                          |

 