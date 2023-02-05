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

En ytterligare faktor för säkerhet man bör ha i åtanke är att inte spara användares lösenord i klartext i ens databas. Man bör använda någon form av kryptering. Det finns olika algoritmer för att kryptera ett lösenord eller "hash a password". Några exempel på hash-algoritmer är SHA-1, SHA-2 (SHA-256, SHA512), Whirlpool, Tiger, AES, Blowfish och MD5 (som länge var det vanligaste sättet). Man bör således använda en funktion för att "hasha" eller "salta" lösenordet när man sparar det och således även använda en funktion för att "dehasha" lösenordet när användaren t.ex. loggar in.

I PHP finns funktionerna password_hash() och password_verify() för detta ändamål.

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
Beskriv rubriken här

## BE 1.11 REST
Beskriv rubriken här

## BE 1.12 XML och andra dataformat
Beskriv rubriken här

## BE 1.13 Webbservrar
Beskriv rubriken här
