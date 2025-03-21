# Individuella reflektioner - Andrei Manea

Svara på var och en av frågorna nedan individuellt (minst 100 tecken per fråga)

## Frågor

### Inledning

#### Vad var ditt mål med projektet initialt?

Att lära mig att arbeta Agilt och att lära mig att jobba i team. Har också lärt mig mer JavaScript.

#### Vad var din känsla inför att arbeta i ett team när du gick in i uppgiften?

Jag var ganska orolig, kände mig väldig osäker över hur mycket JavaScript jag kan. Var också orolig over att jobba med andras kod. 

### Planering och genomförande

#### Hur tycker du att planeringen inför projektet fungerade?

Det gick jättebra! Vi hade sprint möte varje morgon kl. 9 och vi delade uppgifterna och också hjälpte varandra när vi behövde hjälp. Efter varje sprint review, besämde vi vem gör vad.

#### Vad har du bidragit med i planeringen, samt utvecklandet av applikationen.

Product Backlog, hjälpte till att skaffa drafts med vad vi behövde göra. Efter har jag gjort en del sidor (kvitto-receipt och location) och en del funktioner is JavaScript - logout, ETA tills maten blir klar, har också fixat massor av css så att alla sidorna har samma styling. Har fixat API till Google Maps i location.html, custom icons till foodtruck, osv.

#### Beskriv med dina egna ord, er applikation

En app till Yumm Yumm Give Me Some, en mat affär som säljer mat i Stockholm med hjälp av 3 olika foodtrucks. Kunden kan skaffa profil, beställa mat, se kvitto, se tidigare beställningar, och också se vad foodtruckarna finns med hjälp av Google maps. Vi har lika typ av användare, till exempel admin kan see alla ordrar.

### Teamets utmaningar och lösningar

#### Vika var de största utmaningarna för dig?

Java Script, Java Script, Java Script, Java Script, Java Script, Java Script, och ibland Java Script. Men mest JavaScript.


#### Hur löste eller hanterade du dessa utmaningar?

Har fått hjälp av mina kollegor, och sökte mycket på Google. Jag fösöker använda pseudokod när jag kan. Det känns som jag måste "go back to the basics", bygga enkla projekt och träna mer på arrays och hur man använder information från APIer.

#### Vilka kompromisser inom teamet har du fått göra under projektets gång?

Kan inte tänka om några kompromissar. Vi gjorde allt som vi hade i vår backlog och vi var klara med projektet i god tid. 

### Individuell reflektion och utvärdering



#### Vad lärde du dig under projektets gång?

Jag har lärt mig att arbeta agilt, och har lärt mig mycket JavaScript än jag kunde förrut. Har också slutat att använda massor av <div> taggar och använda BEM i CSS från början.

#### Finns det någonting du skulle velat göra annorlunda om du fick chansen igen?

Jag är osäker. Det känns som att jag har inte kodat så mycket i JS, så jag tror att jag skulle hade gjort mer av JS grejerna från product backlog. 

#### Vilka möjligheter ser du med de kunskaper du fått under arbetet med projektet?

Man kan koda appar, och de flesta appar är ganksa enkla (typ app-hemsida till restaurang, eller andra typ av företag). Kanska jag kan inte koda något på backend sidan, men kan säkert göra vanliga sidor till mindre företag. 

### VG-frågor (minst 200 tecken)


#### Beskriv minst tre fördelar med att arbeta agilt och motivera varför de är viktiga. Använd exempel från ert projekt för att styrka dina argument.

Agila metoder erbjuder flexibilitet, kontinuerlig kundfeedback och snabb leverans av MVP. För YYGS innebar detta att snabbt anpassa sig till kundernas behov, regelbundet förbättra appen baserat på feedback och lansera en grundläggande version för att lösa akuta problem. 

#### Beskriv en konkret lösning du föreslagit under projektet. Varför ansåg du att den var bäst? Jämför med minst en annan möjlig lösning och förklara varför du inte valde den.

När vi började designade vi varje sida i Figma för att ha en riktlinje för hur varje del av appen skulle se ut. När vi kom till location.html fick jag idén att använda Google Maps API och visa en realtidskarta över Stockholm med tre anpassade ikoner som representerar foodtruckarna. Den andra lösningen var att bara visa kartan som en enkel .jpg-bild utan någon form av interaktivitet. Jag bestämde mig för att implementera en riktig karta, eftersom detta kommer att hjälpa i framtida projekt. Jag lärde mig hur man använder JS för att ändra vilken del av kartan som först visas när användaren öppnar sidan (som standard visas Nordamerika), och hur man använder custom icons på kartan och koordinater.



#### Ge minst två exempel på lösningar ni valde bort. Analysera varför ni avstod från dem. Hur påverkade det projektet? Kunde något ha gjorts annorlunda?

Som jag nämnde ovan, bestämde vi oss för att inte använda en enkel bild för att representera kartan och valde istället den interaktiva kartan. En annan sak vi bestämde oss för att inte använda var ett gästanvändarsystem, och valde istället att förenkla inloggningsprocessen så att den tar så lite tid som möjligt. Jag är säker på att andra skulle kunna lösa samma problem på flera olika sätt.

#### Reflektera kring hur den kod du bidragit med skulle kunna förbättras, ge konkreta exempel.

Exemplet som kommer till mig är den sista funktionen jag implementerade som loggar ut användaren. Koden som jag skrev först - 

if (logoutNavItem) {
    logoutNavItem.addEventListener("click", () => {
        /* set current till userarray */
        let user = getUserInfo()
        if(user) {
            removeCurrentUser();
        }
      // Update UI, hide stuff :
      logoutNavItem.classList.add("d-none");
      document.getElementById("guestNav").classList.remove("d-none"); //hides the login button while the user is logged in
      document.getElementById("userNav").classList.add("dnone"); //shows the logout button while the user is logged in
      window.location.href = "index.html";
    });
}
Efter jag skrev det, vi fick massor av problem med login-logout knapparna. det visade sig att en av mina kollegor redan hade kod för att dölja/visa inloggningsknappen, så DOM-delen behövdes inte.

#### Om ni hade en vecka till på er, vad skulle du ändrat? Fokusera på arbetsprocessen, samarbetet eller verktygen ni använde. Hur skulle det ha påverkat resultatet?

Jag skulle inte ha ändrat mycket, vårt team var fantastiskt och vi arbetade mycket bra tillsammans, även om vi alla var ganska nya på detta system. Personligen tror jag att jag skulle ha gjort mitt eget liv mycket enklare om jag slutade använda `<div>`-taggar överallt, bara för att senare behöva ändra till semantisk HTML. Jag skulle ha börjat använda BEM för CSS från början istället för att vänta tills vi fick en massa konflikter vid git merge. Om vi hade haft en vecka till, skulle vi ha gjort fler buggfixar och kanske omskrivit hela inloggnings-/användarsystemet som tenderar att bli buggigt ibland på grund av hur vi använder localStorage och externa API:er.
