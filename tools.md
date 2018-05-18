Tools
webpack
npm
brew
bower


Jeder Browser hat eigene Engine

Node.js Ist server auf unserem Rechner. (V8 Engine aus Chrome entzogen)


Um npm projekte in meinem Projekt installieren zu können, muss ich zuerst npm init ausführen


node_modules muss zwingend in .gitignore


mit superstatic kann man aus einem ordner einen laufenden webserver generieren (node.js)
einfach befehl superstatic in gitbash eingeben



Taskrunner
- Grunt (mittels config files einstellen)
- Gulp (mit js schreiben)




gulp muss zwingend im projekt installiert sein, so dass jemand gulp auch verwenden kann, wenn er es auf seinem System nicht global installiert sein
npm install gulp --save-dev

global installieren
npm install -g gulp


im Projektordner immer alles in ordner src speichern, ausser package.json und .gitignore. > geht nachher besser mit gulp





funktioniert was nicht?
npm init vergessen? ;)



browsersync
automatisches synchronisierien des browsers
wird für html,css und js gebraucht



nachdem browsersync gestaret wurde, wird der localhost 3000 und 3001 zurückgegeben. das ist die laufende seite und das GUI von browsersync


Editorconfig
Einstellungen für Whitespaces etc.
phpstorm braucht plugin dafür



jslint
Codequalität erhöhen
entweder Einstellungen in IDE setzen oder Projektweise mit .jshintrc file (donwload von google docs) Settings setzen
von wo das projekt die Settings holt, kann in den phpstorm-Einstellungen eingestellt werden


Minification
Leerzeichen, Zeilenumbrüche, Variablennamen werden optimiert und den Browser schneller zu machen


mit yoeman kann man grundlagen herunterladen wie z.b. gulp vorlagen



