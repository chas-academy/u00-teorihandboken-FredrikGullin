# Teorihandboken - Programmeringsmetodik (PG)
Studerande: Fredrik Gullin

## PG 1.1 Versionshantering (Git)
För att förstå vad *versionshantering* och *Git* är måste vi först förstå vad ett versionshanteringssystem är.

Ett versionshanteringssystem (*VCS / ”version control system”*) är ett system som effektivt håller reda på ändringar i en eller flera filer över tid så att du kan återskapa specifika versioner vid en senare tidpunkt.

Ett *VCS* tillåter dig att återskapa valda filer eller hela projekt till ett tidigare tillstånd, jämföra ändringar över tid, samt spåra vem som gjort någon förändring och när förändringen gjordes. Om förändringen orsakat ett problem kan detta snabbt hittas och åtgärdas med hjälp av systemet. Ett *VCS* är också ett bra sätt att försäkra sig om att data inte går förlorad då man generellt kan återställa allt på ett enkelt sätt.

Det finns olika typer av versionshanteringssystem. I kommande avsnitt ska vi ta en närmare titt på några av dessa och deras för- och nackdelar.

**Lokala Versionshanteringssystem**
Precis som namnet avslöjar är ett lokalt versionshanteringssystem ett system som lagrar informationen om versioner och förändringar över tid i en lokal databas på användarens dator. En fördel är att systemet givetvis kan användas för att jämföra skillnader mellan versioner (*patchar*) men nackdelen med detta system är att det är felkänsligt. Om hårddisken i användarens dator skulle gå sönder så går hela projektets data förlorad. Om det är flera personer som jobbar i samma projekt men lokalt på sina egna datorer är det även svårt att hålla reda på vem som gör vad och mer komplicerat att få de olika delarna att fungera som en helhet.

**Centraliserade Versionshanteringssystem**
Centrala versionshanteringssystem (*CVCS*) utvecklades för att underlätta samarbeten där flera personer är med och utvecklar samma projekt. Det centrerade systemet har en enda server som innehåller alla versionshanterade filer och ett antal användare (*klienter*) som ”checkar ut” filer från den centrala servern. Under många år var detta det vanligaste sättet att versionshantera.

Ett *CVCS* har flera fördelar över lokala VCS då det till exempel gör det möjligt för deltagarna i ett projekt att bli medvetna om vad alla gör i projektet. Administratörer kan ha detaljerad kontroll över vem som kan göra vad sant att det är betydligt enklare att administrera ett centralt system än att hantera lokala databaser på varje enskild användares dator.

Nackdelen med detta system är användarnas beroende av att servern fungerar. Om servern slutar fungera och ligger nere i 1 timme så innebär detta att ingen kan arbeta med projektet under 1 timme. Om serverns hårddisk av någon anledning skulle gå sönder och datan inte går att återställa så går hela projektets historik förlorad (bortsett från datan som finns sparad lokalt på användarnas datorer). När man sparar all data på ett enda ställe riskerar man att förlora allt.

**Distribuerade Versionshanteringssystem**
Ett distribuerat versionshanteringssystem (*DVCS*) är ett system där användarna inte checkar ut den senaste versionen av filerna, utan speglar istället hela databasen (inklusive historik) som sparas lokalt på användarnas datorer. Fördelen med detta är att om en server skulle sluta fungera och datan förloras så kan vem som helst av användarna ladda upp sin spegelbild av projektet för att återställa den. Varje spegelbild (*klon*) är i själva verket en fullständig säkerhetskopia av all data.

Med ett *DVCS* kan användarna, genom att ha flera fjärrförvar, samarbeta med flera personer på olika sätt inom samma projekt, och gör det möjligt att ha flera olika arbetsflöden, vilket inte är möjligt med CVCS.

## PG 1.2 Benchmarking
Beskriv rubriken här

## PG 1.3 Testdriven utveckling
Beskriv rubriken här

## PG 1.4 Deploy och staging
Beskriv rubriken här

## PG 1.5 Debugging
Beskriv rubriken här

## PG 1.6 Dokumentation
Beskriv rubriken här

## PG 1.7 Struktur av kod i projekt
Beskriv rubriken här

## PG 1.8 Automatisering av arbetsflöde
Beskriv rubriken här

## PG 1.9 Virtualisering av utvecklingsmiljö
Beskriv rubriken här

## PG 1.10 Bundeling-verktyg
Beskriv rubriken här

## PG 1.11 Terminalinterface
Beskriv rubriken här

