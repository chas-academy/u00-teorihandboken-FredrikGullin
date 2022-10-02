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

_Källa 1: https://www.exsitec.se/blogg/vad-ar-html_
_Källa 2: Föreläsning - Optimering / Validering av Sebastian Lindgren, Chas Academy den 29 september 2022_

**Markup och taggar**
HTML använder ”markup” för att märka upp text, bilder och annat innehåll för att presentera detta i en webbläsare. HTML markup görs med särskilda element som till exempel <head>, <title>, <body>, <header>, <footer>, <article>, <section>, <p>, och <div> med flera.

Ett HTML-element urskiljer sig från övrig text i ett dokument genom att använda taggar, ”<” och ”>”. Ett element kan anges med både små och stora bokstäver eller till och med en blandning av dessa. Det är dock rekommenderat att använda små bokstäver.

_Källa 3: https://developer.mozilla.org/en-US/docs/Web/HTML_


**CSS**
Cascading Style Sheets (CSS) är ett stylesheet språk som används för att designa och presentera informationen i ett HTML dokument. Med CSS kan man designa hur olika element ska visas på en skärm, på papper, i tal eller andra typer av media. CSS kan även användas med XML.

När det gäller webbutveckling används CSS för att lägga till styling och layout till en webbsida. Man kan till exempel ändra font, färg och storlek på textelement som vi gick igenom i föregående avsnitt. Man kan också hantera avstånd mellan olika delar av sidans innehåll och dela upp innehållet i olika kolumner eller lägga till animationer.

CSS är ett av webbens huvudsakliga språk och är en standard för webbläsare i enlighet med [W3C specifications](https://www.w3.org/Style/CSS/#specs). 

_Källa 4: https://developer.mozilla.org/en-US/docs/Web/CSS_


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

_Källa 5: https://www.exsitec.se/blogg/vad-ar-css_

## HC 1.2 Responsiv design
Beskriv rubriken här

## HC 1.3 Tillgänglighet inom webb
Beskriv rubriken nedan här

## HC 1.4 Aktuella webbstandarder (gällande och kommande standarder)
Beskriv rubriken nedan här

## HC 1.5 CSS Pre-processorer (ex SASS/LESS)
Beskriv rubriken nedan här

## HC 1.6 Optimering och validering av HTML & CSS
Beskriv rubriken nedan här
