# Client-Server architectuur


# REST endpoints


# Security: bearer tokens

Als je aan de receptie van een hotel aankomt dan moet je eerst je identiteit bewijzen (dmv je identiteitskaart) en vervolgens krijg je een key card die je toegang geeft tot je hotelkamer.




Hetzelfde principe wordt gehanteerd voor het beveiliging van de backend. Wanneer een gebruiker van de frontend toegang wil krijgen tot de backend moet hij eerst zijn identiteit bewijzen en vervolgens krijgt hij van de backend een token waarmee hem verdere toegang tot de backend wordt verleend. Dit token noemen we een bearer token. De drager (bearer) van het token krijgt toegang tot de backend.

Een speler zal zich dus eerst moeten registeren. Dit kan natuurlijk zonder beveiliging gebeuren. Om een speler te registeren is het REST endpoint /api/Authentication/register voorzien.



Eens een speler geregisteerd is kan hij inloggen en een token aanvragen. Hiervoor is het REST endpoint /api/Authentication/token.



Het response (in json formaat) dat je terugkrijgt van de server bevat de id en nickName van de speler en het (bearer) token. 



Wanneer je eenmaal een bearer token hebt bekomen, kan je de andere REST endpoints gebruiken om bijv. een spel te starten, een schip te plaatsen,… Je moet je bearer token dan meegeven in de Authorization request header. Hieronder zie je het request om een spel te starten. 




Als je gebruikmaakt van fetch om in javascript de REST endpoints aan te spreken kan je het bearer token opslaan in sessionStorage. Hieronder zie je de aanmaak van een fetch-commando met Bearer token. 


fetch(url,
{
  method:"POST",
  body: JSON.stringify(myData),
  headers:{
    'Accept':'application/json',
    'Content-Type':'application/json',
    'Authorization':'Bearer' + sessionStorage.getItem("token")
  }
})
