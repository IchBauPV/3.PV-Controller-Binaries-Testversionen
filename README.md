# Steuerung-Binary
Hier sind die Binaries der Steuerung für den ESP32 abgelegt.  
Das Flashen kann mit den ESP32 Flash Tool erfolgen: https://www.espressif.com/en/support/download/other-tools?keys=&field_type_tid%5B%5D=13

#### Historie:  
3.3.23: 0.9 Beta Release mit neuem SML Parser zum Test für diverse Zähler, 2 Widerstände gemäß Schaltplan nötig (oder richtiger Lesekopf), alles andere optional  
3.3.23: 0.9_Pullup Beta Release wie vor, aber mit internem 10k-Pullup aktiviert, so dass  Fototransistor direkt an PIN 16 und GND angeschlossen werden kann

#### Aktueller Funktionsumfang:
1. SML-Parser integriert für alle Zähler, die den Standard unterstützen
2. Anzeige von  Wirkverbrauch und Einspeisung (aktuell,heute, gestern) und Gesamtverbrauch
3. Unterstützung für Einrichtungszähler durch 3-Step Lastreduzierungs-Algorithmus
4. Automatischer Accesspoint zum Anmelden im Heimnetz, wenn hinterlegtes Netz nicht gefunden
5. Datum und Zeit vom Netz (NTP)
6. Sommer-Winterzeitumstellung (hoffentlich)
7. Data Logging für Wirkverbrauch und Einspeisung und Zählerstand stündlich mittels SPIFFS (Flash)
8. Konfigurationsmenü zum Einstellen des Regelverhaltens (bleibt erhalten durch EEPROM)
9. Erkennung von Externem Zugriff und Deaktivierung der Konfigurationsmöglichkeit (nur von 192.168... aus)
