# Steuerung-Binary
Hier sind die Binaries der Steuerung für den ESP32 abgelegt.  
Das Flashen kann mit den ESP32 Flash Tool erfolgen: https://www.espressif.com/en/support/download/other-tools?keys=&field_type_tid%5B%5D=13

#### Funktionsumfang:
V 0.9 Beta
1. SML-Parser integriert für alle Einheitenzähler, die den Standard unterstützen (über IR-Schnittstelle)
2. Unterstützung für Einrichtungszähler
3. Anzeige von  Wirkverbrauch und Einspeisung (aktuell, heute, gestern) und Gesamtverbrauch
4. Anzeige über LCD 
6. Webserver für http-Zugriff
7. RS485 Schnittstelle und Ansteuerung für Soyosource 1200 Wechselrichter 
8. Batterie-Leer-Erkennung durch Prüfung der Einspeisung alle 10 Minuten
9. Nulleinspeisung durch 3-Step Lastreduzierungs-Algorithmus, Einspeisepunkt ist beliebig
10. Automatischer Accesspoint zum Anmelden im Heimnetz, wenn hinterlegtes Netz nicht gefunden
11. Datum und Zeit automatisch vom Netz (NTP)
12. Sommer- und Winterzeitumstellung (hoffentlich)
13. Data-Logging für Wirkverbrauch und Einspeisung und Zählerstand stündlich mittels SPIFFS (Flash), aktuelles Jahr und Vorjahr
14. Konfigurationsmenü zum Einstellen des Regelverhaltens und der Anzahl der Wechselrichter (bleibt erhalten durch EEPROM)
15. Erkennung von Externem Zugriff und Deaktivierung der Konfigurationsmöglichkeit (nur von 192.168... aus)
16. Fehleralarm beim IR-Datenempfang über LED und Buzzer
17. WLAN Verbindungsverlust Benachrichtigung durch Piepton alle 10 Minuten; automatisches Reconnect
18. Automatisches Einwählen ins Netz bei Neustart
19. "Notlaug" nach Neustart ohne Netzverbindung und Uhrzeit nach 1 Minute ohne Verbindungserfolg   

#### Historie:  
3.3.23: 0.9 Beta Release mit neuem SML Parser zum Test für diverse Zähler, 2 Widerstände gemäß Schaltplan nötig (oder richtiger Lesekopf), alles andere optional  
3.3.23: 0.9_Pullup Beta Release wie vor, aber mit internem 10k-Pullup aktiviert, so dass  Fototransistor direkt an PIN 16 und GND angeschlossen werden kann

