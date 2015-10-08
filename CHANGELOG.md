** WPИ-XM Server Stack - http://wpn-xm.org/         Copyright (c) Jens-André Koch.

### Introduction

This document is a curated, chronologically ordered list of notable changes for
each version of WPN-XM.

1. Legend for the desription of changes 

We label changes to describe their impact on the project, as follows:

Type of Change | Description
-------------- | -----------------------------------------------------
| NEW          | for a new feature
| CHG          | for changes in existing functionality
| DPR          | for once-stable features removed in upcoming releases
| REM          | for deprecated features removed in this release
| FIX          | for any bug fixes
| SEC          | to invite users to upgrade in case of vulnerabilities

2. Template

This is a template for a new release section with a few changes:

Date         | Type of Change | Description
------------ | -------------- | -----------
[YYYY-MM-DD] | Unreleased     | VERSION x.y.z 
[2015.MM.DD] | NEW            | added a
[2015.MM.DD] | FIX            | fixed b
[2015.MM.DD] | CHG            | removed c

3. Unreleased Section

The "Unreleased" section at the top is for keeping track of current changes.
At release time, its just changed from "Unreleased" to "Released".
A new "Unreleased" section is added, when the next change is added.

_____________________________________________________________________________

## Change Log

------------  ----------------------------------------------------------------
[2015-MM-DD]  Unreleased  VERSION 0.8.z
------------  ----------------------------------------------------------------
[2015.MM.DD]  NEW   added x
[2015.MM.DD]  FIX   fixed y
[2015.MM.DD]  CHG   removed z

------------  ----------------------------------------------------------------
[21.08.2015]  Release VERSION 0.8.6
------------  ----------------------------------------------------------------

              FIX   component extractions:
                    - "msysgit/git for windows" extracted to "/bin/git"
                    - "gogs" extracted to "/bin/gogs"
                    - Imagick extracted to "/bin/imagick"
                    - PHP extensions extracted to "/bin/php/ext"
              CHG   removed xdebug from PHP7 installers. no release, yet.
              CHG   switched from "msysgit" to "git for windows"

------------  ----------------------------------------------------------------
[12.07.2015]  Release VERSION 0.8.5
------------  ----------------------------------------------------------------

              FIX   installers to stop to inserting global settings
                    into the extension section in php.ini
              CHG   all "Lite Installers" ship "ConEmu"
              FIX   phpext_phalcon download URLs
              FIX   Imagick download URLs
              CHG   switched to Imagick portable zips
              NEW   added "Imagick x64" to "Full Installers x64"
              FIX   removed MoveFiles() from all installers to avoid
                    the folder renaming problem
              FIX   fixed extraction errors of several PHP Extensions and Node
              FIX   default configuration of xdebug from installer
              FIX   fixed paths to the opcache and xdebug in php.ini
              FIX   fixed webinterface cannot redeclare class error
              CHG   removed component "junction"

------------  ----------------------------------------------------------------
[28.06.2015]  Release VERSION 0.8.4
------------  ----------------------------------------------------------------

              FIX   fixed uninstaller to not recursively delete reparse points
              NEW   added redis configuration
              CHG   enabled PHP extensions (by default):
                      mysql, pdo_mysql, pdo_sqlite, sqlite, openssl
  28.06.2015  CHG   server control panel is now released with version number

------------  ----------------------------------------------------------------
[26.06.2015]  Release VERSION 0.8.3
------------  ----------------------------------------------------------------
              RC

  17.06.2015  NEW   added vcredist 2015 detection o LiteRC installer for PHP7

  26.04.2015  CHG   moved configs into subfolders
                    and updated installers accordingly
              CHG   added "COMPILE_FROM_IDE" define to allow local compiles
  25.04.2015  CHG   Removed Debug-Webinstallers and their build tasks
              CHG   added ExecHidden() function to installers
              CHG   moved webgrind config into "/configs/webgrind"
                    and updated installers accordingly
  24.04.2015  FIX   fixed another crash of the SCP
                    (when trying to start the not-installed PostgreSQL)
              CHG   use individual php.ini's per PHP version
  23.04.2015  NEW   improved SSL pre-configuration (added ca-bundle.crt)
                    set cainfo settings to PHP.ini
  15.04.2015  CHG   adjusted batch scripts: replaced %cd% with %~dp0)
                    renamed batch scripts: removed "wpnxm-" prefix
  22.03.2015  NEW   added Strawberry Perl x64
              CHG   x64 versions of the Full Installer include Perl x64
  17.03.2015  NEW   added RoboMongo
              CHG   dropped RockMongo (it's unmaintained).
              CHG   silent installation of VCREDIST

------------  ----------------------------------------------------------------
[14.03.2015]  Release VERSION 0.8.2
------------  ----------------------------------------------------------------

  14.03.2015  FIX   mariadb inital database creation failed
              FIX   updated wpn-xm.ini with missing values
              FIX   missing openssl.conf
              FIX   paths in generate-certificates.bat
              FIX   copy additional nginx config examples (domains-disabled)
              FIX   mariadb extraction error
              FIX   openssl extraction error
              FIX   run PERL relocation script hidden
              CHG   disable deprecated PHP Extensions php_mysql in default cfg
              FIX   ampersand UTF-8 problem in the install wizard by using +
              FIX   rockmongo is no longer extracted to \bin but to \www\tools

------------  ----------------------------------------------------------------
[07.03.2015]  Release VERSION 0.8.1
------------  ----------------------------------------------------------------

  07.03.2015  CHG   Will Travis release it?
                    The gift that he gives to me... No one knows!
                    Using Console mode, without xvfb window.

------------  ----------------------------------------------------------------
20.09.2014    Release Version 0.8.0
------------  ----------------------------------------------------------------

  20.09.2014  CHG   Renamed Installation Wizards

                    There are 4 installation wizard types:
                     - webinstaller
                     - full (formerly bigpack)
                     - standard (formerly allinone)
                     - lite

              CHG   Installation wizards for multiple PHP versions (including x64):

                    Each installation wizards is build for the following PHP versions:
                     - PHP 5.4 x86
                     - PHP 5.5 x86 & x64
                     - PHP 5.6 x86 & x64

              CHG    Deployment to Github, Sourceforge and WPN-XM server

              Milestone Issues

              https://github.com/WPN-XM/WPN-XM/issues?milestone=10&q=is%3Aclosed

              #252 https://github.com/WPN-XM/WPN-XM/issues/252  mongo stop command doesn't work
              #250 https://github.com/WPN-XM/WPN-XM/issues/250  Warning/PHP Startup: Unable to load dynamic library 'ext\php_mongo.dll' - %1 is not a valid Win32 application.
              #244 https://github.com/WPN-XM/WPN-XM/issues/244  Web Installer Failure - 404 on php extension X-cache
              #243 https://github.com/WPN-XM/WPN-XM/issues/243  rockmongo is installed in a versionized folder
              #239 https://github.com/WPN-XM/WPN-XM/issues/239  [build.xml][commit-versionized-registries] workingdir is not found
              #237 https://github.com/WPN-XM/WPN-XM/issues/237  execute stripdown scripts in each "full-version-phpversion-bitsize" folder
              #234 https://github.com/WPN-XM/WPN-XM/issues/234  some php extensions for 5.5 (and 5.6) missing
              #233 https://github.com/WPN-XM/WPN-XM/issues/233  movedownloadfiles misses downloads
              #231 https://github.com/WPN-XM/WPN-XM/issues/231  exchange xhprof with uprofiler
              #229 https://github.com/WPN-XM/WPN-XM/issues/229  add pickle - php extension installer
              #224 https://github.com/WPN-XM/WPN-XM/issues/224  switch buildsystem from nAnt to Phing
              #223 https://github.com/WPN-XM/WPN-XM/issues/223  the imagick core dlls must be filtered out on the php extensions tab (config)
              #222 https://github.com/WPN-XM/WPN-XM/issues/222  "CORE_RL_wand_.dll is missing" error when enabling imagik.
              #219 https://github.com/WPN-XM/WPN-XM/issues/219  Varnish installed under \bin\varnish-3.0.2
              #216 https://github.com/WPN-XM/WPN-XM/issues/216  Add php_uploadprogress extension.
              #212 https://github.com/WPN-XM/WPN-XM/issues/212  /bin/backup folder is not created during install the
              #211 https://github.com/WPN-XM/WPN-XM/issues/211  Starting MongoDB after installation
              #210 https://github.com/WPN-XM/WPN-XM/issues/210  Starting memcached
              #207 https://github.com/WPN-XM/WPN-XM/issues/207  Going from MariaDB 5.5 to 10.0
              #206 https://github.com/WPN-XM/WPN-XM/issues/206  add option to start control panel minimized
              #204 https://github.com/WPN-XM/WPN-XM/issues/204  lift MongoDb version lock (v2.0.8)
              #196 https://github.com/WPN-XM/WPN-XM/issues/196  PostgreSQL is not in control panel
              #195 https://github.com/WPN-XM/WPN-XM/issues/195  Put all the admin folders in "server/www/tools/"
              #194 https://github.com/WPN-XM/WPN-XM/issues/194  Website shows 0.6.0 as Latest Release
              #193 https://github.com/WPN-XM/WPN-XM/issues/193  add php extension phalcon
              #186 https://github.com/WPN-XM/WPN-XM/issues/186  updater: add dialog "building custom registries for installers"
              #152 https://github.com/WPN-XM/WPN-XM/issues/152  show only installed components in the SCP
              #56  https://github.com/WPN-XM/WPN-XM/issues/56   switch between PHP versions

              Commits

              https://github.com/WPN-XM/WPN-XM/compare/0.7.0...v0.8.0

              Version Information

              Please see the website for the full version information of
              software components shipped by the full, standard and lite installation wizards.
              The webinstaller ships latest versions from our registry.

              http://wpn-xm.org/#downloads-list

              Version Information

              Changes (bigpack-0.7.0-w32 -> full-0.8.0-php5.4-w32)

              UPD adminer was updated from v4.0.3 to v4.1.0
              UPD imagick was updated from v6.8.9-0 to v6.8.9-7
              UPD mariadb was updated from v5.5.36 to v10.1.0
              UPD memcached was updated from v1.4.5 to v1.5.7
              UPD mongodb was updated from v2.0.8 to v2.7.6
              UPD nginx was updated from v1.5.13 to v1.7.5
              UPD node was updated from v0.11.12 to v0.11.13
              UPD nodenpm was updated from v1.4.6 to v1.4.12
              UPD perl was updated from v5.18.2.1 to v5.20.1.1
              UPD php was updated from v5.4.27 to v5.4.33
              UPD phpext_amqp was updated from v1.4.0beta2 to v1.4.0
              UPD phpext_imagick was updated from v3.2.0b1 to v3.2.0b2
              UPD phpext_mongo was updated from v1.4.5 to v1.5.7
              DEL phpext_xcache was removed
              UPD phpext_xdebug was updated from v2.2.4 to v2.2.5
              DEL phpext_xhprof was removed
              UPD phpmyadmin was updated from v4.2.0-alpha2 to v4.2.8.1
              UPD postgresql was updated from v9.3.4 to v9.3.5
              UPD rockmongo was updated from v1.1.5 to v1.1.7
              UPD wpnxmscp was updated from v0.6.1 to v0.8.0
              DEL xhprof was removed
              ADD phpext_phalcon v1.3.2 was added
              ADD phpext_uploadprogress v1.0.3.1 was added
              ADD phpext_uprofiler v0.9.2 was added
              ADD pickle v0.1.1 was added
              ADD uprofiler v1.0 was added

              Changes (allinone-0.7.0-w32 -> standard-0.8.0-php5.4-w32)

              UPD adminer was updated from v4.0.3 to v4.1.0
              UPD mariadb was updated from v5.5.36 to v10.1.0
              UPD memcached was updated from v1.4.5 to v1.5.7
              UPD mongodb was updated from v2.0.8 to v2.7.6
              UPD nginx was updated from v1.5.13 to v1.7.5
              UPD php was updated from v5.4.27 to v5.4.33
              UPD phpext_amqp was updated from v1.4.0beta2 to v1.4.0
              UPD phpext_mongo was updated from v1.4.5 to v1.5.7
              DEL phpext_xcache was removed
              UPD phpext_xdebug was updated from v2.2.4 to v2.2.5
              DEL phpext_xhprof was removed
              UPD phpmyadmin was updated from v4.2.0-alpha2 to v4.2.8.1
              UPD rockmongo was updated from v1.1.5 to v1.1.7
              UPD wpnxmscp was updated from v0.6.1 to v0.8.0
              DEL xhprof was removed
              ADD phpext_phalcon v1.3.2 was added
              ADD phpext_uploadprogress v1.0.3.1 was added
              ADD phpext_uprofiler v0.9.2 was added
              ADD pickle v0.1.1 was added
              ADD uprofiler v1.0 was added
              ADD varnish v3.0.2 was added

              Changes (lite-0.7.0-w32 -> lite-0.8.0-php5.4-w32)

              UPD adminer was updated from v4.0.3 to v4.1.0
              UPD mariadb was updated from v5.5.36 to v10.1.0
              UPD nginx was updated from v1.5.13 to v1.7.5
              UPD php was updated from v5.4.27 to v5.4.33
              UPD wpnxmscp was updated from v0.6.1 to v0.8.0
              ADD pickle v0.1.1 was added

------------  ----------------------------------------------------------------
12.04.2014    Release Version 0.7.0
------------  ----------------------------------------------------------------

  12.04.2014  ADD google closure comiler
              ADD node, nodenpm,
              ADD redis
              ADD varnish
              ADD php extensions: amqp, wincache, msgpack, varnish
              UPD WPN-XM SCP (icon bug fix in v0.6.1)

              Milestone / Issues

              https://github.com/WPN-XM/WPN-XM/issues?milestone=9&page=1&state=closed
              + fixed lots of small issues i introduced over time

              Version Information

              https://github.com/WPN-XM/registry/blob/0.7.0/wpnxm-software-registry-bigpack-0.7.0-w32.csv
              https://github.com/WPN-XM/registry/blob/0.7.0/wpnxm-software-registry-allinone-0.7.0-w32.csv
              https://github.com/WPN-XM/registry/blob/0.7.0/wpnxm-software-registry-lite-0.7.0-w32.csv
              Webinstaller -> Latest

------------  ----------------------------------------------------------------
tba           Release Version 0.6.1
------------  ----------------------------------------------------------------

 19.12.2013   UPD  Inno Download Plugin v1.1.0

------------  ----------------------------------------------------------------
19.12.2013    Release Version 0.6.0
------------  ----------------------------------------------------------------

 18.12.2013   This release adresses several bugs in the Server Control Panel:
                   console/debugging popup screen removed
                   daemons not found
                   daemons not started
                   logfile not opened, because wrong path
                   webinterface button not working

              Features

             [server control panel]
              - executable has been renamed from "wpnxm-scp.exe" to "wpn-xm.exe"
              - reworked settings classes
              - enabled configuration dialog
              - added RunOnStartup: places SCP in Windows Autostart)
              - added StopDaemonsOnQuit:
                stops all running daemons, when user Quits the SCP in the Tray
              - added RunDaemonsOnStartup with daemon selection:
                starts daemons, when SCP starts
              - enabled all configuration buttons
                they resolve to the webinterface config section
              - splashscreen added
             [wpn-xm.ini]
              - is the global configuration file used by SCP and Webinterface
              - is auto-generated with default settings by the server control panel
              - with defaults settings is also installed with the stack
             [webinterface]
              - runs with embedded PHP server and also with Nginx (default)
              - has start & stop buttons for daemons

------------  ----------------------------------------------------------------
02.12.2013    Release Version 0.5.4
------------  ----------------------------------------------------------------

 30.11.2013   NEW    webinterface update to work with embedded PHP server
 09.11.2013   NEW    added build tasks
                     prepare-downloads-lite & prepare-downloads-allinone
                     Both move downloads to a specific subfolder.
                     auto-commit-versionized-registries
 07.11.2013   CHG    created registry repository
                     switched from updater to registry submodule
 31.10.2013   FIX    fixing mariadb issue with missing performance_tables
              UPD    NSSM v2.16
 30.10.2013   CHG    software registry files are now versionized
 28.10.2013   NEW    added "wpn-xm-lite-installer-w32"
 25.10.2013   CHG    renamed innosetup script files
                     each postfixed with "-w32"
                     new installer "bigpack" which ships everything (perl).
                     removed perl from "allinone"
 21.10.2013   NEW    added PostgreSQL
 18.10.2013   NEW    added Strawberry Perl, feature request/issue #125
              UPD    Inno Download Plugin v1.0.1 - due to my bugreport :)
 15.10.2013   CHG    switched from InnoTools Downloader to Inno Download Plugin
                     this fixes the https download problems
                     https://github.com/WPN-XM/WPN-XM/issues/114
 26.08.2013   FIX    SSL Certificate Paths in Nginx Config
 06.07.2013   UPD    InnoSetup v5.5.3
 08.04.2013   CHG    renamed wpnxm-scp.exe to server-control-panel.exe
 05.04.2013   NEW    "shutdown blocking" process scan during deinstallation
 01.03.2013   NEW    Nginx loads Domain Configs from /domains-enabled folder
                     Tweaks to MariaDB settings
              FIX    fixed start-menu shortcuts
                     https://github.com/WPN-XM/WPN-XM/issues/89

------------  ----------------------------------------------------------------
tba           Release Version 0.5.3
------------  ----------------------------------------------------------------

              NEW    NGINX 1.3.13
              NEW    PHP 5.4.12
[20.02.2013]  FIX    dialog "Server processes still running" during uninstall
                     shutdown call was invalid
              FIX    removed read-only file permissions from  pthreadGC2.ddl
                     (from /bin/memcached). it was not deleted by uninstall.

------------  ----------------------------------------------------------------
18.02.2013    Release Version 0.5.2
------------  ----------------------------------------------------------------

                     Some entries missing here..

              CHG    removed debug token completely
              NEW    added phpmemcachedadmin
              FIX    removed DEBUG token on bootstrap.php
              NEW    added build tasks "reset-git-submodules",
                     to reset all APPVERSION token changes in git submodules
              NEW    added build tasks "compile-server-control-panel"
                     and "build-server-control-panel"
              NEW    added PHP Extension Mongo 1.3.4
[02.02.2013]  NEW    added RockMongo 1.1.5
                     added version crawler for RockMongo
                     added RockMongo to status, download list and registry
                     added RockMongo to installation wizard
              NEW    registry-update add() handles now also single arrays
              NEW    MongoDB stripdown script and stripdown build task
[01.02.2013]  FIX    /logs directory does not exist on startup
                     https://github.com/WPN-XM/WPN-XM/issues/75

------------  ----------------------------------------------------------------
[21.01.2013]  Release Version 0.5.1
------------  ----------------------------------------------------------------
              https://github.com/WPN-XM/WPN-XM/issues?milestone=5&state=closed

[20.01.2013]  FIX    missing semicolon in nginx.conf
                     missing slash in webinterface/helper/phpini.php
              FIX    uninstall abort dialog did not abort
                     https://github.com/WPN-XM/WPN-XM/issues/71
              FIX    stripdown script and foldernames with spaces
                     https://github.com/WPN-XM/WPN-XM/issues/70
              UPD    updated NANT to v0.92 (2012-06-09)
              NEW    issue #74 - build tasks "stripdown-mariadb"
                     building of the AllInOne Installer is now only one-click
              UPD    issue #69 - software registry out-of-sync

------------  ----------------------------------------------------------------
[19.01.2013]  Release Version 0.5.0
------------  ----------------------------------------------------------------

              NEW    All-In-One Installer
                     PHP 5.4.11, Nginx 1.3.9, XDebug 2.2.1, MariaDB 5.5.28
                     Adminer 3.6.2, phpMyAdmin 3.5.5, Composer, PEAR,
                     APC 3.1.14, Junction, Memadmin 1.0.12, Memcached 1.4.5,
                     MongoDB 2.2.1, OpenSSL 1.0.1c, XHProf 0.10.3,
                     Fake Sendmail, Webgrind, WPN-XM SCP 0.4.0
[13.12.2012]  NEW    build tasks for the All-In-One Installation Wizard
              FIX    fixed start and stop icon names
[12.12.2012]  UPD    InnoSetup v5.5.2
              REM    removed OpenCandy from Installation Wizard builds
              ...
[22.09.2012]  NEW    wpn-xm logo SVG :)
              NEW    experimental vcredistributable2008 check
[20.09.2012]  NEW    experimental portable mode
                     (create no registry key and drop uninstallation)
              NEW    added additional task to innoscript for
                     creation of start stop desktop icons,
                     scp desktop and quick launch icon
[02.09.2012]  NEW    enabled php_com_dotnet extensions by default

------------  ----------------------------------------------------------------
[01.09.2012]  Release Version 0.4
------------  ----------------------------------------------------------------

[31.08.2012]  CHG    sorted all URLS and FILES in the innoscript
[31.08.2012]  NEW    handling of phpext_xhprof
              NEW    added FAKE-SENDMAIL
[31.08.2012]  CHG    disabled extensions zeromq (not compat version atm)
[30.08.2012]  NEW    server-control-panel shutdown already running processes
[23.08.2012]  CHG    webinterface: fixed repository links
              UPD    twitter bootstrap v2.1.0
[13.08.2012]  MOD    website-wpn-xm.org is own git repository now
                     server-control panel is an git submodule now
                     updater is an own git repository now
[07.08.2012]  CHG    copy the installation wizard log into the logs folder
[05.08.2012]  FIX    fastcgi_read_timeout increased for xdebug step debugging
[03.08.2012]  NEW    added MEMADMIN v1.0.12 - Webinterface for Memcached
[23.07.2012]  MOD    webinterface is an git submodule now
[16.07.2012]  NEW    wpnxm-software-registry + get & checkversion script
                     get.php is a redirection script pointing to download urls
                     checkversion uses software registry for version compares
                     wpnxm-software-registry is an auto-updated array of
                     the software components of the stack and their urls
              NEW    added twitters bootstrap css framework to enhance css
                     of the webinterface; adjusted some styles
[05.07.2012]  UPD    Rewrite of Webinterface - using frontcontroller pattern
[03.07.2012]  UPD    Webinterface Updates - Modal Window for Reset Database PW
[02.07.2012]  UPD    UPD ADMINER 3.4.0
              FIX    CSS, font-sizes, shadows
              UPD    innosetup wizard image
              NEW    Webinterface > Configuration > Tab (PHP)
                     AJAX PHP.INI Editor
[26.06.2012]  FIX    PHPMYADMIN default config added
[25.06.2012]  NEW    Website - added screenshot carousel for feature screens
[24.06.2012]  NEW    added HOSTS tool and nginx vhost creation script
                     https://github.com/WPN-XM/WPN-XM/pull/31
[20.06.2012]  NEW    added COMPOSER 1.0 - http://getcomposer.org/
[19.06.2012]  UPD    PHPMYADMIN 3.5.1
[18.06.2012]  CHG    removed hardcoded URLs from Innosetup Scripts
                     download URLs point to a header redirection script
                     https://github.com/WPN-XM/WPN-XM/pull/30
[18.06.2012]  NEW    added icons to config page (php, nginx, mariadb, xdebug)
[18.06.2012]  FIX    getMariaDBVersion() and switched to mysqli methods
[16.06.2012]  UPD    PHP 5.4.4
[15.06.2012]  FIX    build.xml bootstrap.php encoding (read/write token nant)
[15.06.2012]  FIX    installation wizard - uninstaller now working
              NEW    detect running processes before uninstalling
              NEW    dialog to warn user about deletion of projects folder
              FIX    report icon was fetch from the web
              NEW    synced the state (enabled/disabled) of tool pushbuttons
                     in the SCP with the daemon, they rely on (php+nginx)

------------  ----------------------------------------------------------------
[11.06.2012]  Release Version 0.3
------------  ----------------------------------------------------------------

[11.06.2012]  NEW    added WPN-XM SCP 0.3.0
[11.06.2012]  NEW    added base for application settings management to SCP
[08.06.2012]  UPD    MARIADB 5.5.24 w32
                     Our bugreport about inclusion of debug files was included.
                     The download size of maria.zip decreased from 180 to 130mb.
[08.06.2012]  FIX    Status led not updated at initial start
                     https://github.com/WPN-XM/WPN-XM/issues/20
[05.06.2012]  UPD    NGINX 1.2.1
[05.06.2012]  NEW    php is added to environment variable PATH
[04.06.2012]  FIX    fixed cfg edit order: config files are copied, then modified
[04.06.2012]  FIX    installations seems stuck, while extraction of zip files
                     added two progressbars showing total progess and component
[01.06.2012]  UPD    InnoSetup 5.5.0
[11.05.2012]  UPD    PHP 5.4.3
                     APC 3.1.10-5.4
[07.05.2012]  UPD    PHP 5.4.2
              NEW    using stamped icon in installation wizard
[25.04.2012]  FIX    renamed go-pear.php to go-pear.phar
              NEW    added go-pear.bat to startfiles
              NEW    added reset-db-pw.bat to startfiles
              UPD    merged my-medium.ini of MariaDB 5.5.23 into /configs/my.ini
              UPD    bumped version numbers on website
              UPD    added PEAR to wizard images and WPN-XM string to icon
              NEW    added wpn-xm debug.iss for building a debug executable
                     added build task "compile-wpnxm-debug-setup"
[24.04.2012]  UPD    NGINX 1.2.0
                     PHP 5.4.0
                     MARIADB 5.5.23
                     XDEBUG 2.2.0RC2
[19.04.2012]  FIX    download link to junctions was broken (case-sensitive)
              NEW    added opencandy
              FIX    charset problems
                     downgraded to Innosetup 5.4.3 non-unicode
                     used PChar instead of PAnsiChar in innotools downloader
              FIX    user projects were not listed in the projects panel
              NEW    added installation wizard images
              FIX    renamed var Filename_zeromq to Filename_phpext_zeromq
              NEW    added versioning of webinterface during build process
              CHG    updated webinterface menu accordingly
[18.04.2012]  NEW    added PEAR (go-pear.phar) to the stack
[16.04.2012]  NEW    added Adminer 3.4.4 - Database management in one file
[14.04.2012]  NEW    added twitter profile images to /resources dir
[09.04.2012]  UPD    Logo
[12.03.2012]  UPD    readme, website to reflect the ZeroMQ php/ext arrival
              NEW    PHP Extension for ZeroMQ v2.1

------------  ----------------------------------------------------------------
[06.02.2012]  Release Version 0.2
------------  ----------------------------------------------------------------

[06.02.2012]  UPD    NGINX 1.1.11
                     PHP 5.3.10
                     MARIADB 5.3.3-rc
                     XDEBUG 2.1.3
                     PHPMYADMIN 3.4.9
[04.02.2012]  NEW    added OpenCandy Ads to one version of the wizard
[22.01.2012]  NEW    added comments with links to nant & inno setup help
              CHG    build.xml: build directory is now "_build"
              NEW    ISS: define wizard application title and tray message
              NEW    ISS: added SetupLogging and logfile copying to app dir
              NEW    ISS: added bug url to start menu folder
[21.01.2012]  CHG    updated InnoToolsDownloader to be unicode compatible
              NEW    added Mircosoft's junction tool for creation of symlinks
[17.01.2012]  CHG    webinterface
                     fixed centering bugs while displaying phpinfo
                     removed menu.php, welcome.phpin favor of htmlelements.php
              NEW    display counter for welcome message in webinterface
              CHG    gitignore - ignores now QT and build folders
              NEW    NANT build process automation complete
              CHG    build.xml
                     added build command clean-builddir
                     added build command update-iss-files
                     added build command compile-wpnxm-setup
              UPD    PHP 5.3.9
              NEW    added build.xml - the nant buildfile
              NEW    added build.bat - call to nant injecting the buildfile
              NEW    added NANT 0.91 to /bin/nant for build process automation
              NEW    added Inno Setup 5.4.3 Unicode to /bin/innosetup
              CHG    cleanups
                     moved batch build file to /bin/build-old.bat
                     moved setup.ico to /bin/icons folder
                     moved iss files from toplevel to /innosetup folder
[16.01.2012]  FIX    "set PHPRC" is not working; start-wpnxm.bat now changes
                     into the php directory to find the php extensions;
              UPD    phpMyAdmin 3.4.8
              UPD    NGINX 1.1.10
              NEW    link for immediate redirection
[07.12.2011]  CHG    renamed severpack to server stack

------------  ----------------------------------------------------------------
[12.11.2011]  Release Version 0.1
------------  ----------------------------------------------------------------

              NEW    created and set up website wpn-xm.org
                     PHP 5.3.8
                     NGINX 1.1.7
                     XDebug 2.1.2 (PHP Extension)
                     MariaDB 5.3.2-beta
                     phpMyAdmin 3.4.6-english
                     Memcached 1.4.5
                     memcached (PHP Extension)
                     Webgrind
                     Xhprof
                     APC (PHP Extension)
              NEW    selected components for the server stack
              NEW    created base for wpn-xm server control tray application
              NEW    created base for wpn-xm webinterface
              NEW    two ISS files, for standalone and for bundled distribution
[12.06.2011]  NEW    layed out a directory structure for the project

------------    ----------------------------------------------------------------