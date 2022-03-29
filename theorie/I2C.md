# I²C - Inter-Integrated Circuit

![Aufbau](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3e/I2C.svg/1920px-I2C.svg.png)

- Master-Slave-Bus
- Serieller 2-Draht-Bus
- Bidirektionale Daten- und Taktleitung verwendet
- Mindestens einen Master sowie bis zu 127 Slaves (mehrere Master => "Multi-Master-Bus")
	- Slaves müssen alle mit einer individuellen Adresse codiert werden
	- Broadcastkanal, um alle Slaves anzusprechen

- Adressierung
	- Master sprechen die Slaves jeweils aktiv => Slaves können nie selbstständig beginnen
	- Kommunikation
		- Durch Start-Signal des Master übernimmt der Master den Bus
		- Dieser gibt anschließend Adresse des Slaves aus, mit welchen es kommunizieren möchte
		-  Abhängig vom R/W-Bit werden nun Daten byteweise geschrieben (Daten an Slave) oder gelesen (Daten vom Slave)
		- Anschließend werden die Daten auf den Bus geschrieben
		- Nach dem Lese- bzw. Schreibvorgang: Slave sendet ein Acknowledge (`ACK`) - Master quittiert diesen anschließend (außer beim Broadcast)
	- `Repeated-Start` kann vorkommen, um die erneute Übertragung zu triggern
	- Alle Bytes werden dabei „Most Significant Bit First“ übertragen.
