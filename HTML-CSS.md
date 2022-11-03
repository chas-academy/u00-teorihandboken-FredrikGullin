# Teorihandboken - HTML & CSS (HC)
Studerande: Fredrik Gullin

## HC 1.1 HTML & CSS
HTML står för HyperText Markup Language och är en av webbens grundläggande byggstenar tillsammans med CSS (Cascading Style Sheets) och Javascript. Med användning av HTML kan man strukturera en webbsida med rubriker, styckeindelning samt för att strukturera upp sidans olika delar och innehåll. Man kan även infoga länkar, bilder och videos med HTML.

”Hypertext” refererar till länkar som kopplar ihop en webbsida med en eller flera andra webbsidor. Länkar är en fundamental aspekt av webben.

HTML-kod används endast för att ge struktur och saknar möjlighet att utföra kommandon. HTML är således ett märkspråk och inte ett programmeringsspråk. HTML är en sidas struktur och CSS är det man använder för att designa själva sidan. Javascript är det som används för att ge sidan olika typer av funktionalitet.

För att beskriva relationen mellan struktur, design skulle man till exempel effektivt kunna göra alla rubriker på en webbsida röda, märka upp dessa med HTML i sidans struktur för att senare kunna arbeta med och ändra just sidans rubriker i CSS.

_Detta kan se ut på följande sätt med HTML-kod och CSS:_


**HTML**        |**CSS**         |
----------------|----------------|
<h1>Rubrik</h1>	|h1 {color: red;}|
----------------|----------------|


Ovanstående kod skulle göra att alla rubriker på sidan, som märkts upp med <h1> taggen, till röda. Samma tänk används även när man ska ge sidan någon form av funktionalitet. Om man till exempel vill att något ska hända när man trycker på en knapp på sidan måste denna märkas upp med HTML för att kunna länkas till ett skript som utför det man vill ska hända.

HTML-struktur används även av sökmotorer. Information om en webbsidas innehåll, nyckelord (för sökbarhet) och författare läggs in i sidans ”huvud” och märks upp som metadata. En sökmotor kan därefter jämföra metadatan med en användares sökning och förstå om sidans innehåll är relevant och därefter presentera detta för användaren.

_Metadata kan se ut på följande sätt i ett HTML-dokument:_


<head>
	<meta charset=”UTF-8”>
	<meta name=”description” content=”Free web tutorials”>
	<meta name=”keywords” content=”HTML, CSS, Javascript”>
	<meta name=”author” content=”Fredrik Gullin”>
	<meta name=”viewport” content=”width=device-width, initial-scale=1.0”>
</head>


I ovanstående exempel kan en sökmotor förstå att webbsidan innehåller ”Free web tutorials” med nyckelorden HTML, CSS och Javascript samt att författaren av sidan heter Fredrik Gullin. Därefter jämför sökmotorn sidans metadata mot en användares sökning och om dessa matchar varandra förstår sökmotorn att det är relevant att presentera sidan som ett sökresultat.

_Källa 1:_ https://www.exsitec.se/blogg/vad-ar-html
_Källa 2:_ Föreläsning - Optimering / Validering av Sebastian Lindgren, Chas Academy den 29 september 2022

**Markup och taggar**
HTML använder ”markup” för att märka upp text, bilder och annat innehåll för att presentera detta i en webbläsare. HTML markup görs med särskilda element som till exempel <head>, <title>, <body>, <header>, <footer>, <article>, <section>, <p>, och <div> med flera.

Ett HTML-element urskiljer sig från övrig text i ett dokument genom att använda taggar, ”<” och ”>”. Ett element kan anges med både små och stora bokstäver eller till och med en blandning av dessa. Det är dock rekommenderat att använda små bokstäver.

_Källa 3:_ https://developer.mozilla.org/en-US/docs/Web/HTML


**CSS**
Cascading Style Sheets (CSS) är ett stylesheet språk som används för att designa och presentera informationen i ett HTML dokument. Med CSS kan man designa hur olika element ska visas på en skärm, på papper, i tal eller andra typer av media. CSS kan även användas med XML.

När det gäller webbutveckling används CSS för att lägga till styling och layout till en webbsida. Man kan till exempel ändra font, färg och storlek på textelement som vi gick igenom i föregående avsnitt. Man kan också hantera avstånd mellan olika delar av sidans innehåll och dela upp innehållet i olika kolumner eller lägga till animationer.

CSS är ett av webbens huvudsakliga språk och är en standard för webbläsare i enlighet med [W3C specifications](https://www.w3.org/Style/CSS/#specs). 

_Källa 4:_ https://developer.mozilla.org/en-US/docs/Web/CSS


**Inline CSS**
För att kunna använda CSS krävs en grundläggande förståelse för HTML och hur CSS används med ett HTML-dokuments underliggande struktur. För att applicera en viss design behöver CSS-koden peka på det HTML-element man vill korrigera.

_Detta kan se ut på följande sätt:_


<p>Jag är en vanlig paragraf!</p>

Man kan ändra färg på paragrafen genom att lägga in CSS-kod direkt i HTML-elementets start-tagg och på så vis göra  texten blå.

<p style=”color:blue”>Jag är en vanlig paragraf!</p>


Här använder vi attributet ”style” med ”color:blue” för att ändra paragrafens färg. På samma sätt kan man till exempel ändra textstorlek genom att byta ut ”color:blue” mot ”font-size:20px”. Textstorleken i paragrafen skulle i detta fall ändras till 20 pixlar. Samma mönster och struktur (”sak-att-ändra: ändringsvärde”) följs oavsett vad man vill ändra. Detta sätt att använda CSS kallas ”Inline CSS”.

Att använda Inline CSS kommer dock göra HTML-koden stökig och svår att underhålla och därför rekommenderas andra tillvägagångssätt.


**Internal CSS**
Ett annat alternativ är att använda ”Internal CSS” genom att, i HTML-dokumentet, använda style-taggen. Mellan <style> och </style> kan man lägga till CSS-kod.

_För att ändra paragraftexten till blå med Internal CSS kan man göra så här:_


<p>Jag är en vanlig paragraf!”</p>

<style>
	p {
		color: blue;
	}
</style>


**External CSS**
Man kan använda External CSS genom skapa en separat CSS-fil som man hänvisar till från HTML-dokumentet.

_Detta görs genom att länka till CSS-filen i sidans huvud och kan se ut på följande sätt i HTML:_


<head>
	<link rel=”stylesheet” href=”style.css”>
</head>


På detta sättet förstår webbläsaren att den ska applicera de CSS-regler som finns i CSS-filen på HTML-dokumentet som ska visas.

_För att göra paragraftexten blå med External CSS kan man gå tillväga på följande sätt:_


HTML							 |CSS
---------------------------------|----------------|
<p>Jag är en vanlig paragraf!</p>|p {color: blue;}|
---------------------------------|----------------|

_Detta skapar dock en regel som ändrar dock färgen på alla ”p-element” i hela HTML-dokumentet._


**Class**
Om man vill ändra textfärg i en specifik paragraf kan man använda sig av en klass i HTML-dokumentet för just det element du vill ändra.

_En klass i HTML skapas så här:_


<p class=”blue”>Jag är en vanlig paragraf!</p>


_Nu har vi skapat en klass som heter ”blue”. Klassen pekas ut i CSS-koden genom att skriva punkt följt av klassens namn och ser ut så här:_


.blue {color: blue;}


På det här sättet har vi endast ändrat färg på den paragraf som hör till klassen ”blue”. Detta kan göras både i Internal- och External CSS. En klass kan användas för att tilldela en mängd olika egenskaper till olika element i HTML-dokumentet.

Detta var en kort beskrivning av HTML och CSS. För att läsa mer om detta besök [MDN](https://developer.mozilla.org/en-US/).

_Källa 5:_ https://www.exsitec.se/blogg/vad-ar-css

## HC 1.2 Responsiv design
Innan konceptet för responsiv design var webbsidor byggda för att passa en specifik skärmstorlek. Om användaren hade en större eller mindre skärm än vad designen avsåg kunde detta leda till en rad oönskade resultat, som till exempel att användaren var tvungen att scrolla sig igenom sidan på ett onaturligt sätt för att ta del av innehållet, eller överdrivet långa textremsor. Med tiden utvecklades ett större antal skärmar med olika storlekar och med det utvecklades även konceptet för responsiv design.

Responsiv design är en metod som gör webbsidor responsiva så de fungerar på olika skärmstorlekar. Detta innebär att sidans layout förändras och anpassas efter användarens skärmstorlek, bredd och upplösning med mera. Detta koncept förändrade sättet vi utvecklar hemsidor med anpassningar för ett internet med en mängd olika enheter.

Innan responsiv design existerade i sin nuvarande form har utvecklare försökt lösa problem med huruvida webbsidor kan anpassas till olika skärmstorlekar på olika sätt. HTML är generellt responsivt och texten på en webbsida kommer anpassas efter en enhets skärmstorlek. Detta kallas ”liquid layout”. Problemet med denna layout är att webbsidan skulle se ihoptryckt ut på en mindre skärm eller att textraderna skulle bli väldigt långa och därav svårlästa.

För att komma runt detta problem försökte utvecklare ett nytt tillvägagångssätt genom att ge sidans element en bestämd pixelbredd. Detta kallas ”fixed width layout”. Problemet med detta tillvägagångssätt är att användaren behöver scrolla horisontellt för att se hela innehållet när skärmbredden är mindre än själva websidan, samt att det uppstår flera tomrum på sidan när man använder en större skärm.

När det mobila internet blev en verklighet i samband med att mobiltelefonin utvecklades brukade företag bygga två webbsidor, en anpassad för datorer och en anpassad för mobiltelefoner. Sidorna som var anpassade för mobiltelefoner var dock ofta väldigt ofta en nedbantad version av hemsidan, vilket ledde till frustration över att mobilanvändare inte hade tillgång till all information som fanns på företagets datoranpassade hemsida. Detta innebar även att man behövde uppdatera och underhålla två sidor istället för en.

Termen ”responsiv design” etablerades av Ethan Marcotte under 2010 och beskrev ett tillvägagångssätt som kombinerade 3 olika tekniker. Ethan förespråkade användningen av fluid grids, fluid images och media queries för att komma runt problemen med responsivitet.

Media queries
Användandet av media queries var en av nyckelfaktorerna till att responsiv design blev en vedertagen standard när det kommer till webbutveckling.

En media query fungerar på följande sätt:

Utvecklaren anger ett villkor som till exempel minimum bredd för en skärm. Om villkoret är uppfyllt ska ett antal CSS regler tillämpas. Reglerna anges direkt i själva media queryn.

**Till exempel:**

@media screen and (min-width: 800px){
	.container {
		margin: 1em 2em;
	}
}

I detta exempel är villkoret att minimum bredden för en skärm ska vara 800 pixlar ska vara uppfyllt för att CSS reglerna för klassen container ska vara: margin: _1em 2em_.

Om skärmbredden är mindre än 800 pixlar så är villkoret ej uppfyllt och därmed gäller de ursprungliga reglerna för klassen container.

Media queries läggs till i slutet av CSS koden. Detta då koden läses uppifrån och ner. Om en media query skrivs mitt i koden kan den bli åsidosatt av senare regler i dokumentet och därför inte fungera. Man kan ha flera media queries för att lägga till flera brytpunkter för att anpassa webbsidan olika regler för flera olika skärmstorlekar.

Responsiviteten i webbsidor bygger inte enbart på brytpunkter och media queries, de använder även på responsiva designmetoder som till exempel multiple-column layout, flexbox och grid.

En grid är generellt responsiv för att underlätta då man redan gjort antagandet att utvecklare vill använda responsiva metoder när de skapar webbsidor.

Multiple-column layout är den äldsta av dessa metoder. Utvecklaren anger ett antal kolumner (column-count) som innehållet på sidan ska delas upp i. Webbläsaren kommer därefter räkna ut storleken på dessa i förhållande till användarens skärm.

I en flexbox kommer flex-föremål initialt krympa och distribuera utrymme mellan varandra enligt det utrymme som finns tillgängligt i själva flex-boxen. Man kan styra hur föremålen beter sig i flex-boxen när de får mer, eller mindre, utrymme runt omkring sig genom att ändra värden för flex-grow och flex-shrink.

Utöver dessa metoder kan man även använda responsiva enheter som procent (%), em, rem, vh och vw för att göra olika element (boxar, text och bilder) responsiva.

_Källa:_ https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design

## HC 1.3 Tillgänglighet inom webb
Tillgänglighet inom webbutveckling syftar till att tillgängliggöra till exempel en webbsida, en applikation eller ett system för personer med olika grad av funktionsnedsättning. Detta är en viktig del av utformning av en webbsida och bör beaktas under hela utvecklingsprocessen.

Tillgänglighetsanpassade webbsidor presenterar information genom flera sensoriska kanaler, så som ljud och syn, och de möjliggör  ytterligare sätt för webbplatsnavigering och interaktivitet utöver det typiska ”peka och klicka” gränssnittet, som tangentbordsbaserad kontroll och röstbaserad navigering. Kombinationen av ett multisensoriskt tillvägagångssätt med mångsidig interaktivitet tillåter personer med funktionsnedsättning att ta del av samma information som icke-funktionsnedsatta användare.

Genom att göra din webbsida tillgänglighetsanpassad ser du till att alla dina potentiella besökare, inklusive personer med funktionsnedsättning, har en anständig användarupplevelse och har tillgång till all information som presenteras på sidan. Detta förbättrar även webbsidans användbarhet för alla användare.

**När man skapar digitalt innehåll som till exempel webbsidor bör man överväga följande riktlinjer:**

    * Förlita dig inte enbart på kontrast och färger som det enda sättet att navigera sidan
    * Bilder bör ha en ”alt text” i HTML-koden som beskriver vad bilden föreställer
    * Funktionalitet bör vara tillgänglig genom både mus och tangentbord och även vara ”taggad” för att fungera med röstbaserade styrsystem
    * Inkludera text för ljudet på podcasts eller videor
    * Webbsidan bör ha en funktion för att hoppa över avsnitt
    * Webbsidan ska uppfylla riktlinjerna i WCAG 2.1 nivå AA
    * Övervägg att testa din webbsidas tillgänglighet med ett verktyg

WCAG står för ”Web Content Accessability Guidelines” och är en internationellt etablerad och rekommenderad standard för tillgänglighetsanpassning inom webbutveckling. Standarden är framtagen av World Wide Web Consortium (W3C) och sammanställer kunskaper från ett stort antal användare och experter.

Den 23 september 2018 trädde Webbtillgänglighetsdirektivet i kraft i Sverige och alla EU-länder. Lagen omfattar hela den offentliga sektorn samt statliga och kommunala bolag som uppfyller vissa krav. Lagen innebär att webbplatser, extranät, intranät, dokument och appar ska uppfylla kraven på tillgänglighet i EN301549.

_Källor:_

https://www.usability.gov/what-and-why/accessibility.html
https://webbriktlinjer.se/lagkrav/folj-standarder-tillganglighet/
https://www.funka.com/design-for-alla/lagar-och-regler/

## HC 1.4 Aktuella webbstandarder (gällande och kommande standarder)
Webbstandarder kan ses som gängse rekommendationer från World Wide Web Consortium (W3C) med andra standardiseringsorgan och beskriver hur webbaserat innehåll ska skapas, presenteras och tolkas. Standarder för detta har funnits sedan webben började utvecklas men har under senare år blivit ett vedertaget begrepp och uppnått ett brett stöd i de större webbläsarna.

Genom att följa en webbstandard när man utvecklar en webbplats så kan man vara mer säker på att koden även kommer fungera i kommande webbläsare. Standarden avser även att underlätta för användare som är beroende av olika verktyg så som skärmläsarprogram och punktskriftshjälpmedel.

Utöver detta finns ett flertal fördelar med att följa rekommenderade webbstandarder när man utvecklar en webbplats. Man kan exempelvis minska kostnader för utveckling och förvaltning av webbplatsen då det går snabbare att sätta sig in i hur en webbplats är uppbyggd och fungerar om den följer riktlinjerna i allmänt vedertagna standarder, speciellt om det är ett större projekt med ett flertal utvecklare i ett team. Genom att till exempel separera webbplatsens innehåll och presentationen av innehållet blir ändring av utseendet av webbplatsen enklare. Sidans svars- och laddningstiden blir snabbare då filstorleken enligt standard för optimering minskar.

HTML5 blev, efter flera års arbete, en ”W3C recommendation” i oktober 2014. Det innebär att specifikationen är en färdig webbstandard. HTML5 är den gällande standarden som utvecklas kontinuerligt och stöds redan av alla moderna webbläsare och är även bakåtkompatibel med äldre versioner.

När man utvecklar en webbplats bör man även anpassa sidan till tidigare versioner, men till en viss gräns. I första hand testar man sidan mot de senaste versionerna av webbläsare. Detta då webbläsare utvecklas snabbt och de flesta uppdateras automatiskt. Tillverkarna blir dock allt bättre på att följa standarder men överväg att se till att sidorna även fungerar på lite äldre versioner.

Utvecklare har ingen skyldighet att anpassa webbplatsen efter webbläsare som grovt avviker från standarden, som till exempel flera år gamla webbläsare.

**Rekommenderad standard**
    * Använd HTML5. HTML version 5 är den senaste versionen och har bra stöd i de flesta verktyg.
    * Använd inte XHTML om det inte finns synnerliga skäl till detta.

För att kontrollera om sidan i fråga följer den standard man valt för uppmärkningskoden kan man använda W3C:s valideringsverktyg (http://validator.w3.org).

**Kommande standarder**
HTML5 blev som sagt en standard i oktober 2014 och har sedan dess utvecklats kontinuerligt av ”the whatWG community” som också har bekräftat att HTML6 är på väg. Detta är dock en process som kommer ske över tid och allt släpps inte på en gång.

**Man antar att HTML6 kommer innehålla följande funktioner:**

    * Express tags – Taggar som är mer semantiskt korrekta som <logo> för logga, <sidebar> för en sidebar med mera, istället för att använda <div class=””>.
    * Native Modals Support - <dialog> elementet är på väg med HTML6. Kan jämföras med JavaScript-drivna modala fönster.
    * Freedom to Resize Image – Möjligvis en ny tag <srcset> vilket i teorin skulle möjliggöra för browsers att välja mellan flera bilder för bästa resultat på olika skärmar / webbläsare.
    * HTML6 Dedicated Libraries – Introducerar bibliotek som sparas i cach-minnet vilket förbättrar upplevelsen för både utvecklare och användare.
    * Annotation for images and videos – Möjliggör tolkning av bilder och videos.
    * Authentication enhancement – Användning av ”embedded keys” istället för cookies etc.
    * Customized Menus in HTML6 – En meny tag som kan hantera interaktivitet på ett bättre sätt än listor.
    * HTML6 Integrated Camera – Bättre stöd för användning av kameran på exempelvis en mobiltelefon.
    * Good Microformats – Standarder som är kapabla att definiera generell data för att förbättra sökbarheten.

Enligt whatWGs blogg är detta vad som framgår av användarnas önskemål. Vad som slutligen kommer finnas med i HTML6 återstår att se.

_Källor:_
https://www.happiness.se/artiklar/vad-ar-webbstandarder
https://webbriktlinjer.se/riktlinjer/81-utveckla-webbplatsen-enligt-en-standard-snarare-an-for-en-webblasare/
https://www.positronx.io/html6-is-coming-here-is-a-sneak-peek/
## HC 1.5 CSS Pre-processorer (ex SASS/LESS)
Beskriv rubriken nedan här

## HC 1.6 Optimering och validering av HTML & CSS
Beskriv rubriken nedan här
