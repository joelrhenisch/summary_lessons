#Javascript
### Einleitung
- Flash sehr leistungsintensiv, daher wurde es vom Markt geärumt  
- www.javascript.info  

###Dev-Tools Chrome  
- Wenn Seite auf https ist, aber js nicht, funktioniert es nicht
- In Chrome mit Dev-Tools Objekt auswählen und in Console $0 schreiben und bestätigen. So sieht man die Eigenschaft des Objekts.
- Debugging  
chrome://devices  
- Unterschied console.dir und console.log  
console.dir -> auf z.B. div Element -> Element kann aufgeklappt werden und genau analysiert werden. (gibt es nur im Chrome )  
console.log -> auf z.B. div Element -> zeigt weniger Infos an wie bei console.dir
- Typ der Variablen sehen  
typeof VARNAME  
- Variablen definieren  
früher: var  
jetzt: let
- script-Tag in HTML  
Nachteil: muss überall im Code eingefügt werden (bei mehreren Seiten)  
Vorteil: lädt schon sofort 
- Pfade definieren
-> Pfad so anfangen -> //
so nimmt er https: von letzten Pfad
- "use strict" muss am Anfang des Dokuments mit doppelten Anführungszeichen geschrieben werden 
--> so erscheinen saubere Meldungen bei möglichen Fehler in der Console
- var i wird defniiert wenn ein Zähler definiert wird, z.b: eine Schleife
for(let i=0)


###Datentypen, Naming, Operatoren & PHP-Storm
- Whitespaces/Tabulator automatisch aufräumen  
alt-command-L
- Nachteil von Dash-Namensgebung -> json kann nicht implemiert werden, ausser man geht Umwege

######3 Datentypen von JS
number // var foo = 42;  
string // var foo = "bar" 
boolean // var foo = true 
null // bedeutet nichts bzw. null
undefined // nichts definiert  
object // {key: value}

######Operatoren
- a++  
wird erst nach der Ausgabe dazugerechnet
- ++a  
wird vor der Ausgabe dazugerechnet
- !    
negation = heisst nicht (Negation einer Aussage)

######neues JS
- alert( `hello ${1}` ); // ?
mit den Backtics können Variablen in einem String ausgegeben werden
www.babeljs.io  
JS Compiler alt zu neu und umgekehrt

###### JS Befehle  
- Konstante werden immer in Grossbuchstaben geschrieben  
- parse ind wandelt immer Ganzzahlenwert  
- parse float wandelt in Gleichkommazahl  
- Mit einem Fenster etwas nachfragen und darauf Antwort geben können via textinput Feld  
result = prompt("aa");  
- Ternary operator (muss nur bei hoher Performance so geschrieben werden, Klarheit geht vor)
let accessAllowed = (age > 18) ? true : false;
--> besser mit if/elseif/else schreiben  
- while schlaufe  
do while läuft mindestens 1x durch und macht Prüfung ob erledigt am Schluss  
while läuft nur durch wenn Prüfung am Anfang positiv erledigt 
- switch / if Unterschiede  
switch: wenn genaue Entsprechung getroffen wird, z.B. männlich/weiblich
if: wenn Alter abgefragt wird (x-beliebige Faktoren)
zusätzlich zu Switch: brake muss immer hinzugefügt werden, sonst rasselt er weiter und führt mehrere aus  
do while: läuft mind. 1x durch, prüft am schluss die ausgabe
  
- Objekte  
_method sind private Methoden (mit Underline vornedran sind es private Methoden)  
wenn gleichartige Elemente vorhanden sind (z.B. Einkaufsliste) dann soll ein Array verwendet werden     
chaining:
mit einem Punkt wird der Wert der vorherigen Funktion an die nächste übergeben
strinify und parse sind genau das Gegenteil
um einen Array durchlaufen zu lassen wie zum Beispiel durch eine Wurzel: hier wird map verwendet
    
    
    
Divide and Conquer  
- console.log innerhalb von EventListener einführen

script src nie in Head sondern in body. JS will sonst Objekte ausführen welche gar nicht da sind.
Seite kann weiss bleiben, wenn Ladezeit sehr hoch ist. Reihenfolge beachetn wenn mehrer soruces defineirt sind

Testing in terminal ausgeben  
- in Verzeichnis wechseln mit git
- mocha todo_test.js

$?  
- Abfrage auf Exit-Code (letzten Befehl welcher ich ausgeführt habe prüfen)

- cat Datei  
öffnet Datei und gibt alle Zeilen in Git

zen coding oder emmet coding  
- Abkürzungen beim Coden, z.B. ul>li*2)




