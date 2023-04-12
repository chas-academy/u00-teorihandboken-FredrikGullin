# Teorihandboken - Projektmetodik (PJ)
Studerande: Fredrik Gullin

## PJ 1.1 Agila metoder (Scrum, Kanban, Extreme Programming)
Agila metoder är ett sätt att arbeta i projekt där arbetet utförs i korta etapper som kallas sprintar. En sprint kan beskrivas som en beställning av något som ska utföras. Därefter planerar man för arbetet, genomför det och avslutar sprinten.

Detta är dock en väldigt förenklad förklaring och det finns flera olika agila arbetssätt man kan implementera i sitt projekt med olika tillvägagångssätt och "ceremonier" för att säkerställa att man faktiskt jobbar agilt.

Agila metoder hjälper både beställare och leverantör att få fram en bättre slutprodukt. Under projektets gång får man en tydlig bild över hur mycket av backlogen som kommer kunna realiseras. Man kan uppleva att mycket tid går åt till möten men plannering är viktigt och möten är tidbegränsade (time-boxade). På så sätt begränsar man tiden som läggs på planering. Med agila arbetsmetoder tar man kontinuerligt in återkoppling från användare vilket hjälper till med att prioritering av uppgifter. Detta kan leda till att vissa prioriterade uppgifter väljs bort till förmån för andra viktigare uppgifter. Önskemål som man hade vid projektets start kan visa sig vara onödiga när man tagit till sig användarnas återkoppling och kan därför prioriteras bort vilket både kan spara tid och pengar för beställaren.

**Scrum**
Scrum är en agil metod för systemutveckling som uppfanns under 1990-talet och är idag en etablerad metodik för systemutveckling som används i hela världen.

Fördelarna med scrum är att man fokuserar på affärsnytta samt möjligheten att förändra ett pågående projekt på ett strukturerat sätt. I scrum använder man en så kallad "backlog" istället för en klassisk kravspecifikation. En backlog kan beskrivas som en levande prio-lista med önskemål och uppgifter som ska utföras i projektet. Styrkan med scrum är att man kan fokusera på vad projektet behöver då prioritetsordningen kan ändras under projektets gång och åtaganden som hade hög prioritet i början av projektet kan prioriteras ned och lämna plats för nya uppgifter som efter en viss tid får högre prioritet då detta skapar mer värde (affärsnytta).

**Roller**
I scrum finns det tre uttalade roller:

* Produktägare (product owner): Produktägaren sammanställer och prioriterar önskemål om tillägg och ändringar, främst utifrån affärsnytta. I ett webbprojekt är det vanligt att produktägaren är en projektledare hos beställaren.

* Scrum master: Scrum mastern coachar teamet och ser till att allt rullar på smidigt. Scrum mastern stämmer av mellan aktörer samt ser till att det inte finns några hinder för teamet.

* Team: Teamet är självorganiserande och bestämmer gemensamt vem som gör vad och hur man löser olika uppgifter.

**Komponenter / ceremonier**
* Backlog: En prioriterad lista med alla önskemål om produkten. Produktägaren prioriterar och har ansvar över backlogen. Uppgifterna i en backlog skrivs ofta som "user stories".

* Sprint backlog: Den del av produktbacklogen som teamet åtar sig att implementera under en sprint.

* Daily scrum: Ett kort statusmöte för teamet. Scrum master går igenom alla personer i teamet som besvarar tre frågor:

    1. Vad har jag gjort sedan igår?
    2. Vad ska jag göra till imorgon?
    3. Finns det något som hindrar mig?

* Sprintgenomgång (sprint review): En genomgång av status på det arbete som ska genomföras i sprinten. Genomgången inkluderar även demonstration av funktionaliteten för produktägare, kunder och andra inbjudna intressenter. Syftet är att skapa en gemensam förståelse och vision för projektets status.

* Återblick (sprint retrospective): Teamet, scrum mastern och produktägaren går tillsammans igenom erfarenheter från den gångna sprinten och identifierar möjliga förbättringar i arbetssättet. Några punkter kan väljas ut och åtgärdas i kommande sprint.

* Sprintplanering (sprint planning): Produktägaren, scrum mastern och teamet går igenom de önskemål / uppgifter som finns. Därefter bryter teamet ned kraven och uppskattar hur mycket tid de olika önskemålen kan tänkas behöva. Genom att jämföra tidsestimerade och prioriterade önskemål med tillgänglig tid tas en sprint backlog fram som teamet åtar sig att genomföra.

**Kanban**
Kanban är en visuell metod för att hantera arbetsflödet på individ-, team-, och organisationsnivå. En kanban-tavla med fält för "att göra", "pågående" och "klart" är ett utmärkt sätt att börja visualisera arbetet.

**Extreme programming**
Extreme programming (XP) är baserat på fem värderingar: kommunikation, enkelhet, återkoppling, mod och respekt.

Metoden värderar kontinuerlig kommunikation med beställare / kund och därför är det viktigt att denna finns tillgänglig. Kunden har möjlighet att bestämma vad som ska uppfyllas av produkten som utvecklas och i vilken ordning dessa ska prioriteras.

XP har ett antal så kallade "tillämpningar" som stöttar de fem värderingarna:

* Planeringsspelet: funktionalitet i nästa leverans bestäms genom prioriterade verksamhetsberättelser och tekniska bedömningar.

* Små leveranser: produkten levereras i små inkrementella versioner.

* Metafor: en enkel beskrivning av hur produkten ska fungera.

* Enkel design: genom att hålla koden enkel blir även designen enkel. Ta bort komplexitet från koden kontinuerligt när den upptäcks.

* Testning: tester skrivs innan koden utvecklas. Programmerare skriver tester och validerar koden medan kunden skriver tester som testar och validerar verksamhetsberättelser.

* Omstrukturering av kod: ta kontinuerligt bort identiska (dubbletter) och komplexa kodbitar.

* Parprogrammering: programmerare arbetar i par vid en dator. En skriver koden medan den andre granskar koden.

* Gemensamt ägandeskap: alla har rätt att ändra i all kod, skriven av dem själva eller någon annan.

* Kontinuerlig integration: när en implementationsuppgift är utförd byggs systemet / produkten och integreras med den redan färdiga koden. Detta kan ske flera gånger per dag.

* 40-timmars arbetsvecka: programmerare tänker och därmed arbetar bättre utvilade. Övertid tillåts inte i två veckor i rad.

* Kund på plats: kunden arbetar med utvecklarna på heltid för att kunna svara på frågor, definiera produkten och skriva tester.

* Kodstandard: konsekvent kodstandard som alla programmerare följer.

__Källa: https://www.happiness.se/artiklar/vad-ar-scrum__
__Källa: https://www.planview.com/se/resources/guide/introduction-to-kanban/__
__Källa: https://projektforum.se/xp-extreme-programming/__

## PJ 1.2 Icke-agila metoder
Beskriv rubriken nedan här

## PJ 1.3 Entreprenörskap inom webbutveckling
Beskriv rubriken nedan här

## PJ 1.4 Issue handling
Beskriv rubriken nedan här
