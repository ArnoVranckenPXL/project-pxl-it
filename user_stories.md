# User stories

 

| Story  ID            | 1                                                            |
| -------------------- | ------------------------------------------------------------ |
| Naam                 | Als gebruiker kan ik mij registreren zodat ik toegang krijg met mijn credentials (username en paswoord) tot de spelomgeving waarin ik een spel kan opstarten en spelen. |
| Screen               | Registration  screen                                         |
| Trigger              |                                                              |
| Script               | Als gebruiker die zich wenst te registreren vul ik de volgende informatie in:<br />-    email  <br/>-    nickname <br/>-    paswoord  <br />-    Re-enter  paswoord<br />Wanneer de gebruiker klikt op de "Registreer"-knop wordt gecontroleerd of alle velden ingevuld zijn. Daarna wordt gecontroleerd of beide ingevulde paswoorden identiek zijn en voldoen aan volgende regels:<br />TODO paswoord regels<br />De ingevulde gegevens worden vervolgens verstuurd naar de backend. Indien de registratie succesvol is verlopen, wordt het login-scherm getoond zodat de gebruiker kan inloggen. Indien er een fout is opgetreden wordt de foutboodschap getoond. |
| Deadline             |                                                              |
| Acceptance  criteria | - Er wordt een foutboodschap getoond indien er gegevens ontbreken<br />- Er wordt een foutboodschap getoond indien beide paswoorden niet overeenkomen.<br />- Er wordt een foutboodschap getoond indien er een fout is opgetreden in de backend bij het registeren van de gebruiker.<br />- Het login-scherm wordt getoond indien de registratie van de gebruiker correct is verlopen. |
| Backend URL          | http://{host}:{port}/api/Authentication/register             |

 