#Terminal
- Wie lösche ich einen Ordner?  
rm -d	
- Wie lösche ich einen Ordner mit Inhalt?  
- rm -r
- Wie zeige ich den aktuellen Pfad?  
pwd
- Textdatei erstellen  
touch test.txt 
- Textdatei mit Inhalt erstellen  
echo "blablabl" > test.txt 
- Ordner/Datei unbenennen   
git mv <old name> <new name>

#Gitbash
- Welche Version von GitBash ist installiert?  
npm -v
- Was ist die .idea Datei?  
.idea ist verstecktes Verzeichnis, wird von php storm erstellt 
 
#GIT
- zentrales Repository (centralized version control)  
 alle arbeiten auf dem gleichen Server
- verteiltes repository (distributed version control)  
 jeder arbeitet auf dem eigenen Server  
 auf github.com > Repository > Settings > Collaborators > Add User

- an Zeitform halten, "Settings angepasst" oder "Settings anpassen"
- Was ist die "working directory"  
  hier arbeiten wir immer
- Dateien beim Upload ignorieren. Dazu eine .gitignore im Verzeichnis erstellen und z.B. folgende Dateien auflisten  
- .idea
- .DS_Store
- Thumbs.db  <-- dieser ist wichtig für Windows
- samstag.txt  
- Cheatsheet: http://rogerdudler.github.io/git-guide/
- commit -C         commit -c  
c gleicher Commit wie vorhin, aber Text kann editiert werden  
C gleicher Commit wie vorhin, mit gleichem Text und wird sofort gesendet
- Um Versionskontrolle vom Ordner zu löschen, wir .git Ordner gelöscht

### Commands GIT
- git init  
erstelle neues Repository Verzeichnis
- git status  
zeig mir den aktuellen Status meiner Working Copy


#### Ablauf GIT

##### stage
- git add test.txt  
- von Stage löschen: git reset -- test.txt

##### commit
- git commit -m "mein erster Commit"  
__sehr wichtig: -m verwenden__
- Wenn eine Datei lokal bearbeitet wird und dann commitet wird, steht "modified: test.txt"

##### push
- Verknüpfung github zu local copy  
git remote add origin https://github.com/joelrhenisch/git-test-1.git
- Push der lokalen Commits an remote origin  
git push -u origin master

##### stash
- git stash  
aktueller Stand auf die Seite stehen - erstellt Kopie der Working Copy, auf dieser arbeite ich jetzt
- git stash pop	 
die aktuelle Version wird verworfen und die Sicherung wird wiederhergestellt
- git stash apply
die Änderungen werden zusammen addiert -> es entstehen Konflikte
- git stash list  
alle Änderungen werden aufgelistet

##### Konflikte
- git diff  
zeigt von allen Dateien die Unterschiede an
- git diff test.txt  
zeigt von dieser Datei die Unterschiede an
- gitlog  
so wird aufgezeigt welche Änderungen gestaget wurden
- git fetch  
holt die Änderungen vom Server, liest sie aber nicht ein. d.h. man kann die Versionen vergleichen
- git log origin/master  
sieht die Änderungen vom Kollegen, ohne dass man etwas eingelesen hat
- git diff origin/master  
Unterschiede von überarbeiteten Version vom Kollegen und meiner aktuellen lokalen Version 
- git pull  
es werden alle Daten vom Server geladen - muss immer zuerst gepullt werden, sonst kann nichts gepusht werden

#### SSH-Key erstellen 
- in gitbash folgender Befehl ausführen (Befehl ist für Windows). Jetzt wird der generierte SSH-Key in die Zwischenablage kopiert
$ cat ~/.ssh/id_rsa.pub | clip
- auf github.com/settings/keys  
new ssh key und Schlüssel einfügen. Bei title E-Mail-Adresse einfügen. Jetzt SSH-Key adden

#### Branches (Zweig): Abzweiger von Master
- Master ist immer 100% funktionsfähig
- Branches löschen wenn sie gemerged wurden
- immer in das Zielort wechseln beim mergen, z.b Änderungen von branch1 in master branch --> muss ich in masterbranch wechseln
- Branch erstellen  
git branch test  
- zu Branch wechseln  
git checkout test
- Branch erstellen und wechseln
git checkout -b test
- Branches auflisten  
git branch
- Branch löschen  
git branch -d test
- Branch löschen, auch wenn nicht gemerged  
git branch -D test
- git push -u origin BRANCH-NAME  
Branch pushen
- git push origin --delete test  
löscht Branche
- git checkout master  
wechseln auf masterbranch
- git checkout .  
setzt auf letzten Commit des Branches
- git merge --abort  
merge abbrechen
- Stand vom letzten Remote wiederherstellen  
$ git reset --hard origin/master	löscht auch die Datei, welche den Unterschied gemacht hat  
$ git reset --soft origin/master    Datei ist noch da, muss aber wieder geaddet werden
- git fetch origin  
git reset --hard origin/master  
Alles zurücksetzen auf letzten Stand vom remote origin
- git checkout -- <filename>  
auf den letzten Stand von meinem lokalen Head zurück
- gitk  
eingebaute git-GUI
6