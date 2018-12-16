Džumlaček (Joomla! Czech) WAMP server New Generation
==============
[![verze](https://img.shields.io/github/release-pre/svatas/dzumlacekNG.svg?label=Poslední+verze&style=popout)](https://github.com/svatas/dzumlacekNG/releases)
[![datum](https://img.shields.io/github/release-date-pre/svatas/dzumlacekNG.svg?label=ze+dne)](https://github.com/svatas/dzumlacekNG/releases)
[![HitCount](http://hits.dwyl.io/svatas/dzumlacekNG.svg)](https://github.com/svatas/dzumlacekNG)
[![stažení](https://img.shields.io/github/downloads/svatas/dzumlacekNG/total.svg?label=Staženo)](https://github.com/svatas/dzumlacekNG/releases)
[![Licence](https://img.shields.io/github/license/svatas/dzumlacekNG.svg?label=Licence)](https://cs.wikipedia.org/wiki/Apache_Licence)
[![repo size](https://img.shields.io/github/languages/code-size/svatas/dzumlacekNG.svg?label=Velikost+zdrojového+kódu)](https://github.com/svatas/dzumlacekNG/releases)

[![podpora](https://img.shields.io/badge/Podporuje-www.joomlaportal.cz-orange.svg)](https://www.joomlaportal.cz)

Přenosné běhové prostředí pro Microsoft Windows, které uživatelům přináší platformu pro testování Joomly.

Historie aplikace sahá do roku 2007, kdy se objevila potřeba mít nějaké jednoduché testovací běhové prostředí do Microsoft Windows.

Projekt prošel několika stádii dle toho, na jakém balíčku pro WAMP byl postaven.

Současná verze je forkem aplikace [SurfStack Wamp](https://github.com/josephspurrier/surfstack-wamp). Nejsou zde prozatím nějaké zásadní změny v kódu, vše je zatím vedeno v úrovni zbavení se kódu, který pro účely Džumlačeku není potřebný.

- není nutno mít něco jiného než Apache, MySQL a PHP
- existuje speciální spouštěcí aplikace pro snadnou správu běhového prostředí

Není nutná žádná instalace, balíček s archivem rozbalte do PC a spusťte aplikaci DžumlačekNG.exe.

Číslo verze Džumlačeku vychází z verze Joomly!, která je v balíčku dostupná.

V tuto chvíli je k dispozici :
- Apache v2.4.10 (Web Server) (10-20-2014 32-bit VC11)
- MySQL v5.6.21 (Databáze) (09-23-2014 32-bit)
- PHP TS v5.6.0 (Skriptovací jazyk) (08-28-2014)
- Adminer v4.1.0 (Správce databáze MySQL) (04-18-2014)
- Joomla! 3.9.1 (Redakční systém alis Content Management) (11-27-2018)

Na jedno kliknutí jsou k dispozici:
- Composer (Správce PHP závislostí) (Downloads and installs the latest version)
- PHPUnit (PHP Testovací Framework) (Downloads and installs the latest version)
- PEAR (Repozitář PHP rozšíření a aplikací) (Downloads and installs the latest version)
- phpDocumentor (Generátor PHP dokumentace) (Downloads and installs the latest version)
- phpdbg (PHP Debugger) (Command prompt)
- Phalcon Tools (Utilita do příkazové řádky) (Command prompt)

PHP rozšíření:
- Phalcon v1.3.4 (High Performance PHP Framework) (10-29-2014 32-bit)
- Xdebug v2.2.6 (Debugger a Profiler) (11-15-2014 32-bit)
- Mongo v1.5.6 (Ovladač MongoDB) (11-11-2014 32-bit)
- OAuth v1.2.3 (Autorizační rozšíření) (04-10-2014 32-bit)

Stažení
------------
Poslední verze [v3.9.1](https://github.com/svatas/dzumlacekNG/releases) (13-12-2018).

Instrukce
------------
1. Rozbalte obsah balíčku do libovolné složky
2. Spusťte **dzumlacekNG.exe**
3. Zatrhněte zatržítko u každého serveru, který chcete spustit
4. Klikněte na tlačítko **Spustit**
5. Stiskněte tlačítko **Joomla! Frontend** pro uživatelskou část Joomly! nebo tlačítko **Joomla! Backend** pro správcovské rozhraní

Výchozí nastavení MySQL Databáze
-------------------------------
- Jméno databáze: DNG
- Uživatelské jméno: root
- Heslo: (prázdné)

Složky
-------
- \amp\app: obsahuje binární soubory aplikací
- \amp\config: obsahuje upravené konfigurační soubory aplikací
- \amp\doc: obsahuje CHANGELOG, LICENSE, README
- \amp\src: obsahuje C# zdrojový kód pro apikaci DzumlacekNG.exe
- \webroot\localhost\public: výchozí složka pro instalaci Joomly!

Poznámky
-----
- Binární soubory MySQL jsou nezměněné, můžete odstranit nepoužívané soubory a distribučná soubor bude menší
- Binární soubory PHP jsou nezměněné, můžete odstranit nepoužívané soubory a distribučná soubor bude menší
- Binární soubory Apache jsou nezměněné, můžete odstranit nepoužívané soubory a distribučná soubor bude menší

Kompatibilita
-------------
- Složka \amp\app obsahuje oficiální binární soubory aplikací, proto je můžete kdykoliv nahradit originálními soubory vyšší verze přímo od dodavatele (PHP rozšíření musíte také aktualizovat)
- Složka \amp\config obsahuje upravené konfigurace aplikací
- Každý konfigurační soubor obsahuje proměnné, které budpou nahrazeny hodnotami dodanými programem DzumlacekNG.exe
- Jakékoliv změny v konfiguracích budou aplikovány při dalším spuštění MySQL, PHP nebo Apache.

Website Simulation
------------------
To resolve any domain like www.example.com on your local system, add the domain
name to your system hosts file:

1. Copy C:\windows\system32\drivers\etc\hosts to your desktop
2. Open the hosts file in Notepad
3. Add the following lines to the bottom of the hosts file:
4. 127.0.0.1  example.com
5. 127.0.0.1  www.example.com
6. Save the modified hosts file
7. Copy the modified hosts file back to: C:\windows\system32\drivers\etc\hosts
8. Close your web browser if open
9. Run SSWamp.exe
10. Place a check next to the Apache option
11. Click Turn On
12. Test the configuration by opening your web browser to: http://example.com

Quick Solutions
---------------
- Unblock all files on Windows Vista or Windows 7 if prompted
- Allow Apache, Nginx, MySQL, MongoDB, Memcached, and SSWamp.exe through the
firewall if prompted
