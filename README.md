Džumlaček (Joomla! Czech) WAMP server New Generation
==============
[![verze](https://img.shields.io/github/release-pre/svatas/dzumlacekNG.svg?label=Poslední+verze&style=popout)](https://github.com/svatas/dzumlacekNG/releases) ![datum](https://img.shields.io/github/release-date-pre/svatas/dzumlacekNG.svg?label=ze+dne) [![HitCount](http://hits.dwyl.io/svatas/dzumlacekNG.svg)](http://hits.dwyl.io/svatas/dzumlacekNG) ![stažení](https://img.shields.io/github/downloads/svatas/dzumlacekNG/total.svg?label=Staženo) ![Licence](https://img.shields.io/github/license/svatas/dzumlacekNG.svg?label=Licence) ![repo size](https://img.shields.io/github/languages/code-size/svatas/dzumlacekNG.svg?label=Velikost+zdrojového+kódu)

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
- Adminer v4.1.0 (MySQL Database Manager) (04-18-2014)

Na jedno kliknutí jsou k dispozici:
- Composer (PHP Dependency Manager) (Downloads and installs the latest version)
- PHPUnit (PHP Test Framework) (Downloads and installs the latest version)
- PEAR (PHP Extension and Application Repository) (Downloads and installs the latest version)
- phpDocumentor (PHP Documentation Generator) (Downloads and installs the latest version)
- phpdbg (PHP Debugger) (Command prompt)
- Phalcon Tools (Command Line Utility) (Command prompt)

PHP rozšíření:
- Phalcon v1.3.4 (High Performance PHP Framework) (10-29-2014 32-bit)
- Xdebug v2.2.6 (Debugger and Profiler) (11-15-2014 32-bit)
- Mongo v1.5.6 (MongoDB Driver) (11-11-2014 32-bit)
- OAuth v1.2.3 (Authorization Bindings) (04-10-2014 32-bit)

Download
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
- Password: (prázdné)

Folders
-------
- \amp\app: obsahuje binární soubory aplikací 
- \amp\config: contains custom configurations for the applications
- \amp\doc: contains CHANGELOG, LICENSE, README
- \amp\src: contains C# source code for SSWamp.exe
- \webroot\localhost\public: default location for all web files

Notes
-----
- MySQL binaries are unmodified, but exclude files to make the distribution smaller
- Nginx binaries are unmodified
- PHP binaries are unmodified, but exclude files to make the distribution smaller
- Apache binaries are unmodified, but exclude files to make the distribution smaller

Compatibility
-------------
- The \amp\app folder holds official binaries so the contents of each folder
can be replaced with binaries downloaded from original vendor (PHP extensions
must be updated as well to match the config)
- The \amp\config folder holds custom configurations for the applications
- Each configuration has variables which are replaced by values provided by
SSWamp.exe
- Any changes made to the configurations will apply the next time MySQL, Nginx,
PHP, Apache are started

Technical Notes
---------------
- Nginx uses a highly dynamic configuration which supports multiple websites

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
