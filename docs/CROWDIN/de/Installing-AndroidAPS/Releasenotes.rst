Release notes
*****
Eine Schritt-für-Schritt-Anleitung des Updates findest Du `hier <../Installing-AndroidAPS/Update-to-new-version.html>`_. Auf dieser Seite gibt es auch einen Abschnitt mit möglichen Schwierigkeiten und Lösungsansätzen.

Folgende Information wird angezeigt, so bald ein neues Update zur Verfügung steht:

.. image:: ../images/AAPS_LoopDisable90days.png
  :alt: Update info

Dann hast Du 60 Tage Zeit, das Update durchzuführen. Wenn Du nicht innerhalb dieser 60 Tage updatest, wird AndroidAPS in den LGS-Modus (Reduzierung der Basalrate bei niedrigen Glukosewerten, keine Korrektur zu hoher BZ-Werte - siehe `Glossar <../Getting-Started/Glossary.html>`_) wie im  `Ziel (objective) 4 <../Usage/Objectives.html>`_ beschrieben.

Wenn Du auch weitere 30 Tage (90 Tage ab dem neuen Release-Datum) nicht aktualisierst, wird AAPS auf Open Loop wechseln.

Bitte verstehe, dass diese Änderung nicht dazu dient, die Anwender zu gängeln, sondern aus Sicherheitsgründen erfolgt. Neue Versionen von AndroidAPS bieten nicht nur neue Funktionen, sondern auch wichtige Sicherheitsfixes. Deshalb ist es notwendig, dass jeder Anwender so schnell wie möglich aktualisiert. Leider gibt es noch Fehlerberichte aus sehr alten Versionen, so dass dies ein Versuch ist, die Sicherheit für jeden einzelnen Benutzer und die gesamte DIY-Community zu verbessern. Danke für dein Verständnis.

Version 2.5.1
=====
Erscheinungsdatum: 31.10.2019

Bitte beachte die `wichtigen Hinweise <../Installing-AndroidAPS/Releasenotes.html#wichtige-hinweise>`_ und `Beschränkungen <../Installing-AndroidAPS/Releasenotes.html#kann-ich-dieses-update-nutzen-aktuell-werden-noch-nicht-unterstutzt>`_, die bei `Version 2.5.0 <../Installing-AndroidAPS/Releasenotes.html#version-2-5-0>`_ aufgeführt sind. 
* Es wurde ein Fehler im Netzwerk-Status-Empfänger behoben, der zu einigen Abstürzen geführt hat (nicht kritisch, würde aber viel Energie verbrauchen auf Grund der ständigen Neuberechnungen).
* Eine neue Versionssteuerung, die es ermöglicht, kleinere Aktualisierungen durchzuführen, ohne die Aktualisierungsbenachrichtigung auszulösen.

Version 2.5.0
=====
Erscheinungsdatum: 26.10.2019

Wichtige Hinweise
-----
* Verwende `Android Studio Version 3.5.1 <https://developer.android.com/studio/>`_ oder neuer `um die App zu erstellen <../Installing-AndroidAPS/Building-APK.html>`_ oder `ein Update durchzuführen <../Installing-AndroidAPS/Update-to-new-version.html>`_.
* Wenn Du xDrip+ verwendest, muss `identify receiver <../Configuration/xdrip.html#identifiziere-empfanger>`_ gesetzt sein.
* Falls Du den Dexcom G6 mit der `gepatchen Dexcom App <../Hardware/DexcomG6.html#g6-mit-der-gepatchten-dexcom-app>`_ verwendest, benötigst Du die Version aus dem `2.4 Ordner <https://github.com/dexcomapp/dexcomapp/tree/master/2.4>`_.

Kann ich dieses Update nutzen? Aktuell werden NOCH NICHT unterstützt:
-----
* Android 5 oder niedriger
* Poctech
* 600SeriesUploader
* Glimp
* Patched Dexcom App aus dem Verzeichnis 2.3

Wichtige neue Funktionen
-----
* Interne Änderung des targetSDK auf 28 (Android 9), Jetpack-Unterstützung
* RxJava2, Okhttp3, Retrofit support
* Alte `Medtronic Pumpen <../Configuration/MedtronicPump.html>`_ werden unterstützt (RileyLink erforderlich)
* Neues Plugin `Automation <../Usage/Automation.html>`_
* Möglichkeit, `nur einen Teil des vom Bolus-Rechner ermittelten Bolus <../Configuration/Preferences.html#erweiterte-instellungen>`_ abzugeben
* Darstellung der Insulinaktivität
* Anpassung der IOB-Vorhersagen auf Basis der Autosens Ergebnisse
* Neue gepatchte Dexcom App (`2.4 Ordner <https://github.com/dexcomapp/dexcomapp/tree/master/2.4>`_)
* Signaturprüfung
* Möglichkeit für OpenAPS Anwender, die Ziele (Objectives) zu überspringen
* Neue `Ziele (objectives) <../Usage/Objectives2019.html>`_ -  Wissens-Check & App-Bedienung
   
   (Wenn Du mindestens mit dem Ziel "Starte den Open Loop" in einer vorhergehenden Version begonnen hast, ist der Wissens-Check optional.)
* Fehlerbehebung Dana Treiber, bei dem eine falsche Zeitdifferenz angegeben wurde
* Fehlerbehebung `SMS-Befehle <../Usage/SMS-Commands2019.html>`_

Version 2.3
=====
Erscheinungsdatum: 25.04.2019

Wichtige neue Funktionen
-----
* Wichtiger Sicherheitsfix für Insight (wirklich wichtig, wenn Du die Insight nutzt!)
* Bugfix History-Browser
* Bugfix Delta-Berechnungen
* Sprach-Updates
* Überprüfung git und Warnung bei gradle Upgrade
* Zusätzliche automatische Tests
* Bugfix eines potentieller Absturzes des Alarm Sound Dienstes (Danke @lee-b!)
* Bugfix BG-Broadcast (funktioniert nun unabhängig von den SMS-Berechtigungen!)
* Neuer Versionscheck


Version 2.2.2
=====
Erscheinungsdatum: 07.04.2019

Wichtige neue Funktionen
-----
* Korrektur Autosens: deaktiviert TT Anstiege / senkt Zielwert
* Neue Übersetzungen
* Korrekturen Insight Treiber
* Korrektur SMS-Plugin


Version 2.2
=====
Erscheinungsdatum: 29.03.2019

Wichtige neue Funktionen
-----
* Anpassung Assistent für die `Zeitumstellung <../Usage/Timezone-traveling.html#zeitumstellung-sommer-winterzeit>`_
* Wear Update für die Smartwatch
* Update `SMS plugin <../Usage/SMS-Commands2019.html>`_
* Möglichkeit, bei den Objectives (Zielen) zurück zu gehen
* Unterbrechung des Loop wenn Speicherplatz des Smartphones aufgebraucht ist.


Version 2.1
=====
Erscheinungsdatum: 03.03.2019

Wichtige neue Funktionen
-----
* Unterstützung für `Accu-Chek Insight <../Configuration/Accu-Chek-Insight-Pump.html>`_ (von Tebbe Ubben und JamOrHam)
* Statusanzeige auf dem Hauptbildschirm (Nico Schmitz)
* Assistent für die Zeitumstellung (Sommer-/Winterzeit - Roumen Georgiev)
* Korrektur der Verarbeitung von Profilnamen, die von Nightscout übertragen werden (Johannes Mockenhaupt)
* Sperre des User Interface behoben (Johannes Mockenhaupt)
* Unterstützung für die aktualisierte G5-App (Tebbe Ubben und Milos Kozak)
* G6, Poctech, Tomato, Eversense als BZ-Quelle (Tebbe Ubben und Milos Kozak)
* Korrektur deaktivieren SMB Präferenzen (Johannes Mockenhaupt)

Verschiedenes
-----
* Falls Du ein vom Standard abweichenden smbmaxminutes Wert nutzt, musst Du diesen erneut eingeben.


Version 2.0
=====
Erscheinungsdatum: 03.11.2018

Wichtige neue Funktionen
-----
* Oref1/SMB wird unterstützt (`oref1 documentation <https://openaps.readthedocs.io/en/latest/docs/Customize-Iterate/oref1.html>`_). Bitte lies zuerst die Dokumentation, damit du weißt was du davon erwarten kannst, wie es funktioniert, was der SMB erreichen kann und wie er zu benutzen ist, damit er gut arbeitet.
* Unterstützung für `_Accu-Chek Combo <../Configuration/Accu-Chek-Combo-Pump.html>`_
* Setup Wizard: Der neue Assistent führt dich durch die Einrichtung von AndroidAPS.

Einstellungen, die bei Umstellung von AMA zu SMB erforderlich sind
-----
* Objective 8 muss gestartet sein, damit die SMB-Funktion zur Verfügung steht (der SMB-Reiter zeigt dir, welche Beschränkungen bestehen).
* maxIOB enthält nun das gesamte IOB, nicht nur das hinzugefügte Basalinsulin. Das bedeutet: Wenn du einen Bolus von 8 IE gegeben hast und maxIOB ist 7, dann wird kein SMB ausgelöst, solange das Gesamt-IOB nicht wieder auf unter 7 IE abgefallen ist.
* Der Standardwert von min_5m_carbimpact erhöht sich von 3 bei AMA auf 8 beim SMB. Wenn du also von AMA auf SMB umstellst, dann musst du den Wert manuell auf 8 erhöhen.
* Bitte beachte beim Erstellen einer AndroidAPS 2.0 apk: Configuration on demand wird in der aktuellen Version des Android Gradle Plugins nicht unterstützt! Wenn der Build-Prozess mit einem Fehler zu "on demand configuration" fehlschlägt, dann kannst du folgendes tun:

   * Das Einstellungen-Fenster öffnen, indem du auf Datei > Einstellungen (auf dem Mac: Android Studio > Preferences) klickst.
   * Klicke im linken Fensterbereich auf Build, Execution, Deployment > Compiler.
   * Deaktiviere die "Configure on demand" Checkbox.
   * Klicke Apply oder OK.

Übersichtsseite
-----
* Im oberen Menüband (Abschnitt A) kannst du durch langen Fingerdruck den Loop pausieren oder deaktivieren, die Pumpe trennen, das aktuelle Profil anzeigen und einen Profilwechsel machen, sowie temporäre Ziele (temp targets - TT) einstellen. Die temporären Ziele verwenden Standardwerte, die du in den Einstellungen festlegen kannst. Das neue Standard-Ziel “HypoTT” löst ein temporäres Ziel im höheren BZ-Bereich aus, damit der Loop nicht überreagiert nachdem du Korrektur-Kohlenhydrate gegessen hast.
* Neue Behandlungs-Schaltfläche: die alte Behandlungs-Schaltfläche ist weiterhin verfügbar, aber standardmäßig deaktiviert. Du kannst jetzt selbst einstellen, welche Schaltflächen du auf dem Home-Screen haben willst. Neue Buttons für Insulin und Kohlenhydrate (inkl. `eCarbs/extended carbs <../Usage/Extended-Carbs.html>`_)
* `Farbige Vorhersagelinien <../Getting-Started/Screenshots.html#abschnitt-e>`_
* Option in den Dialogen für Insulin, Kohlenhydrate, Rechner und Füllen/Vorfüllen ein Feld für Bemerkungen, die zu Nightscout hochgeladen werden, anzuzeigen.
* Überarbeiteter Füllen/Vorfüllen-Dialog. Möglichkeit, gleichzeitig Careportal-Einträge für Katheter- und Reservoirwechsel zu erstellen.

Watch
-----
* Auf die separate Build Variante “wearcontrol” wird verzichtet, die Smartwatch-Steuerung ist jetzt in der full build Variante enthalten. Um die Bolus-Steuerung auf der Smartwatch zu verwenden, musst du dies in AAPS auf dem Smartphone aktivieren.
* Der Rechner wird nur noch nach Kohlenhydraten (und - falls aktiviert - nach einem Prozentsatz) fragen. Du kannst in den Einstellungen auf dem Smartphone festlegen, welche Parameter bei einem Bolus, der von der Smartwatch aus gegeben wird, in die Berechnung einbezogen werden sollen.
* Bestätigungen und Info-Dialoge funktionieren jetzt auch unter Android Wear 2.0 gut.
* eCarbs Menüeintrag hinzugefügt

Neue Plugins
-----
* PocTech App als BZ-Quelle
* Dexcom App (patched) als BZ-Quelle
* Oref1 Empfindlichkeitserkennung

Verschiedenes
-----
* Die App verwendet jetzt “drawer”, um alle Plugins zu zeigen. Alle Plugins, die im Konfigurations-Generator als sichtbar markiert sind, werden als Reiter im oberen Bereich (Abschnitt A) angezeigt (Favoriten).
* Überarbeitung des Konfigurations-Generators und des Objectives-Reiters. Beschreibungen hinzugefügt.
* Neues App-Icon
* Viele weitere Verbesserungen und Fehlerbehebungen.
* Von Nightscout unabhängige Alarme wenn die Pumpe über längere Zeit nicht erreichbar ist (z.B.  schwache Pumpenbatterie) und bei verpassten CGM-Werte (siehe lokale Alarme in den Einstellungen).
* Option, das Display immer an zu lassen.
* Option, die Hinweise als Systemmeldungen anzuzeigen.
* Advanced filtering (das erlaubt die Nutzung von “SMB immer an” und “6 Stunden nach dem Essen”) wird unterstützt mit der gepatchten Dexcom App (nicht mit der originalen Dexcom App!) oder xDrip mit dem G5 native mode als BZ-Quelle.
