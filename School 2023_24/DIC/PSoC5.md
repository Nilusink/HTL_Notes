---
title: PSoC5
updated: 2023-10-04 10:17:25Z
created: 2023-09-27 09:51:00Z
latitude: 47.29482000
longitude: 16.19914000
altitude: 0.0000
---

<style>
	body {
		font-size: 1.65vw;
		background: white;
		color: black;
	}
	date {
		color: gray;
		font-size: 1.3vw;
	}
	h1 {
		margin-top: 10vw;
		font-size: 5vw;
	}
	h2 {
		margin-top: 8vw;
		font-size: 4vw;
	}
	h3 {
		margin-top: 6.6vw;
	 	font-size: 3.3vw;
	}
	h4 {
		margin-top: 5vw;
		font-size: 2.5vw;
	}
	.merke {
		background-color: rgba(150, 0, 0, 100);
		border-radius: 2.2vw;
		border: .4vw solid red;
		padding: 2.2vw;
		margin: 1.1vw;
		color: white;
	}
	.infobox {
		background-color: rgba(20, 100, 150, 100);
		border-radius: 2.2vw;
		padding: 2.2vw;
		margin: 1.1vw;
		color: white;
		
		transition: all .3s cubic-bezier(0, 1.3, .8, 1.3);
		
		user-select: none;
	}
	.infobox:hover {
		background-color: rgba(30, 120, 180, 100);
	}
	.infobox:active {
		transform: scale(1.1, 1.1);
	}
	re {
		color: red;
	}
	or {
		color: orange;
	}
	strong {
		color: #05f01c;
	}
	.wimage {
		justify-content: center;
		background: white;
		align-items: center;
		padding: 1.1vw;

	}
	.wimagetext {
		flex: 3;
		margin-left: 2.2vw;
		color: black;
	}
	.wimagetext:hover {
		flex: 5;
	}
	.wimageimage {
		flex: 2;
	}
	.wimageimage:hover {
		flex: 3;
	}
	tr {
		background: #333;
	}
    mark {
		border-radius: 5px;
    	padding: 2px;
    }
</style>
# I/O-Komponenten des PSoC5
Kontakt zur Außenwelt
Input / Output = Eingabe / Ausgabe de rArten:
* **GPIO**: General Purpose IO
* **SIO**: Spezial IO
* **USBIO**: USB-Datenverbindung

<br>

Pin-Komponente in PSoC ist für physische Pins z.B. zur Ansteuerung für LEDs, Auswertung Buttons, etc.
Mode für Pins:
* analoger Ein / Ausgang - High Impedance Analog (digital immer 0)
* digitaler Ein- / Ausgang - High Impedance Digital
* Resistive Pullup: Widerstand gegen <mark style="background: #ff6666">VCC</mark>, z.B. Schalter (siehe oben)
* Resistive Pulldown: Widerstand gegen <mark style="background: #000; color: #fff">GND</mark>, z.B. Schalter-Eingang (Siehe Oben)
* Open Drain drive low: Hochomig oder <mark style="background: #000; color: #fff">GND</mark>
* Open Drain drives high: Hochomig oder <mark style="background: #ff6666">VCC</mark>
* Stron Drive: klassischer Ausgangspin (<mark style="background: #ff6666">VCC</mark> oder <mark style="background: #000; color: #fff">GND</mark>)
* Ressistive Pullup + Pulldown: Ausgang wird über Widerstand auf <mark style="background: #ff6666">VCC</mark> oder <mark style="background: #000; color: #fff">GND</mark>

<br>

Im PSoC-Creator gibt es 4 voreinsgestellte Pins: Analog, Digital bidirect, Digital In / Out.

### Konfigurationsmöglichkeiten
* Pin-Editor für die Zuordnung physischer Pins
* Softwarepin ohne Hardwareverbindung (**<or>HW-connection</or>**)
* Analog
  * Verbindung zwischen Pin und analogen System
* Digitaler Input
  * Verbindung von Pin zu digitalen System
  * CPU && DMA (**D**irect **M**emory **A**ccess) können lesen
* Digitaler Output
  * Verbindung von Pin zu digitalen System
  * CPU && DMA können Schreiben
* Bi-Direktional
  * Hauptsächlich für Kommunikationskomponenten wie I^2^C
* Interrupt
  * kurzes Hardware-Programm welches auf Änderungen reagiert
* Output
  * **<or>slew-rate</or>** (Anstieg Ausgangsänderung)
  * **<or>drive-level</or>** (Höhe der Ausgangsspannung)
  * Stromeinstellung
 