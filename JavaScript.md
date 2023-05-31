# Teorihandboken - JavaScript (JS)
Studerande: Fredrik Gullin

## JS 1.1 JavaScript / ECMAScript
JavaScript är ett programmeringsspråk som används för att skapa interaktiva och dynamiska webbsidor. Det introducerades av Netscape Communications i december 1995 och har sedan dess blivit ett av de mest populära språken inom webbutveckling.

JavaScript möjliggör att man kan interagera med webbsidor genom att lägga till interaktivitet, dynamiska effekter och manipulation av innehåll. JavaScript används ofta för att skapa funktioner som formulärvalidering, animationer, API-anrop och DOM-manipulation med mera. JavaScript körs direkt i webbläsaren på klientsidan (frontend). JavaScript är tillsammans med HTML och CSS webbens grundläggande byggstenar.

Ett vanligt användningsområde för JavaScript är att bestämma vad som ska hända när en användare interagerar på olika sätt med en webbsida. Detta görs ofta med en så kallad "event listener" vilket innebär att applikationen "lyssnar" på vad användaren gör, t.ex. scrollar på sidan, klickar på ett specifikt fält eller börjar fylla i ett formulär. Detta plockas upp av olika event listeners som därefter genererar en respons. _Mer om detta under punkten "Event handling"..._

**ECMAScript**
ECMAScript är den officiella standarden gör JavaScript som fastställs av ECMA International, en organisation som utvecklar standarder inom information och kommunikationsteknik. ECMAScript definierar språkets syntax, funktioner, objektmodell samt andra detaljer för att säkerställa att JavaScript-implementeringar är kompatibla och konsekventa över olika plattformar och webbläsare.

Nya ECMAScript-versioner släpps löpande med nya funktioner och förbättringar. ECMAScript 6 (även känd som ES6) var en betydande uppdatering som införde viktiga förbättringar och nya funktioner samt blockomfattande deklarationer, arrow-funktioner, klasser, moduler med mera.

De senare versionerna av ECMAScript har också introducerat många användbara funktioner så som _destrukturering, spread-operator, async / await, klassmetoder och moduler_, som förbättrar språkets funktionalitet och möjliggör mer effektiv och läsbar kod.

_Källa: https://www.exsitec.se/blogg/vad-ar-javascript_

_Källa: https://en.wikipedia.org/wiki/ECMAScript_ 

## JS 1.2 JavaScript-ramverk och -bibliotek
Det finns flera ramverk (frameworks) och bibliotek för JavaScript så som Angular, React, Vue, NextJS och Express.js med mera, där Angular, React och Vue är de tre största.

Då vi under utbildningen har fokuserat på Angular, React och Express tänkte jag passa på att kortfattat beskriva dessa.

**Angular**
Angular är ett "open source" ramverk som egentligen är baserat på TypeScript (Typad JavaScript) som utvecklats av Google. Angular används för att bygga kraftfulla och komplexa webbapplikationer. Med Angular kan utvecklare skapa allt från enkla till avanecrade applikationer genom att dra nytta av funktioner som databinding, komponentbaserad arkitektur samt enkel hantering av routing. Angular stöttar även enhetstester. Angular i sig erbjuder även en väldefinierad struktur och "best practice" som hjälper till med skapandet av robusta och skalbara applikationer.

De främsta fördelarna med Angular är strukturen som följer med och att Angular erbjuder en helhetslösning.

**React**
React är ett populärt "open source" ramverk som används för att bygga användargränssnitt i JavaScript. React har utvecklats av Facebook under 2011 och används för att skapa interaktiva och dynamiska webbapplikationer. React använder en komponentbaserad arkitektur, vilket i och för sig inte är unikt för React, men det sätt som det är implementerat på, gör det enkelt att återanvända och underhålla kod. React erbjuder även "virtual DOM" (Document Object Model) för effektiv uppdatering av användargränssnitt. React är också flexibelt och kan användas för att bygga både enkla komponenter och stora applikationer med hjälp av olika verktyg och bibliotek.

De främsta fördelarna med React är möjligheten att dela upp störa projekt i mindre hanterbara delar samt återanvändning av funktioner.

Idag hittar du React.js hos företag som Apple, Paypal, Netflix och såklart Facebook.

**Express**
Express är ett snabbt och minimalistiskt webbramverk för Node.js. Det används för att bygga webbapplikationer och API:er med hjälp av JavaScript eller TypeScript. Express erbjuder enkel hantering av routing, middleware och HTTP-requests. Det ger utvecklare frihet att strukturera och organisera sin kod på ett sätt som passar deras behov. Med stöd för olika tillägg och moduler kan Express utökas med extra funktioner och integreras smidigt med databaser och andra verktyg. Det är ett kraftfullt verktyg för att skapa effektiva och skalbara webbapplikationer.

De främsta fördelarna med Express.js är dess breda utbud av funktioner och verktyg samt att det erbjuder en kraftfull och enkel arkitektur som gör utvecklingen snabb och enkel.

_Källa: https://en.wikipedia.org/wiki/Angular_
_Källa: https://limetta.se/tips-metoder-for-digitala-projekt/vad-ar-react-javascript-ramverk/_
_Källa: https://limetta.se/tips-metoder-for-digitala-projekt/vad-ar-react-javascript-ramverk/_


## JS 1.3 Promises
Promises inom JavaScript är ett koncept för att hantera asynkron kod och hanteringen av resultat från asynkrona operationer som API-calls eller databasförfrågningar. 

_Asynkron kod är kod som körs oberoende av det vanliga programflödet. Istället för att blockera exekveringen av resten av koden och vänta på att en operation ska slutföras, tillåter asynkron kod att andra instruktioner kan köras samtidigt medan den asynkrona operationen pågår i bakgrunden. Det gör det med andra ord möjligt att hantera och svara på händelser och resultat på ett effektivt sätt utan att blockera eller fördröja andra delar av programmet._

Ett promise representerar ett eventuellt resultat av en asynkron operation och kan antingen vara i tillståndet "fullfilled" med ett resultat, eller "rejected" med ett fel.

Promises används för att undvika callback-hell och skapa mer läsbar och hanterbar asynkron kod. Istället för att använda callback funktioner använder man promises och länkar samman operationer med metoder som t.ex. ".then()" och ".catch()".

Man använder metoden ".catch()" för att fånga upp och hantera eventuella fel som kan uppstå under utförandet av de asynkrona funktionerna. Det vill säga när den asynkrona operationen tilldelats statusen "rejected" och retrunerat ett fel. Metoden .catch() tar emot en callback-funktion som kommer köras när promise-objektet blir avvisat. Callback-funktionen får felet som ett argument och kan sedan hantera eller logga felet på ett lämpligt sätt.

Man använder ".then()" metoden för att hantera ett promise som har statusen "fullfilled", det vill säga när den asynkrona funktionen har slutförts och returnerat ett resultat. Metoden .then() tar emot en callback-funktion som kommer att köras när promise-objektet är uppfyllt. Resultatet av promise-objektet skickas in i callback-funktionen som ett argument och kan sedan hantera resultatet och använda det i koden.

![Kod exempel](./Pictures-JavaScript/exempleCatchThen.jpg)

Med promises kan man utföra asynkrona operationer och sedan behandla resultatet (eller felet) när det blir tillgängligt vilket möjliggör mer elegant kodhantering.

_Källa: Föreläsning den 3 november 2022 av Sebastian Lindgren_

Källa: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise

## JS 1.4 OOP i JavaScript
Beskriv rubriken här

## JS 1.5 DOM-manipulation
Beskriv rubriken här

## JS 1.6 HTTP-requests
Beskriv rubriken här

## JS 1.7 Lexical scope
Beskriv rubriken här

## JS 1.8 Event handling
Beskriv rubriken här

## JS 1.9 Prototype inheritance
Beskriv rubriken här

## JS 1.10 Higher-order functions
Beskriv rubriken här

## JS 1.11 Single-thread programming
Beskriv rubriken här

## JS 1.12 OAuth från frontend
Beskriv rubriken här

## JS 1.13 Websockets
Beskriv rubriken här

