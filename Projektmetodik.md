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
Det finns ett antal icke-agila metoder. Jag har valt att beskriva vattenfallmetoden för att reda ut vad en icke-agil metod är.

**Waterfall metoden**
Waterfall metoden eller vattenfallmetoden som det kallas på svenska är en icke-agil projektledningsmetod som betonar en linjär progression från början till slutet av ett projekt. Denna metokdik, som ofta används av ingenjörer, förlitar sig på noggrann planering, detaljerad dokumentation och steg som utförs i en följd.

Vattenfallmetoden använder en logisk progression av steg, på samma sätt som vatten rinner över kanten på en klippa, och går ut på att sätta distinkta mål för varje utvecklingsfas. Dessa mål kan inte göras om efter dessa har upnåtts.

Dr. Winston W. Royce vid Lockheed Software Technology Center introducerade konceptet i en artikel publicerad 1970 om hans erfarenhet av att utveckla programvara för satelliter. Royce använde dock inte termen vattenfall, utan hänvisade istället till nedströmsvärdet av dokumentation.

Vattenfallsmetoden forsätter att användas i industriella designapplikationer. Det nämns ofta som den första metodiken för mjukvaruutveckling. Metoden används också mer generellt som en projektledningsmetodik på hög nivå för komplicerade och mångfacetterade projekt.

**Fördelar med vattenfallmetoden**
* Möjliggör för ett stort team att arbeta mot samma mål som har definierats i kravstadiet
* Tvingar fram struktur och diciplin inom organisationen
* Enkelt att förstå, ordna och följa uppgifter
* Underlättar avdelningsfördelning och ledningskontroll baserat på schemat eller deadlines
* Definierar kodstandard innan design och kod implementeras
* Möjliggör tidig design av systemet och underlättar specifikationsändringar
* Tydliga milstolpar och deadlines

**Nackdelar med vatenfallmetoden**
* Designen är inte anpassningsbar
* När ett fel upptäcks måste hela processen börja om
* Metoden innehåller inte feedback från användare eller klienter under processens gång
* Metoden fördröjer testning till slutet av processen
* Metoden tar inte hänsyn till felkorrigering
* Metoden har mycket begränsade möjligheter att hantera förfrågningar om ändringar, omfattningsjusteringar eller uppdateringar
* Vattenfallmetoden låter inte processer överlappa varandra för samtidigt arbete i olika faser, vilket leder till lägre effektivitet
* Ingen fungerande produkt är tillgänglig förrän de senare stadierna av projektets livscykel
* Vattenfallmetoden är inte idealisk för komplexa pågående projekt med hög risk

__Källa: https://www.techtarget.com/searchsoftwarequality/definition/waterfall-model__

## PJ 1.3 Entreprenörskap inom webbutveckling
Om man vill bli en entreprenör och starta ett företag inom webbutveckling finns det en mängd saker att överväga innan man kör igång. Utöver gedigna kunskaper om webbutvecklingsteknologier bör man även ha stark förståelse för branchen samt kunna identifiera en potentiells kunds specifika behov samt ha förmåga att bygga långsiktiga affärsrelationer. Att ha god branchförståelse möjliggör god planering. En välgjord affärsplan kan hjälpa till med tydligt definierade mål och framtagandet av strategier för tillväxt, vilket är en grundläggande förutsättning för att lyckas.

Med det sagt är det bra om man bl.a. skapa sig en uppfattning om vilka kostnader som kan uppstå och därmed förstå hur prissättningsstrukturen bör se ut.

**Företagskostnader**
* Före öppnandet av företaget
    * Affärsplan och kostnader för efterforskning (marknadsanalys med mera)
    * Lånekostnader
    * Startkostnade
    * Teknologiska / materialkostnader
* Företagets dagliga kostnader
    * Marknadsföring
    * Lönekostnader
    * Försäkrings- och licenskostnader
    * Ytterligare material / tegonoliska kostnader

Man bör även ha en bra idé om vad man vill göra och profilera företaget utifrån detta. Detta är viktigt för att kunna skapa ett "helhets koncept" eller en "signatur" vilket skapar en känsla av baknatskap hos potentiella kunder. Som webbutvecklare kan man ta en multitud av olika uppdrag och detta behöver inte vara begränsat till att utveckla webbsidor.

Det är även bra att överväga vilka kostnader som finns i ett projekt för att kunna avgöra en budget.

**Projektkostnader**
* Vilken stack används i projektet
* Komplexiteten i projektets olika delar
* Hur mycket UX/UI och annat förarbete som behöver göras

Dessa är de initiala avgörande faktorerna för projektets kostnad.

**Intäktsmodeller**
Några förslag på hur ett företag kan tjäna pengar inom webbutveckling:

* Serviceavtal / maintenance - Månadsavgift / bindningstid
* Licenskostnader
* Projektpris

**Prissättning**
Förslag på prissättning:

* Vad är kunden berädd att betala?
* Hur stort är behovet?
* Vad kostar konkurrentens lösningar?

**Kundrelationer**
Det är viktigt att upprätta bra relationer till kunder och som entreprenör är det givande att jobba utifrån kundfokuserade metoder. Att lyssna på kundens behov och ge utmärkt kundservice kan bidra till att bygga långsiktiga affärsrelationer.

**Team och partnerskap**
Att ha rätt team eller partners kan vara avgörande för hur framgångsrikt ett företag blir. Hitta likasinnade personer som du har förtroende för.

**Marknadsföringsstrategier**
Detta kan handla om digital marknadsföring, sociala medier, nätverksevenemang och kampanjer med mera.

**Utbildning och uppdatering av färdigheter**
Som entreprenör inom webbutveckling är det viktigt att hålla sig uppdaterad med de senaste teknologierna och trender. Detta bör göras genom kontinuerlig utbildning och självstudier. Att ha bra koll på läget bidrar till att företaget behåller sin konkurrenskraft.

**Portfolio**
Skapa en portfolio där företaget kan visa upp sina tidigare arbeten och projekt. På så vis kan företaget visa upp vad som kan erbjudas / förväntas på ett tilltalande sätt.

**Bokföring**
Sist men inte minst _Hitta en bra revisor!_

_Källa: Föreläsning den 24 maj 2023 med Sebastian Lindgren_

## PJ 1.4 Issue handling
Inom projektmetodik och webbutveckling syftar "issue handling" till processen att identifiera, hantera och lösa problem / utmaningar som kan uppstå under projektets gång. Ett "issue" kan vara en uppgift som ska lösas under utvecklingsprocessen eller en situation / problem som påverkar projektets framsteg eller resultat negativt.

Issue handling brukar involvera följande steg:

* Identifiering och dokumentation av uppgiften / problemtet (t.ex. tekniska svårigheter / buggar / missförstånd mellan leverantör och kund)
* Värdera och prioritera, det är viktigt att skapa en uppfattning om vad som behöver lösas först
* Analysera problemet och skaffa förståelse för orsakerna till problemet (t.ex. utvärdera påverkan av ändrade krav)
* Ta fram adekvata lösningar till problemet och kommunicera detta till kunden
* Utveckla lösningarna och implementera dessa i projektet samt utför tester
* Övervaka hur lösningen fungerat och ta in feedback från t.ex. användare / kund (gör uppföljningar)

Genom att hantera uppgifter, problem och utmaningar på ett strukturerat sätt genom issue handling-processen kan teamet minimera störningar och se till att projektet håller sig på spåret. Detta bidrar även till ökat förtroende från kunder vilket också ger en högre "kundnöjdhet".

Ett bra sätt att organisera issue handling är att använda en Kanban board. En Kanban board består vanligtvis av kolumner som representerar olika stadier i arbetsflödet som t.ex. "backlog / att göra", "pågående", "klart".

Fördelar med att använda en Kanban board:

* Visualisering - Det är enkelt att se vart i arbetsflödet en issue befinner sig
* Prioritet - Det är lätt att se vilken prioritet ett issue har
* Samarbete - Det är enkelt för teamet att se vem som gör vad samt vilken status ett pågående issue har
* Kontinuerlig förbättring - Teamet kan identifiera flaskhalsar och förseningar i issue handling-processen och därefter vidta åtgärder för att optimera arbetsflödet
* Transparens - En Kanban board ger tydlighet och transparens i projektets framsteg för alla inblandade

Med det sagt är en Kanban board ett mycket bra verktyg för att hantera issue handling.**

**Github issues & issue handling**
Github issues är ett verktyg som tillhandahålls av Github och är anpassat för utvecklare. Tanken är att Github issues ska hjälpa utvecklarna att bryta ner stora problem i mindre uppgifter (issues) som kan fördelas över teamet. Verktyget hjälper även till med god översikt av projektet som helhet, status för olika issues, vem som gör vad samt med versionshantering, commits, pull requests och "merging" av features.

Processen för issue handling med Github issues kan sammanfattas på följande sätt:

1. Skapa en issue - Kan vara ett problem, en idé eller ett förbättringsförslag. Man kan även lägga till en beskrivning av en issue.
2. Tilldela - En issue kan tilldelas till specifika personer inom teamet som då ansvarar för denna issue. Man kan även tilldela en etikett som stöd för att organisera och katigorisera hanteringen av en issue, t.ex. bug, förbättring, idé etc.
3. Samarbete - Andra medlemmar i teamet kan kommentera en issue och på så vis delta i diskussionen kring denna.
4. Arbetsflöde - Github issues har inbyggd funktionalitet för att organisera arbetsflödet för issues. En issue kan tilldelas med en specifik status som öppen, pågående eller avslutad vilket hjälper till med att hålla koll på vad teamet behöver fokusera på.
5. Referenser - Om en issue är relaterad till en annan issue kan man lägga till en referens så att det framgår att dessa issues hör ihop.
6. Avsluta - När en issue är löst eller när diskussionen om en issue nått en slutsats kan man stänga denna. Issuen får då statusen avklarad vilket indikerar att den inte behöver mer uppmärksamhet.

_Källa: https://www.lucidchart.com/blog/what-is-issue-management_
_Källa: https://www.planview.com/se/resources/guide/introduction-to-kanban/_
_Källa: https://github.com/features/issues_
_Källa: https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart_