---
Title: Webbplatsdesign och aktuella trender
Description: Webbplatsdesign och aktuella trender
svg: trend
Template: analysis
---

Webbplatsdesign och aktuella trender
=======================

Företaget *Sök Under* har inkommit med hemställan om en undersökning kring aktuella trender med avseende på webbdesign, utan att närmare precisera begreppet. Uppdraget är därmed behäftat med stor frihet att utföra en självständig analys i ämnet, och vi väljer för ändamålet trenne aspekter av intresse.

Den första rör förekomsten av **mörkt tema** på en webb präglad av bländande vitt. Man har sedan webbens större etablering i mitten av 1990-talet sökt emulera papper som underliggande medium, men det rör sig i själva verket om diametralt olika ljuskällor. I bokens fall reflekteras omgivningens ljus med dämpning, varför ögonen inte lider skada, medan skärmen emitterar ljus med en styrka som i regel överträffar ambient nivå, vilket kan leda till ansträngning, särskilt vid frekvent bruk.

Av den senare anledningen noteras typiskt hur användare drar ned ljusstyrkan, framförallt på mobila skärmar. Detta även för att spara ström, då skärmutstrålning är den största källan till kort batteritid. Med minskad ljusstyrka framträder emellertid färger mindre klart, varför helhetsupplevelsen blir en smula dämpad. Mörkt tema löser båda dessa problem, och är således idealt för rikare innehåll.

Den andra aspekten tar avstamp i en betydligt äldre företeelse kring **responsiv design**, men den är å andra sidan ständigt aktuell på en webb som ska passa allt fler upplösningar och dimensioner för olika slags enheter, från ultravida stationära bildskärmar i 8K till de minsta mobilskärmar i vertikalt grundläge. En vanlig metod är att erbjuda skilda versioner beroende på enhetstyp, men här vill vi veta hur elastisk sajten är för *stationära* enheter.

Slutligen studerar vi hur **sidfoten** har formgivits, då denna del av webbsidan ligger allra längst ned i flödet. Har man verkligen tvättat och sörjt för fötterna, eller är det en illaluktande detalj som man har försummat för ett fåfängt ytligt ideal kring det mer synliga huvudet?

Urval
-----------------------

Vi väljer här att förlägga undersökningen till de fem största nyhetstidningarna i Sverige, räknat efter pappersupplaga. Det är medier som lägger stor vikt vid design och funktionalitet på sina plattformar, och de är därför mer relevanta än exempelvis myndighetssidor vad avser trender kring webbdesign. De fem drakarna är i fallande ordning: [Dagens Nyheter](https://www.dn.se/), [Aftonbladet](https://www.aftonbladet.se/), [Expressen](https://www.expressen.se/), [Svenska Dagbladet](https://www.svd.se/) och [Göteborgs-Posten](https://www.gp.se/).

Man kan notera att Schibsted ligger bakom såväl Aftonbladet som Svenska Dagbladet, och att Bonniers på motsvarande vis förfogar över både DN och Expressen, varför man kan förmoda att det finns beröringspunkter mellan de olika plattformarna inom samma koncern.

Metod
-----------------------

De första aspekterna kring **mörkt tema** och **responsiv design** bereder inga större svårigheter, utan är enkla att koncist sammanfatta i några få ord. Vi betraktar huruvida sajten i fråga stödjer mörkt tema med automatik baserat på operativsystemets inställningar, eller om man erbjuder en manuell inställning. På samma sätt undersöker vi hur responsiv respektive sajt är i ett antal konfigurationer.

 Hur **sidfoten** är utformad är däremot mer komplicerat, då det finns ett antal företeelser av vikt att hålla reda på. Här vill vi veta om det rör sig om en *fet och detaljerad* eller en *smal* fot, eller för den delen *obefintlig*. Har sidfoten inkorporerat tidningens *logotyp*? Nyttjar man *ikoner* för *sociala länkar*, och i så fall vilka?

 Vidare vill vi veta huruvida man nyttjar någon form av *aktiv typografi* i designen av sidfoten, som någon fristående bild eller mer flytande element. Är sidfoten formmässigt *integrerad* med övrigt material på sidan?

Resultat
-----------------------

### Dagens Nyheter

#### Mörkt tema

Tidningen erbjuder inget mörkt tema för vare sig desktop- eller mobilversion. Designen går i traditionellt monokromt vitt och svart med sparsamt inslag av röda element, varför det skulle vara en smal sak att implementera ett mörkare alternativ via några extra stilregler och en kaka.

#### Responsiv design

Layouten är primärt given i tre kolumner på frontsidan: artiklar, sidospalt samt en reklamkolumn längst till höger. För enskilda artiklar försvinner sidospalten, varvid två kolumner kvarstår. En viss plasticitet finns i så måtto att reklamkolumen kollapsar vid minskning av bredden, men övrigt material har en minimal vidd om 1008 pixlar, under vilken gräns en skrollist framträder.

![Responsivitet Dagens Nyheter](%assets_url%/img/responsivitet-dn.webp){.nofilter}
*Horisontell skrollist*

Till yttermera visso har man en absolut maximal vidd om 1340 pixlar, inklusive reklamkolumn, vilket ger en stel och statisk formgivning som inte skalar mer än på marginalen. Tidningen misslyckas helt i fråga om responsivitet.

![Fullvidd Dagens Nyheter](%assets_url%/img/fullvidd-dn.webp){.nofilter}
*Statisk bredd, stel layout*

#### Sidfot

Foten är fet och ges av fyra plus två plus en kolumner, men utan elasticitet då bredden är statiskt satt till 1180 pixlar. Här råder emellertid invers färgsättning med vit text på mörkare bakgrund. Logotyp finns, likväl som sociala länkar, även om ikonerna för de senare saknas. Det rör sig mest om obligatorisk och rudimentär information, och någon spännande typografi kan man inte skönja här.

![Sidfot Dagens Nyheter](%assets_url%/img/sidfot-dn.webp){.nofilter}
*Standardfot*

### Aftonbladet

#### Mörkt tema

Mörkt tema erbjuds i menyn, men bara för den innevarande sidan, eller permanent i inloggat läge – ett märkligt grepp. Desktop- och mobilversioner är härvidlag identiska.

![Sidfot Aftonbladet](%assets_url%/img/tema-ab.webp){.nofilter}
*Aftonbladet ser mörkt tema som en plustjänst*

#### Responsiv design

Tidningen lägger sig på 1294 pixlar i maximal vidd, med artikelflöde och sidospalt. Man har därvid samma begränsning som kollegan ovan, men man skalar å andra sidan exemplariskt ned till minsta möjliga bredd. Godkänt.

#### Sidfot

Tidningen latladdar ett oändligt flöde av sensationsjournalistik, men slutligen hamnar man ändå på något slags sidfot, som dock inte är mycket att visa upp. Logotyp saknas, och man har istället en siluett av grundarfiguren. I övrigt är informationen minimal, och här finns inte tillstymmelse till aktiv eller annan typografi.

![Tema Aftonbladet](%assets_url%/img/sidfot-ab.webp){.nofilter}
*En smutsig fot*

### Expressen

#### Mörkt tema

Ljust och mörkt färgtema erbjuds i toppmenyn, därtill med en automatisk inställning (via `prefers-color-scheme` i CSS). Föredömlig hantering i både desktop- och mobilversion, och medier som önskar läsare som stannar längre vid sajten borde ta efter.

![Tema Expressen](%assets_url%/img/tema-expressen.webp){.nofilter}
*En lösning som manar till efterföljd*

#### Responsiv design

Sidbredd för två kolumner anges här i koden till 992 pixlar, och den är helt statisk. I praktiken ströbläddrar man kanske kvällstidningar i normal fönsterbredd, men det känns ändå gammalmodigt. Man har redan den erforderliga koden i mobilversionen, och man kunde därför slå samman till en enda.

![Responsivitet Expressen](%assets_url%/img/responsivitet-expressen.webp){.nofilter}
*Horisontell skrollist*

#### Sidfot

Likt grannen i Bonnier-skrapan har man en statisk sidfot, här i tre kolumners utförande över några rader. Fet till formen, men fattig till innehållet. Man har i vart fall en logotyp och en enstaka ikon till den enda sociala länken X. Inte heller mobilversionen skalar, utan är satt i en vänsterställd kolumn, samtidigt som loggan är centrerad. Utformningen är dock harmoniserad med avseende på färger och andra element.

![Sidfot Expressen](%assets_url%/img/sidfot-expressen.webp){.nofilter}
*Fet men tom sidfot*

### Svenska Dagbladet

#### Mörkt tema

Tidningen är konservativt lagd till ideologin, och så även i designen. Något mörkt tema erbjuds således inte, vare sig i desktop- eller mobilversion.

#### Responsiv design

Vidden maxar ut vid 1298 pixlar men är i övrigt föredömligt responsiv. Sidfoten följer dock med hela fönsterbredden.

#### Sidfot

Tidningen har en ganska fet sidfot, initialt i fyra plus två kolumner, vilka skalar föredömligt med ändrad sidbredd. Logotyp finns, likväl som en dekorativ ikon för kundtjänstfunktionen. Fem sociala länkar ges, men utan tillhörande ikoner. Bakgrunden är blå med vit förgrundstext, i kontrast till och i harmoni med övrigt innehåll. Godkänt.

![Sidfot Svenska Dagbladet](%assets_url%/img/sidfot-svd.webp){.nofilter}
*Proper men funktionell sidfot*

### Göteborgs-Posten

#### Mörkt tema

Inte heller rikets framsida erbjuder på sin portalsajt en mörk design som tillval, utan traskar i gamla invanda spår.

#### Responsiv design

En grid om 1332 pixlar definierar tre kolumner *(main main sidebar)*, med 980 pixlar reserverade för redaktionellt material. Nedskalning till 200 pixlar sker utan problem, med kollaps av sidospalt.

#### Sidfot

Göteborgstidningen har i vart fall finast fotarbete, med en halvfet och ganska skönt formgiven gestaltning i fyra kolumner som skalar exemplariskt, inklusive byte från vänsterställd till centrerad modell. Informationen är dock tunn, och de tre sociala länkarna saknar ikoner. Det är ändå en klar vinnare i detta skrala fält, trots den överlånga sista raden.

![Sidfot Göteborgs-Posten](%assets_url%/img/sidfot-gp.webp){.nofilter}
*Harmonisk sidfot, och bäst i test*

Analys
-----------------------

### Mörkt tema

Nyhetsplatserna ligger i allmänhet långt efter sociala medier, videotjänster och tekniksajter i fråga om ett erbjuda modern formgivning med alternativ för mörkt tema. Ändå är det mest en fråga om enkla förändringar i stilscheman, och kräver alltså inte en radikal nydesign. Ikoner, logotyper med mera är sedan länge i vektor- eller transparent rasterformat, varför det inte erbjuder några problem att invertera modellen.

Traditionen lever stark, och man vågar kanske inte rubba på invanda koncept. Men eftersom det är en valfri företeelse, torde det inte ha någon inverkan på affärsmodellen – i vart fall inte någon negativ. Redaktionsmedarbetare använder oftast själva mörkt läge på sin enhet, men man kanske betraktar läsarna med ett annat raster.

### Responsiv design

Två paradigm kristalliserar här ut sig, å ena sidan en helt statisk äldre modell kring en sidbredd om 1000–1300 pixlar, representerad av Bonniers båda flaggskepp DN och Expressen, och å den andra en mer modern responsiv som skalar elastiskt ned till minsta realistiska fönstervidd.

Det senare är en rationell metod, och det kan finnas goda skäl att i allmänhet sätta en övre gräns. Men samtidigt har vi här att göra med tidningar, som traditionellt sätter sitt material över ett stort antal kolumner. Här skulle man vilja se nyare grepp via `flex`, `grid` och `columns` för att låta artikelmassan flöda över ett godtyckligt antal kolumner, inte bara en eller två, utan åtta, tolv eller rent av tjugo för riktigt stora bildskärmar.

![Pappersversion Dagens Nyheter](%assets_url%/img/dn-papper.webp){.nofilter}
*Traditionell tidningssättning, grid med åtta kolumner*

Tekniken finns, även om det innebär en del huvudbry att integrera en sådan modell i en redaktionell miljö som omfattar ett stort antal medarbetare. Å andra sidan är dessa system ofta så komplexa att det blir svårt att implementera en ny design utan att bygga helt nytt, och det är i regel en dyr historia.

### Sidfot

Statistik har att över hälften av all tid läggs på sidans översta del, med fallande andelar ju längre ned i skrollfältet man kommer. Sidfoten ägnas sällan någon uppmärksamhet, och av det skälet lämnas den ofta i sticket vid utformningen. Men den seriösa designern släpar inte fötterna efter sig, utan lägger lika stor vikt vid alla delar, och i sanningens namn kostar det inte så mycket att en gång för alla formge denna tämligen statiska del av sidan.

Mer relevanta funktioner läggs numera i en utfälld meny i helsideläge, och sidfoten har därför på sätt och vis förlorat sin roll som informationsbärande enhet. Men den har fortfarande formmässig relevans i syfte att markera avslut och rama in produkten, ungefär som en etikett på en flaska vin.
