---
Title: Design och webbplatser
Description: web
Template: analysis
---

Design och webbplatser
=======================

En webbplats – [Seonmi art](https://www.student.bth.se/~nido24/dbwebb-kurser/design/me/kmom10/) – har skapats, och vi önskar nu undersöka denna med avseende på laddningstid och prestanda. Därvidlag nyttjas dels *Google Page Speed Insights* (PSI), och dels *Goggle Chrome Lighthouse* i navigeringsmodus, på såväl lokal som aktuell server.

Urval
-----------------------

Sajten har ett grundtema samt fyra alternativa teman, som samtliga testas för ett antal sidor, nämligen [frontsidan](https://www.student.bth.se/~nido24/dbwebb-kurser/design/me/kmom10/), [about](https://www.student.bth.se/~nido24/dbwebb-kurser/design/me/kmom10/about), [design](https://www.student.bth.se/~nido24/dbwebb-kurser/design/me/kmom10/design), [gallery](https://www.student.bth.se/~nido24/dbwebb-kurser/design/me/kmom10/gallery) samt [hilites](https://www.student.bth.se/~nido24/dbwebb-kurser/design/me/kmom10/hilites). Inalles rör det sig då om fem gånger fem eller tjugofem sidor för såväl mobil som desktop.

![Seonmi art (tema analog)](%assets_url%/img/seonmi-analog.webp)
*Seonmi art, tema **analog***

Metod
-----------------------

För vart och ett av sajtens fem teman noteras tre mätningar per utvald sida, varvid medelvärden aggregeras till en slutlig poängsumma för sajtens prestanda. Även laddningstid, datamängd och antal resurser noteras.

För Lighthouse sker utprövningen i anonymt läge, på en 4K-skärm (3840 × 2160) i fullskärmsläge med 200 % zoom för att ha en likvärdig grund. En anledning att nyttja flera instrument är att PSI inte vet vilket tema användaren har valt, utan är hänvisad till grundtemat. Under testningen hårdkodas vart och ett av de fem temana (i header.twig respektive theme.js), för att såmedelst utvärdera respektive temas individuella prestanda.

Resultat
-----------------------

### PSI

 Det visar sig att temana är ganska likvärdiga, med samlad **snittpoäng 94 för desktop och 86** för mobil i PSI:s [mätning](https://docs.google.com/spreadsheets/d/e/2PACX-1vQNB-lynAGuAVDmTcj24qOPe6jS1s2pJG9qtQeec6qMPF4rO6TOwLbCxLcXUxe6nWtbcSW4ygbqKCRa/pubhtml), ett inte helt oävet resultat. Man ser redan här att det främst är frontsidan som drar ned betyget, och att resultatet för desktop är bättre än det för mobil – så brukar det se ut.

<iframe title="PSI" style="height: 40vh; width: 100%" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQNB-lynAGuAVDmTcj24qOPe6jS1s2pJG9qtQeec6qMPF4rO6TOwLbCxLcXUxe6nWtbcSW4ygbqKCRa/pubhtml?widget=true&amp;headers=false"></iframe>

![Seonmi art (mobil version)](%assets_url%/img/seonmi-mobile.webp)
*Seonmi art, mobila versioner*

### Lighthouse, server

I verkligheten laddas emellertid tema *mono* som **default** innan förvalt tema inträder i dess ställe (via javascript och local storage), vilket orskakar en del skiftningar i layouten och därmed poängavdrag. För skarp server [noteras](https://docs.google.com/spreadsheets/d/e/2PACX-1vRc6i1KIv51quIjba7BvYs3_vpnp6wX5SRICOtVLUFueyqYuUYVN9RrznYVQ5TN26F5fBGckwvps8UL/pubhtml) här **poängsumman 85 för desktop och 78 för mobil**, vilket är en förhållandevis markant minskning.

Försök att kringgå detta medelst olika metoder har inte visat sig fungera, utan ger tvärtom sämre resultat, å ena sidan att lägga alla grundstilar direkt som minifierad kod i huvudet, å den andra att ange en tom stilmall. Det är ett oväntat resultat som sporrar till fördjupad analys. Samtidigt noteras laddtider kring sekunden, vilket är fullt godtagbart.

<iframe title="Lighthouse, server" style="height: 40vh; width: 100%" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRc6i1KIv51quIjba7BvYs3_vpnp6wX5SRICOtVLUFueyqYuUYVN9RrznYVQ5TN26F5fBGckwvps8UL/pubhtml?widget=true&amp;headers=false"></iframe>

![Seonmi art (tema dark)](%assets_url%/img/seonmi-dark.webp)
*Seonmi art, tema **dark***

### Lighthouse, lokal server

Tillgängligheten prickar in 100 i poäng på varje sida i varje tema, medan skarp server bara genererar 79 för «bästa praktik» samt 69 för sökmotoroptimering. Detta är en konfigurationsfråga, bland annat avseende cache och HTTP/2 i Apache, och ligger därmed utanför webbutvecklarens räckvidd. På lokal server nås emellertid 100 för båda.

Däremot är det tämligen oväntat att lokal server ger [sämre](https://docs.google.com/spreadsheets/d/e/2PACX-1vQTpxWvIfy-H86AEPm1urKgz1m9XiPzbJQZLQErnbLsMRMjC4F2cJIuo_ZcHZIkWP3ZnF4Fq0FsH2C5/pubhtml) poäng i Lighthouse än PSI och skarp server, **81 för desktop samt 63 för mobil**, särskilt då felen är så mycket färre. Orsaken härtill är för närvarande inte känd.

<iframe title="Lighthouse, local server" style="height: 40vh; width: 100%" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQTpxWvIfy-H86AEPm1urKgz1m9XiPzbJQZLQErnbLsMRMjC4F2cJIuo_ZcHZIkWP3ZnF4Fq0FsH2C5/pubhtml?widget=true&amp;headers=false"></iframe>

![Seonmi art (tema triad)](%assets_url%/img/seonmi-triad.webp)
*Seonmi art, tema **triad***

Analys
-----------------------

Sämst presterar genomgående frontsidan, på grund av den stora hjältebilden i en rad beskärningar. Man får här göra en medveten avvägning mellan formgivning och prestanda. Bäst är å andra sidan galleriet, som består av över femtio bilder, om än i förutsägbara dimensioner.

Tekniker som har nyttjats för att optimera prestandan är främst att ange korrekt bildstorlekar i `srcset`, men samtidigt väljer webbläsaren ofta en bild med högre densitet, vilket genererar avdrag. Webbfonter tenderar att orsaka layoutskiftningar, men med så kallad swapteknik kan man reducera effekten genom att först rendera någon lokal font och därefter ersätta när sidan är fullt laddad.

![Seonmi art (tema tetrad)](%assets_url%/img/seonmi-tetrad.webp)
*Seonmi art, tema **tetrad***

Dynamisk och responsiv layout ger ofrånkomligen skiftningar som kan vara svåra eller omöjliga att parera helt. Det visar sig att bredare sidor presterar något bättre än smalare, nämligen för att skiftningen mäts vertikalt. Härav följer att grundtemat mono presterar bäst, då det saknar en angiven maximal vidd.

Det torde vara en grannlaga uppgift att råda bot i skiftningar som kanske ändå inte går att göra något åt med mindre att man är beredd att kompromissa radikalt med sin design, exempelvis att strunta i webbfonter. I undertecknads optik är prestandan godtagbar i givet skick, och man bör hellre lägga krutet på annat än att fåfängt jaga mikropoäng.

![Seonmi art (tema mono)](%assets_url%/img/seonmi-mono.webp)
*Seonmi art, tema **mono***
