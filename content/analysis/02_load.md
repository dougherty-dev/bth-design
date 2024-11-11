---
Title: Laddtid
Description: clock
Template: analyses
---

Prestanda för några webbplatser
=======================

Ett antal webbsajter undersöks med avseende på laddningstid och användbarhet i syfte att utröna optimalt förfarande vid formgivning av webbresurser. Är responstiden inom ett godtagbart spann eller finns utrymme för förbättringar, och i så fall vilka?

Urval
-----------------------

Tre webbsajter väljs ut för ändamålet, av vilka den första utgörs av Blekinge tekniska högskola (BTH), av det enkla skälet att denna rapport författas inom ramen för dess verksamhet. Den andra är en personlig fotosajt, som råkar omfatta en rad aspekter som avhandlas i denna kurs. Den tredje är statsradion SR. För var och en av de tre webbplatserna väljs tre sidor ut för analys.

Metod
-----------------------

I vår analys stödjer vi oss främst på *Google page speed insights* (PSI) samt webbläsarens inspektor, främst nätverksdelen. För de tre webbplatserna undersöker vi för såväl mobil som stationär dator/platta hur PSI bedömer prestanda, tillgänglighet, sökmotoroptimering (SEO) samt i vilken grad «bäst praktik» har tillämpats vid utformningen.

I inspektorn noterar vi antalet laddade resurser och den totala datavolymen för sidan. För varje undersökt sida bestäms medelvärdet av laddningstid för tre försök, vilka utförs i anonymt läge för att undvika cachade resurser. Resultaten införs i ett [kalkylark](https://docs.google.com/spreadsheets/d/1jC8S_ru2FlA9WRdD5Gra4V0MgnDJaJZR1X-8hIqMw4U/edit?usp=sharing), som även bäddas in här för bekväm referens.

<iframe style="height: 40vh; width: 100%" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQ0b3YS2OnKnHVKBiRlpnxAx2jVzMteNjpfPAYOUdFgN4Xlk4fYwPnKmwNo2KG1njpbrYvKjIfqX6Mm/pubhtml?widget=true&amp;headers=false"></iframe>

Resultat
-----------------------

### Blekinge tekniska högskola

![Blekinge tekniska högskola](%assets_url%/img/bth.avif)

Utbildningsanstalten präglas av långa laddningstider för var och en av de tre sidorna, inklusive fronten. Med ett snitt kring tre sekunder får sajten föga överraskande uselt prestandabetyg i PSI (31–43). Man kunde förvänta att en statlig organisation skulle vara särskilt optimerad för tillgänglighet, men även här är nivån på gränsen till godkänd (89–93), vilket kan ha samband med att man inte tycks ha tillämpat «best practices» i högre omfattning än 75. Bäst omdöme erhåller man för SEO (92–93).

Av PSI:s analys att döma skulle man kunna förbättra prestandan genom att eliminera icke nyttjade skript och stilscheman samt minifiera övriga. Javascript tycks också ha en ganska tung inverkan på prestandan, därtill i en enda tråd. PSI anser vidare att BTH servar förlegade bildformat.

**Sidor**: [https://www.bth.se/](https://www.bth.se/) | [https://www.bth.se/forskning/](https://www.bth.se/forskning/) | [https://www.bth.se/utbildning/program-och-kurser/?val=kurspaket](https://www.bth.se/utbildning/program-och-kurser/?val=kurspaket)

--- 

### Inposure

![Inposure](%assets_url%/img/inposure.avif)

Min privata fotosajt får genomgående värdet 100 av PSI för «best practices», vilket noteras med belåtenhet. Även prestandan når 100 för desktopversionen, men bara 87–93 för mobilen, vilket inte överraskar. Tillgängligheten hamnar statiskt på 81, vilket inte heller är avsett att förvåna givet utformningen. På samma sätt förhåller det sig med SEO, som inte alls har beaktats vid designen. Felen är dock få och skulle ganska enkelt kunna åtgärdas för bättre poäng.

Av de tre sajterna erhålls bara här laddningstider under sekunden (0.7–1.2 s), men då är det en tämligen begränsad sajt som med avsikt har optimerats sålunda. PSI menar att bättre resultat kan erhållas med mindre bilder, men det är en sanning med en modifikation. Bilderna är med avsikt stora och få till antalet variationer för att undvika kostsam mikrohantering, samtidigt som de har minimal tyngd givet ett modernt bildformat som AVIF. Hantering med ett otal exakta versioner är i min optik ett förlegat koncept, och det verkliga problemet är att bilder i allmänhet är *alldeles* för små.

**Sidor**: [https://inposure.se/](https://inposure.se/) | [https://inposure.se/s/3-places.shashin](https://inposure.se/s/3-places.shashin) | [https://inposure.se/s/1-portraits.shashin](https://inposure.se/s/1-portraits.shashin)

---

### Sveriges radio

![Sveriges radio](%assets_url%/img/sr.avif)

Statsradion lägger sig i gult territorium avseende prestanda (54–60) för mobil version, men glänser i övriga klasser. Prestandabetyget bottnar i ganska usla laddningstider om 1.7–4.1 sekunder, men sanningen att säga är den metriken inte längre så relevant givet att de flesta har cacheresurser att tillgå, inte minst från tredje part i form av fonter, skript med mera.

Ur designperspektiv finns inte så mycket att orda om sajten, som åtminstone i det avseendet håller hög klass.

**Sidor**: [https://sverigesradio.se/](https://sverigesradio.se/) | [https://sverigesradio.se/nyheter](https://sverigesradio.se/nyheter) | [https://sverigesradio.se/radioswedenarabic](https://sverigesradio.se/radioswedenarabic)

Analys
-----------------------

Gemensamt för många webbsajter tycks vara att DOM:en anses vara för stor, att man kunde implementera en cacherutin samt en rad småfel som att objekt saknar angiven bredd och höjd. Genomgående är också att sajter presterar bättre på stationär enhet än i mobilen. Skript och stilmallar är som regel för stora, för många och inte optimerade.

Ytterligare fel ges av att ladda för många externa resurser och därmed göra sig beroende av tredje parts kod. Bland mer intressanta fel återfinns «eliminate render-blocking resources», som det kunde löna sig att fördjupa sig i.

Det blir lite av en meningslös exercis, men «vinnare» i detta minitest blir naturligtvis SR, med BTH på jumboplats.

Laddningstid är nog så viktigt, men var mer relevant fordom. Numera finns, inom rimliga gränser (< 4 s initialt, < 2 s succesivt), mer relevamta problem som ständig interaktion kring val av cookies och andra irriterande egenskaper, likväl som att sajter bara erbjuder en för ögonen skadlig vit design.
