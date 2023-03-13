Hier führe ich unsortiert nach Eingang einige Möglichkeiten zur Fehlerbehebung auf:

## 1. Flashen klappt nicht ##
Richtige ESP Version?  
Der ESP verbraucht mit WLAN bis zu 700mA Peak. Ein sehr gutes USB Kabel ist zwingend erforderlich und natürlich nur solche mit Datenleitungen. Ebenso mindestens 1A Stromversorgung.  
Ggf. 470u Elko anlöten zur Stabilisierung (ist aber normal nicht erforderlich).

## 2. Flashen klappt, aber Rebootmeldung im Seriellen Monitor: ##
Einmal die 160 Mhz Version testen.  
Vielleicht habt Ihr mit einer anderen Installation zuvor den Bootloader "verbogen"? ESPRESSIF gibt an: At a 0x10000 (64 KB) offset in the flash is the app labelled “factory”. The bootloader will run this app by default. In dem Fall müsste man wohl einmal mit einer Entwicklungsumgebung eine Datei "normal" flashen, um die Standard Partitionierung wieder herzustellen. Bei mir ist das: Default 4MB with spiffs (1.2MB APP/1.5 MB SPIFFS)  
Möglicherweise hilft Euch dieses [Video](https://www.youtube.com/watch?v=3oEvXhgHZHo), wie man ein Factory Reset macht und einen Bootloader neu flasht (habe ich aber nicht ausprobiert) 
Sonst derzeit keine Ideen, woran das liegt.

## 3. Flashen klappt, LED blitzt, aber kein Accesspoint ##
Wenn der ESP (irgendwann einmal zuvor) mit dem Netz verbunden war, verbindet er sich immer wieder, solange er das WLAN findet. Dann muss er auch im [Router](https://github.com/IchBauPV/1.Infos-zu-Beginn/blob/main/Einstellung-Fritzbox.md) 
gelistet sein. 
Möchte man, dass der ESP wieder mit Accesspoint startet, muss man das verbundene Heimnetz-WLAN ausschalten (z.B. Knopf am Router).  
Wenn gar nichts geht, mit seriellem Monitor Meldungen anschauen (115.200).  
Ggf. einmal die 160 Mhz Version testen.

## 4. Flashen klappt, WLAN verbunden, Seite Stromverbrauch kann aufgerufen werden, aber nur, wenn mit PC verbunden ##
Die Stromversorgung ist wahrscheinlich zu schwach. S. Punkt 1 
