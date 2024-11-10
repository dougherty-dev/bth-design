---
Title: om
Description: Om webbplatsen.
---

# om

***Designkursen*** omfattar ett antal grundläggande tekniker för hantering av stil, färg, typografi, användarvänlighet med mera, givet en befintlig struktur. Här utgår vi från markdown renderad i HTML av **Pico** med **Twig** som mallfabrik, varefter stilscheman definieras och kompileras med SASS till slutlig CSS-fil.

För **SASS** använder vi nästlade definitioner samt lämpliga kortformer som *font*. Även variabler nyttjas för färger och en del andra vanliga definitioner, som ramar och mediaelement.

Modulering medelst @import nyttjas för koncis hantering av stilscheman, även om @use tillsammans med CSS-variabler hade varit en mer stilren lösning. Noterbara stilelement är bland annat en inledande anfang i brödtexten; nyttjande av kolumner, grid och flexbox för responsiv rendering; mörkt grundtema; samt webbfonter (woff2).

För typsnitt nyttjas **Franklin** i tunt grundutförande som brödtext, ett klassiskt linjärt snitt med höggradig läsbarhet, samt **Bodoni** för rubriker, en populär antikva som bland annat figurerar i Dagens Nyheters logotyp.

Av rättighetsskäl nyttjas Googles öppna varianter snarare än kommersiella snitt från Linotype eller Adobe. På denna sajt fokuserar vi på läsbarhet, medan mer aktiv typografi och vackra snitt nyttjas i andra kurser (se sidfot).

![Palett för ursprungligt färgtema](%assets_url%/img/palett.avif){.nofilter}

**Färgpaletten** extraheras ur en bit grillat kött, med mörka och grå kulörer i kombination med rött, orange och gult, som vi medelst **Paletton** flätar samman i ett analogt eldigt tema inklusive en kompletterande blå kulör samt två monokroma kontrastfärger med nyanser. Det mörka grundtemat kompletteras med ett ljust medelst sessionshantering. För mörkt tema dras kontrast upp och ljusstyrka ned ett snäpp.

![Utgångsbild för tema](%assets_url%/img/stek.avif)

Egentligen kunde vi ha gått på känsla och behållit den gröna nyansen som en fjärde analog, men för sakens skull följer vi här protokollet. För ikoner nyttjar vi en pur lösning i Unicode istället för stora och klumpiga lösningar medelst fontfiler. Vi nyttjar även en rad specifika SVG-ikoner.

![Paletter för färgtema ](%assets_url%/img/paletter.avif){.nofilter}
