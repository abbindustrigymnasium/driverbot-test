# Driverbot template
I det här repot hittar ni exempel kod att utgå från samt instruktioner när ni kodar i ert projekt.

## GitHub
Acceptera uppgiften på [https://classroom.github.com/a/cqxgjh7K](https://classroom.github.com/a/cqxgjh7K).

## Mikrokontroller
### Koppla och testa!
Bilden nedan visar hur du ska koppla motorn till din esp.
![image](https://github.com/abbindustrigymnasium/driverbot-template/assets/22837762/703aad4b-4015-4c4a-9739-1644a61969b3)

### Koda
När du löser uppgifterna nedan utgår du från koden i [motorTest.ino](motorTest.ino). Börja med att planera dina lösningar mha psuedokod och/eller diagram innan du skriver den faktiska koden.

1. Läs och tolka koden - vad tror du att den gör? Kommentera i filen. Testa att köra koden för att kontrollera dina antaganden.
2. Koden fungerar inte helt som vi tänkt oss, vi vill att den ska byta körriktning efter 2200 millisekunder och efter 2200 byter igen. I nuläget kör den bara åt ett hål, lös det! Utgå från det du lärde dig om koden i steg 1 och experimentera vid behov vidare genom att ändra olika värden för att se vad varje del gör.
3. Gör om kodstrukturen genom att skapa en funktion/metod ```Drivetest(input1, input2)``` som utför koden från steg 2. Ett anrop av funktionen kan se ut som nedan.
```
Drivetest(motorPinRightDir, motorPinRightSpeed);
```
4. Nu ska vi utöka funktionaliteten i ```Drivetest()```. Kopiera funktionen och döp den nya varianten till ```Drivetest2()```. Nu vill vi se hur snabbt och långsamt motorn kan köra. Skapa en loopande funktion där motorns hastighet succesivt ökar.
5. Vi fortsätter bygga ut funktionaliteten! Utgå från ```Drivetest2()``` och skapa en ny funktion som vi kan kalla ```Drivetest3()```. Den nya funktionen ska kunna göra samma sak som tvåan men alterera mellan vänster och höger varv. Först från långsamt til snabbt på högervarv sedan samma åt vänster sedan höger igen o.s.v...
6. Vi fortsätter bygga på funktionen! I denna version ska du mellan varje varv låta motorn vila några sekunder, du vill även att den i loggen räknar upp hur många varv den har kört.

## MQTT
Jobba utifrån [denna Sway](https://sway.cloud.microsoft/4wekNvX2nqSH0zCX?ref=email&loc=play). 

## VUE
Exempelkod i VUE för att skapa en hemsida som driverboten kan styras via finns [här](https://github.com/abbindustrigymnasium/Driverbot/tree/master/Hemsida).
1. Utgå från koden ovan och testa att styra din bil. OBS! Ni behöver konfigurera koden i ```Driverbot.ino``` så att den pekar mot er broker.
2. För högre betyg än godkänt: modifiera den befintliga koden för att på något sätt förbättra resultatet eller bygg en egen hemsida.

Tips på fördjupningar för högre betyg (mer avancerade problem):
- Skapa en karta över driverbotens rörelse för att illustrera hur den har kört
- Byt ut den typ av input som ges via hemsidan till t.ex. en form som driverboten ska följa eller en punkt den ska köra till

