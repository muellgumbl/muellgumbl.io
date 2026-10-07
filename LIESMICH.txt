MÜLL GUMBL – Version 1.4.0
==========================

Ein kleines virtuelles Haustier für den Browser: Opossum, Dachs, Waschbär,
Klippschliefer & Co. großziehen, füttern, baden, Minispiele spielen
(Käfer fangen, Müll-Digger, Snake, Verlies, Solitär, Poker, Skat, 17+4 ...),
Zimmer einrichten, über die Fußmatte (rechts im Zimmer) in die Stadt gehen, Musik hören.

Läuft ohne Installation, ohne Internet und ohne Anmeldung.


1) SCHNELLSTART
---------------

WINDOWS
  Einfach:     index.html doppelklicken.
  Empfohlen:   START-Windows.bat doppelklicken.
               Das startet einen kleinen Server, der nur auf deinem
               eigenen Rechner läuft, und öffnet http://localhost:8765/
               im Browser. Vorteil: Der Spielstand bleibt auch nach
               Updates zuverlässig erhalten. Das schwarze Fenster
               offen lassen, solange du spielst; zum Beenden schließen.
  Hinweis:     Windows warnt eventuell („SmartScreen“), weil die Datei
               aus dem Internet kommt. Dann „Weitere Informationen“ →
               „Trotzdem ausführen“. Die Skripte sind kurz und lassen
               sich vorher in einem Texteditor lesen.

LINUX
  Einfach:     index.html im Browser öffnen.
  Empfohlen:   Im Terminal im Ordner ./START-Linux.sh ausführen
               (braucht python3, ist fast überall vorhanden; falls
               nötig einmal:  chmod +x START-Linux.sh ).
               Es öffnet http://localhost:8765/ im Browser.

ANDROID
  1. ZIP herunterladen und mit der Dateien-App entpacken.
  2. Firefox für Android öffnen und index.html laden, z. B. über die
     Adresse  file:///storage/emulated/0/Download/MuellGumbl/index.html
     (Pfad an deinen Ordner anpassen).
  3. Chrome kann die Datei oft ebenfalls öffnen, speichert aber nicht
     auf jedem Gerät zuverlässig. Sichere deshalb regelmäßig mit
     „💾 Sichern“ (siehe unten).
  Für Fortgeschrittene: In Termux im Ordner  python3 server.py
  starten und http://localhost:8765/ im Browser öffnen.
  (Auf Android-Geräten ist das Spiel nicht überall getestet.)

Das Spiel braucht einen aktuellen Browser (Chrome, Edge, Firefox,
Brave ...). Ton und Musik starten erst nach der ersten Berührung.


2) SPIELSTAND, SICHERUNG UND UPDATES
------------------------------------

* Dein Spielstand liegt im Browser (localStorage, zusätzlich ein
  Cookie, wenn der Browser das erlaubt) – nicht in der Spieldatei.
* Unten im Spiel gibt es zwei Knöpfe:
    💾 Sichern   speichert eine Datei  muell-gumbl-NAME-DATUM.mgsave.json
    📂 Laden     stellt eine solche Datei wieder her
  Mach vor jedem Update, Browser- oder Gerätewechsel eine Sicherung.
  Die Datei nicht von Hand bearbeiten: Sie ist signiert, bearbeitete
  Dateien werden abgelehnt. Unveränderte Sicherungen lösen keinen
  Manipulationshinweis im Spiel aus.
* UPDATE: Neue ZIP entpacken und die Dateien im selben Ordner
  überschreiben. Danach denselben Browser und denselben Startweg wie
  vorher benutzen:
    - Mit START-Windows.bat / START-Linux.sh bleibt die Adresse
      http://localhost:8765/ gleich – der Spielstand bleibt erhalten.
    - Wenn du index.html direkt öffnest: Ordner und Dateinamen nicht
      ändern (Firefox speichert pro Dateipfad, Chrome/Edge gemeinsam
      für alle lokalen Dateien).
    - Beim direkten Öffnen (file://) nehmen Browser keine Cookies an – dort
      gibt es nur den Browser-Speicher. Sichere deshalb mit „💾 Sichern“,
      bevor du die Datei verschiebst oder eine neue Version entpackst.
* Löschst du Browserdaten/Cookies, ist der Spielstand weg – außer du
  hast eine Sicherung.
* Wenn nach einem Update etwas fehlt: Nichts überspeichern, sondern
  „📂 Laden“ mit der letzten Sicherung benutzen.


3) INHALT DES PAKETS
--------------------

  index.html            das Spiel
  extras/solitaer.html  das Solitär als eigenständige Datei
  START-Windows.bat     Startskript Windows (+ server.ps1)
  server.ps1            kleiner lokaler Server für Windows
  START-Linux.sh        Startskript Linux/macOS (+ server.py)
  server.py             kleiner lokaler Server für Linux/macOS
  LIESMICH.txt          diese Anleitung
  LICENSE.txt           Lizenz (Deutsch und Englisch)
  CHANGELOG.txt         Änderungen
  VERSION.txt           Versionsnummer


4) DATENSCHUTZ (KURZ)
---------------------

Das Spiel sendet keine Daten ins Internet, lädt nichts nach und enthält
keine Werbung, keine Tracker und keine Statistik. Gespeichert wird nur
lokal in deinem Browser: der Spielstand (localStorage und ein Cookie),
Einstellungen wie das Layout und eigene Fotos aus dem Spiel. Beim
Start über START-Windows.bat bzw. START-Linux.sh läuft ein Server nur
auf deinem eigenen Rechner (localhost) und ist von außen nicht
erreichbar.


5) LIZENZ
---------

Kurz: spielen, kostenlos unverändert weitergeben, zeigen, streamen,
Memes/Videos/Screenshots machen – ja. Verkaufen, verändert
veröffentlichen, Teile in ein eigenes Projekt übernehmen oder als
eigene Arbeit ausgeben – nein. Der verbindliche Text steht in
LICENSE.txt.

Kontakt: muellgumbl.wasp766@slmails.com (MülltaucherAhPossum)
