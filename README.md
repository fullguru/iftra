# Seniorentreff

## Einleitung

Dies ist das Repository des Seniorentreffs.

## Installation
* **git init**
* Repository Klonen
* data und public-Ordner auf **777** setzen
* autoload-config: *.local Dateien einfügen
    * Datenbank verbindung anpassen
* ``composer install`` ausführen

## Installation Teil 2 // Assets
* npm install --global npm@latest
* npm install --global gulp-cli
````php
cd public/tools
npm install
````

## Nach einem Update
- den data/cache Ordner leeren

## Neues Modul anlegen
- Modul-Ordner bei **module/** erstellen
- Ordnerstruktur übernehmen **(config + src + view)**
- **module.config.php** + **Module.php** erstellen
- Modul bei **modules.config.php** hinzufügen
- **composer.json**, autoload > psr4: Modul hinzufügen
- Terminal: **composer dump-autoload** (Server: php composer.phar dump-autoload)
- **data/cache** - Dateien löschen

## Assets
``assets`` old css and js files, sometimes still in usage - needs to be changed

``gulp-assets`` new css and js files - minified and optimized + compiled from scss to css.

``src`` new and original files. every change on css or js filed needs to be done in this folder.

file structure: src
* img
* js
* scss
* theme
* vendor

## Deploy + Production
only necessary if you changed something on .scss or .js files

before every git commit or at least git push you need to execute gulp:
````php
cd /public/tools
gulp --prod
````

or use ``composer prepare-commit``