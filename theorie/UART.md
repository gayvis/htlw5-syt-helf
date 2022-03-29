# UART - Universal Asynchronous Receiver / Transmitter

![Aufbau](https://cdn.rohde-schwarz.com/pws/solution/research___education_1/educational_resources_/oscilloscope_and_probe_fundamentals/05_Understanding-UART_01_w1280_hX.png)

- Austausch von seriellen Daten zwischen zwei Geräten
- Zwei Drähte zwischen Sender und Empfänger, um in beiden Richtungen zu senden und zu empfangen
- Fünf bis maximal neun Datenbits
- Kommunikation:
	- Simplex-Betrieb: die Daten werden nur in eine Richtung gesendet
	-  Halbduplex-Betrieb: jede Seite sendet, aber nicht zur selben Zeit
	-  Vollduplex-Betrieb: beide Seiten können gleichzeitig senden
-  Arbeitet asynchron - kein gemeinsames Taktsignal, daher:
	-  Startbit signalisiert das Senden von Nutzdatenbits
	-  Stoppbit kennzeichnet das Ende der Nutzdaten
	-  Versand von Nutzdaten: normalerweise mit dem niedrigstwertigen Bit zuerst (Least Significant Bit, LSB)

![Bitversand](https://cdn.rohde-schwarz.com/pws/solution/research___education_1/educational_resources_/oscilloscope_and_probe_fundamentals/05_Understanding-UART_04_w1280_hX.png)

Quelle: https://www.rohde-schwarz.com/at/produkte/messtechnik/oszilloskope/educational-content/uart-verstehen_254524.html
