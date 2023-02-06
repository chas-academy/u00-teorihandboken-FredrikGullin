# Teorihandboken - Backendutveckling (BE)
Studerande: Fredrik GUllin

## BE 1.1 PHP
Beskriv rubriken här

## BE 1.2 OOP i PHP
Beskriv rubriken här

## BE 1.3 Säkerhet i PHP

**Vad är säkerhet?**
Det man brukar prata om är applikationssäkrehet va IT-säkerhet.

* Applikationssäkerhet: Hur vi säkrar information och skyddar delar i vår applikation från attacker. Med andra ord applikationens egen säkerhet.
* IT-säkerhet: Hur vi skyddar, konfigurerar och ser till att våra system (fysiska och digitala) är säkra.

**IT-säkerhet**
Inom IT-säkerhet talar man oftas om sårbarheter (vulnerabilities). Man syftar då på svagheter eller brister med implementationen eller lösningarna i antingen system eller fysisk hårdvara. Dessa svagheter kan utnyttjas för att få tillgång till systemet där man också kan ställa till oreda eller skada.

**Hacking**
Hacking kan beskrivas som när man försöker ta sig in och få tillgång till ett system. Med andra ord är hacking de handlingar / aktiviteter man utför för att få tillgång till och kompromettera digitala enheter och nätverk. _Hacking är även ett gammalt svenskt uttryck för allmän datavetenskap / programmering (brukas oftast de som lärde sig programmering för ca 20 år sedan)._

**Det finns olika tillvägagångssätt för hacking:**

* Botnät - Förkorttning av botnätverk, kan beskrivas som ett nätverk av kapade datorer som genom "malware" kontrolleras av en hacker. Botnätet kan användas för spamming eller DDos attacker.

* Webbläsarkapning - Innebär att användaren blivit inlurad på en sida som styrs av en hacker men som ser ut som en vanligsida. I allvarliga fall kan detta leda till stöld av inloggningsuppgifter och känslig information.

* Denial of service (DDos) attacker - Innebär att en väldigt stor mängd samtidigt "pingar" / skickar olika kommandon till en server så att den blir överbelastad och får en virtuell explosion. Detta leder långa svarstider och "downtime" (out of service) som även kan öppna svagheter som kan utnyttjas för att ta sig in.

* Ransomeware - Låser ner datorn tills dess att ägaren av datorn betalar en summa pengar till hackern för att låsa upp systemet igen.

* Rootkits - Är mjukvara som används av hackers för att ta kontroll över någon annans dator.

* Trojaner - Är ett program som laddats ner och installerats på datorn som verkar ofarligt men som egentligen innehåller någon typ av skadlig kod. Kan användas för diverse olika syften.

* Virus - Skadligkod som tagit sig in i datorns system som tillexempel trojaner eller ransomware.

* Maskar - En mask är ett slags virus som kopierar- och sprider sig själv vidare till andra datorer genom till exempel e-post.

**Varför vill man hacka?**

Pengar är en bra anledning och ett starkt motiv för att hacka andra människor. Vissa kan göra detta för att "busa" och "jävlas" med andra. Det finns även olika hacker communities som till exempel Anonymous som har sina egna agendor och strukturer. Det kan även användas för olika typer av spionage och används både av olika statliga säkerhetstjänster och privata aktörer för att få fördelar i en värld där information är en allt mer eftertraktad valuta.

Det finns även "goda hackers" som till exempel "hacktivister", "white hats" eller "ethical hackers" som hackar med intentionen att uppmärksamma olika företags säkerhetsbrister. Dessa hackers hackar med goda intentioner, med gott syfte. "Ethical hacking - open the gate just alittle".

**Applikationssäkerhet**

I applikationskitet behöver utvecklare ha koll på sårbarheter i applikationen som utvecklas. Genom att hantera dessa sårbarheter minskar man risken för att applikationen går att hacka. _Man kan läsa mer om de 10 vanligaste sårbarheterna genom att titta på OWASP (open web application security project)._

Några av dem som brukar vara högt upp på listan är:

* Injecering - en brist där opålitliga kommandon kan skickas med i t.ex. SQL-queries (SQL-injektioner) och utföra skadliga operationer.
* Bruten autensering - när en applikations autenseringsflöde är brutet kan användaruppgifter och annan känslig information komprometteras.
* Exponering av känslig data - När APIer inte skyddar känslig data på ett korrekt sätt. Detta kan kompromettera personliga användaruppgifter.

Om säkerheten brister inom dessa områden kan hackare komma åt känslig användarinformation som t.ex. namn, efternamn, adress, lösenord och kreditkortsuppgifter.

* XXE (XML-Exteral Enteties) - När äldre versioner av XML-tolknngsmjukvara oavkortat läser externa referenser. Dessa externa referenser kan användas för att lista interna filer på disk, öppna portar och för att köra egen kod på servern.

* Bruten auktorisering (användarkontroll) - När en applikations auktorisering är bruten kan olika typer av användare få rättigheter till andra användares information, eller t.ex. administrativa funktioner. Det säkraste sättet att "logga" in är genom tredjeparts autensering t.ex. med bankID.

* Felaktig säkerhetskonfiguration - Den vanligaste förekommande bristen. Uppstår när en konfiguration för t.ex. system, ramverk, eller bibliotek saknar korrekt konfiguration för att kunna användas säkret i produktionsmiljö. _Detta är extremt lätt att misslyckas med om man inte kontinuerligt jobbar med detta._

* Cross-Site Scripting (XSS) - Är en brist som uppstår när en applikation inkluderar opålitlig data in i en ny sida utan validering. En XSS attack låter en hackare köra skript i användares webbläsare och kan då få tag i användarsessioner, vanställa webbplatser eller dirigera om användare till skadliga webbplatser.

* Osäker deserialisering - Om deserialisering görs på ett osäkert sätt kan sårbarheten utnyttjas. Denna brist möjliggör flera olika typer av attacker.

* Användning av komponenter med kända säkerhetsbrister - När bibliotek, ramverk etc, som har kända säkerhetsbrister utnyttjas. Kan resultera i förlorad data eller till och med övertagande av en server.

* Otillräcklig loggning och övervakning - När loggar och övervakning är bristande eller saknas kan attacker fortsätta obemärkt och på sikt lyckas manipulera, få ut eller ta bort data. De flesta studier visar att det tar över 200 dagar för att upptäcka ett intrång. Vilket ofta upptäcks av en extern part, snarare än internt.

En ytterligare faktor för säkerhet man bör ha i åtanke är att inte spara användares lösenord i klartext i ens databas. Man bör använda någon form av kryptering. Det finns olika algoritmer för att kryptera ett lösenord eller "hash a password". Några exempel på hash-algoritmer är SHA-1, SHA-2 (SHA-256, SHA512), Whirlpool, Tiger, AES, Blowfish och MD5 (som länge var det vanligaste sättet). Man bör således använda en funktion för att "hasha" eller "salta" lösenordet när man sparar det och således även använda en funktion för att "dehasha" lösenordet när användaren t.ex. loggar in. I PHP finns funktionerna password_hash() och password_verify() för detta ändamål.

En framgångsrik inställning är att se användardata som potentiellt skadlig och på olika sätt skydda sig mot detta. I förlängningen innebär även detta att även sparad data från databasen potentiellt kan vara skadlig då denna kommer från användare. Man bör därför överväga detta tankesätt när man utvecklar en applikation för att göra denna så säker som möjligt.

Ett sätt att skydda sig mot skadlig användarinput (även kallat injektioner) kan vara att använda sig av funktionerna htmlspecialchars() och strip_tags() i PHP. Dessa funktioner saniterar inputen då den inte tillåter html specifika symboler (t.ex. & " ' < >), vilket förhindrar användare från att skicka in direkt skadliga skript i databasen.

_Källa: Föreläsning "Säkerhet i PHP" av Sebastian Lindgren den 16 januari 2023_

## BE 1.4 MVC
Beskriv rubriken här

## BE 1.5 Wordpress
Beskriv rubriken här

## BE 1.6 Heirarkiska databaser
Beskriv rubriken här

## BE 1.7 Relationsdatabaser, SQL och ER-modellering
Beskriv rubriken här

## BE 1.8 OAuth i backend
Beskriv rubriken här

## BE 1.9 HTTP-protokollet
Beskriv rubriken här

## BE 1.10 cURL
cURL är ett terminalverktyg som möjliggör utbyte av data mellan en enhet och en server genom en terminal. 

Genom att använda detta CLI (command line interface) så kan en användare ange en specifik server URL (adressen dit de vill skicka en request) och den data de vill skicka till serverns URL.

Till skillnad från andra liknande verktyg för detta ändamål så använder cURL endast terminalen och saknar ett GUI. cURL fungerar på Linux, Mac och Windows.

cURL använder "libcURL client-side URL transfer library" som stödjer många olika "transfer protocols" så som HTTPS, SMTP och FTP. Det erbjuder även en möjlighet att inkludera "cookies", sätta upp proxys och lägga till en auktoriserings metod för olika requests.

cURL kan användas för att testa en API, ladda ner data från olika källor, testa webbsidor och följande "redirects" genom terminalen.

cURL kan kombineras med olika kommandon för att utföra olika uppgifter så som GET, POST, PUT, PATCH och DELETE. För att visa hur detta går till kommer jag ge några exempel på hur ett curl-kommando är uppbyggt.

**GET**
curl -X GET http://localhost:3000/posts

Detta kommandå hämtar all data från databasen på angiven URL. I detta fall databasen på localhost, port 3000, posts.

Denna data kommer därefter skrivas ut i terminalen där vi kan ta del av informationen som finns i posts.

**POST**
curl -X POST -d 'title=hello' -d 'author=Freddo' http://localhost:3000/posts

Detta kommando kommer skapa en ny post i posts med title "hello" och author "Freddo" i databasen på localhost, port 3000, posts.

**PUT**
curl -X -d 'title=hello' -d 'author=Freddo' http://localhost:3000/posts/1

Detta kommando kommer ändra den befintliga posten med id 1 (om vi utgår ifrån att det ursprungligen fanns en post med id 1) till title "hello" och author "Freddo".

Observera att PUT ändrar de parametrar man anger men raderar / skriver över övrig data som eventuellt finns i denna post.

**PATCH**
curl -X PATCH -d 'title=newHello' http://localhost:3000/posts/1

Detta kommando kommer endast ändra title på posten med id 1 (ovanstående post) till "newHello" men övrig data lämnas oförändrad.

**DELETE**
curl -X DELETE http://localhost:3000/posts/1

Detta kommande kommer radera post med id 1 från databasen.

_cURL som egentligen uttalas curl är ett mycket enkelt, snabbt och bekvämt sätt att hantera och testa t.ex. ett API och kommer bli en mycket älskvärd kompanjon senare i arbetslivet._

_Källa: Föreläsning "Dataformat curl och PHP inlogg" av Sebastian Lindgren den 19 januari 2023_

## BE 1.11 REST
Beskriv rubriken här

## BE 1.12 XML och andra dataformat
Beskriv rubriken här

## BE 1.13 Webbservrar
Beskriv rubriken här
