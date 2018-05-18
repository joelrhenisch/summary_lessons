MongoDB
JSON kommt rein und JSON kommt raus


Eingabe
insert
 
Lesen
select*from todo
Alles von Tabelle exportieren wo nicht erledigt sind
select*from todo where erledigt = false

doppelte Einträge in Spalte löschen (select distinct spaltenname)

Update
update todo
set erledigt = true
where id = 2;

sobald ich viel lesen muss aus Datenbank, sollte es indexiert werden

Bilder nie in DB ablegen, sondern in Storage
Datum, Stichworte, Aufnahmedatum; solche Informationen gehören in DB. Dazu kommt die Referenz, Datei liegt hier...7

BLOB = Binary large object 

Typen können grösser gemacht werden ohne Verluste, aber nicht kleiner. Sonst werden sie gekürzt. Z.B. VARCHAR(256) to VARCHAR(140)

Unterschied VARCHAR und CHAR: bei VARCHAR benötigt er bei weniger Zeichen als defniert nicht den ganzen Speicherplatz

Erkennen von mysql-system: 3306 Port




JOINS
Daten aus mehreren Tabellen zusammen selektieren

mysqltutorial.org anschauen




Projectmanagmenttool
Projekte



Faustregel was in Index kommt:
alles wo in einem where auftaucht (wo häuffig verwendet wird)


Wenn günstige und teure wheres in einem Query verwendet werden, immer günstige am Anfang verwenden.
z.B. suchen name wo mit "A" anfängt am Anfang suchen, %ie% (ob im Namen ein "ie" ist), kommt ganz am Schluss.
So müssen  bei teueren Anfragen nicht wieder die ganze DB durchsuchen.


wenn json in datenbank verwendet wird, verwendet man nicht mysql, sondern nosql/mongo db



neue Spalte in Navicat erstellen
ALTER TABLE movie ADD new_col varchar(200) NULL
