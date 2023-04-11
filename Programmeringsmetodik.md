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

**Git**
Git är ett DVCS som kom till världen 2005 och uppfyller sina ursprungliga mål om att vara lättanvänt, förbluffande snabbt, väldigt effektivt med stora projekt och ett otroligt bra system för icke-linjär utveckling.

**Snapshots**
Konceptuellt sparar andra versionshanteringssystem information som en lista av filändringar, det vill säga en uppsättning filer och ändringarna som gjorts i varje fil över tid (även kallat deltabaserad versionshantering).

Git skiljer sig från övriga versionshanteringssystem och lagrar sin data som en serie ögonblicksbilder (snapshots) av ett miniatyrfilsystem. Varje gång du sparar en version eller sparar tillståndet i ditt projekt i Git så tas en bild över hur alla dina filer ser ut för ögonblicket och en referens till varje ögonblicksbild sparas. För att effektivisera sparas inte en fil på nytt ifall den inte har ändrats, utan endast en länk till föregående identiska fil som redan lagrats. Man kan tänka på data som Git hanterar som en ström av ögonblicksbilder.

De flesta operationerna i git görs lokalt och behöver endast lokala filer och resurser för att fungera (till skillnad från centraliserade versionshanteringssystem där de flesta operationer är beroende av nätverksuppkoppling för att fungera, vilket även leder till fördröjning). Då hela historiken av ett projekt sparas lokalt på användarens dator upplevs arbete i Git som mycket snabbt och effektivt. Då nästan all data sparas lokalt kan man i praktiken göra det mesta även utan internetuppkoppling.

**Integritet**
Allt i Git beräknas som en _checksumma_ innan det lagras och sedan refererar men till den checksumma. Detta innebär att det är omöjligt att ändra innehållet i någon fil eller katalog utan att Git känner till det. Denna funktion är inbyggd i Git på de lägsta nivåerna och är fundamentalt för dess filosofi. Du kan inte tappa information på vägen eller få en korrupt fil utan att Git kan detektera det.

Mekanismen som Git använder för att beräkna checksumman kallas för en SHA-1 hash. Det är en fyrtio lång teckensträng som består av hexadecimala tecken (0-9 och a -f) och beräknas baserat på innehållet i en fil eller katalogstruktur i Git.

När man utför en operation i Git resulterar detta alltid i att något läggs till i databasen. Det är svårt att få systemet att göra någon som inte kan ångras i efterhand eller att data på något sätt går förlorad. Så länge en ögonblicksbild har sparats kan man experimentera fritt utan rädsla att förstöra något.

Git kan användas oftast med en linux-terminal (eller med Git Bash för Windows) där man kan ange kommandon för att få Git att utföra det man önskar. Det är även möjligt att installera en extension i Visual Code som ger en del genvägar för att få Git att utföra vissa operationer.

För att se några exempel på grundläggande kommandon i git terminalen kan man besöka denna sida: [Atlassian - Git commands](https://www.atlassian.com/git/glossary).

__När man arbetar i grupp med större projekt kan det vara bra att ha en strategi för versionshantering. En populär strategi är att arbeta med "git flow". Detta går ut på att man skapar en branch som kallas main som är för produktion, en branch för utveckling som kallas develop och en branch för varje feature man arbetar med, en så kallad "feature branch". En feature kan t. ex. vara att skapa en funktion för något eller någon komponent i projektet. När denna är klar pushas denna upp till repot av utvecklaren som skapat branchen. Därefter görs ett "pull request" där utvecklaren ber någon av kollegorna att inspektera koden och om det finns några problem eller konflikter med övrig kod (en så kallad merge conflict) kan detta lösas innan featuren blir mergead in i develop branchen där projektet existerar i utvecklingsstadie. På detta sätt kan man se till att gruppmedlemmarna inte skriver över varandras kod när de mergar sina tillägg. När develop branchen är redo att mergas med main så uppdateras eller deployas själva applikationen i produktionsläge. Git flow är mycket effektivt och användbart.__

_Källa: https://git-scm.com/book/sv/v2/Kom-ig%C3%A5ng-Om-versionshantering_

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

