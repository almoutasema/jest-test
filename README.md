1. Validate email
Skriv testfall till, och implementera, en funktion som validerar en e-postadress:
2. Validate ZIP
Skriv testfall till, och implementera, en funktion som validerar ett postnummer som kommer in
som en sträng:
3. Skapa Heading
Skriv testfall till, och implementera, en funktion som ska skapa HTML- rubriker. Exempel:
# Skapa jest.config.js
npx ts-jest config:init
"scripts": {
"test": "jest",
"test:watch": "jest --watchAll"
},
validateEmail(”jonatan@gmail.com”) -> true
validateEmail(”jonatan@gmail”) -> false
validateEmail(”jonatan.com”) -> false
validateZip(”12345”) -> true
validateZip(”1234”) -> false
validateZip(”123456”) -> false
validateZip(”abcde”) -> false
4. Formatera Pris
4a)
Skriv testfall till, och implementera, en funktion som avrundar tal. Du bygger ett plugin till en
webbshop som ska ta reda på priserna för olika produkter. Priserna kommer från databasen,
men eftersom det är en internationell webbshop och priserna kan omvandlas mellan olika
valutor, kan man få priser med många decimaler. Du vill att webbshoppen ska visa priset med
två decimaler och lägga på svensk valutasymbol efteråt. Priserna måste avrundas uppåt, så
inte affären förlorar pengar. Exempel:
4b)
Utöka roundPrice så att den tar emot vilken valuta den skriver ut (t.ex. NOK, USD istället för
bara SEK). Börja med att skriva testfall. Ändringen ska vara bakåtkompatibel så alla gamla
testfall ska fungera utan att de ändras
4c)
Man brukar skriva ut olika valutor på olika sätt, t.ex:
USD brukar stå före beloppet (USD 10)
kr brukar stå efter (10kr)
Skriv tester och uppdatera funktionen så att den tar emot ett pattern som beskriver hur beloppet
ska returneras. Exempel:
 makeHeading("Hello", 1) → "<h1>Hello</h1>"
 makeHeading("Next level", 2) → "<h2>Next level</h2>"
roundPrice(232.10542) → "232.11 SEK"
roundPrice(14) → "14.00 SEK"
roundPrice(1024.2048) → "1024.20 SEK"
roundPrice(232.10542, '%PRICE% kr') → "232.11 kr"
roundPrice(14, '$%PRICE%') → "$14.00"
roundPrice(1024.2048, 'USD %PRICE%') → "USD 1024.20 SEK"
5. Kolla om lowercase
Skriv funktionen isLowerCase(input: string) som returnerar true om input endast innehåller
lowercase-bokstäver och false annars. Skriv tester först!
6. Primtal
Skriv tester först och en funktion som testar om ett tal är ett primtal.
8. Genitiv
Skriv tester först och en funktion som tar emot ett namn och returnerar genitivformen av
namnet. Exempel:
9. Async
9 a )
Skriv ett test och skapa funktionen getUsers som i en promise returnerar:
getGenitive("Jonatan") => Jonatans
getGenitive("Anna") => Annas
getGenitive("Claes") => Claes
getGenitive("Hampus") => Hampus
getGenitive("Johanna") => Johannas
[
 {
 "name": "Erik",
 "group": 1
 },
 {
 "name": "Lisa",
 "group": 2
 },
 {
 "name": "Hampus",
9b )
Skriv ett test och skapa funktionen getGroups som i en promise returnerar:
 "group": 2
 },
 {
 "name": "Linda",
 "group": 3
 },
 {
 "name": "Eva",
 "group": 1
 },
 {
 "name": "Anna",
 "group": 3
 }
]
 [
 {
 "id": 1,
 "groupName": "Hajarna"
 },
 {
 "id": 2,
 "groupName": "Valarna"
 },
 {
 "id": 3,
 "groupName": "Zebrorna"
 }
 ]
