---
title: Funktionsweise von I/O Komponenten
updated: 2023-11-29 11:16:52Z
created: 2023-11-06 10:17:34Z
latitude: 47.26921240
longitude: 11.40410240
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
        font-weight: bold;
  }
	strong {
		color: #05f01c;
	}
	.wimage {
		justify-content: center;
		background: white;
		align-items: center;
		padding: 1.1vw;

		display: flex;
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
</style>
# Überblick
Ein µC-System besteht aus mehreren Komponenten:

![µC Aufbau](../../_resources/drawio-{_sketch__true}-2)
## Unterschied Prozessor - Controller
Ein Prozessor (etwa ein i7) braucht immer externe Komponenten (Speicher, ...). Im Zuge der Digitalisierung von Steuerungen verbesserter Fertugungsmöglichkeiten wurden diese Komponenten zusammen mit dem Prozessor in einem Chip integriert. Das daraus entstehende System ist der Microcontroller.

#### Er hat ...
* CPU, Speicher, Takterzeugung, Reset und Komponenten auf einem Chip
* spart somit Platinenfläche und
* ermöglicht kleinere Hardware-Designs

Im Idealfall braucht der µC nur noch eine Versorgungsspannung.

Stand der Dinge: SoC - System on a Chip
Die Idee besteht darin, alle Komponenten auf einem Chip unterzubringen (Ein-Chip-Computer als Basis für Handys).

## CPU
Die CPU, der Microcontrollerkern oder einfach Core, ist das Herzstück des Controllers. Er beinhaltet
* Steuerbefehlsaufarbeitung
* ALU (Rechenwerk)
* Register
* Bussystem zur Ansteuerung aller Komponenten
* Interrupt-Controller

<br>

Er bestimmt mit seiner Bit-Breite, dem Befehlssatz und seiner Architektur die Leistungsfähigkeit des Gesamtsystems.
Beachte dabei die Vesorgungsspannung: 5V/3.3V/1.7V

#### Gängige Type:
| Name                     | Architecture | Instruction Set | RAM   | Clock     |
| ------------------------ | ------------ | --------------- | ----- | --------- |
| Phillips 8XC51-Familie   | 8Bit         | CISC            | 64kB  | bis 33MHz |
| Microchip PIC24F         | 16Bit        | RISC            | 128kB | bis 70MHz |
| Cypress PSoC 5LP ARM CM3 | 32Bit        | CISC            | 256kB | 24 MHz    |

CISC ... <or>C</or>omplex <or>I</or>nstruction <or>S</or>et <or>C</or>omputer
RISC .. <or>R</or>educed <or>I</or>nstruction <or>S</or>et <or>C</or>omputer

## Speicher
Um Daten und Programm speichern zu können, stehen unter anderem folgende Möglichkeiten zur Verfügung:

#### Programmspeicher
* Flash: wiederbeschreibbarer Speicher
* OTP: einmalig programmierbar, für Massenerzeugnisse ohne Update
* NOVRAM: nichtflchtiges RAM (Batterie gepuffert)

Frage: kann das Programm selber den Programmspeicher beschreiben?

#### Datenspeicher
* SRAM: statisches RAM
* EEPROM: dauerhafte Speicherung von Daten, etwa für Setup, langsam

Die Bitbreite hängt von der CPU und dem verwendeten Bus-System ab.
8/16/32 Bit

# Überblick
Wir werden uns im folgenden mit diesen Komponenten beschäftigen:
* GPIO - allgemeine IO-Pins
* UART - asynchrone serielle Schnittstelle
* Timer - Zeitgeber bzw. Ereigniszähler
* ADC - analoge Signale einlesen
* DAC - analoge Signale ausgeben
* SPI - synchrone serielle Schnittstelle

# GPIO
* generelle Aufgabe eines Pins
* Unterschied Analog / Digital-Pin
* Digital-Pin: Drive-Mode
* Read/Modify/Write
* Schaltpegel bei Digital-Pin

<br>

##### Probleme:
* Prellen beim Einlesen eines Tasters
* Achtung: PSoC5 LP
  * Kondensator an Pins 0/2, 0/3, 0/4, 15/2, 15/3, 15/4
  * Debugger an Pins 1/0, 1/1, 1/3
* Zwar lassen sich durch den Pin-Konfigurator logische Pins an beliebige physikalische Pins anschließen, doch hat das System einige dedizierte (OPV, UART/USB-Bridge)

# UART - asynchrone serielle Schnittstelle
##### Aufgabe:
Serieller Datenaustausch zwischen zwei (oder mehreren) Systemen.

<br>

##### Beispiel:
* Anschluss eines Terminals an einem router
* Anschluss einer Bluetooth-Tastatur an einen PC

<br>

##### Wichtige Begriffe / Fragen:
* Half / Full Duplex Betrieb
* UART-Parameter (Baudrate, Parität, Anzahl Stopp-Bits)
* Frame
* wie synchronisiert der Sender den Empfänger?
* Probleme der Baudrate-Generierung
* Pegelanpassung an die physikalische Übertragunsleitung

## Interner Aufbau
Die UART sendet die zu übertragene Daten mit Hilfe eines Schieberegisters vom Sender zum Empfänger Dort werde die serielle Daten wiederrum mittels Schieberegister einlesen.
Wichtig: beide Schieberegister müssen diese Taktung
![UART Aufbau](../../_resources/drawio-{_sketch__true}-1)
<!--System Bus
Read by CPU or DMA		Write by CPU or DMA
RX Data Register	TX Data Register
Receive Shift register	transmit shift register
rx state machine	tx state machine
rx status register	tx status register
8x or 16x ovwersampling	controlregister-->

Der Frame einer UART-Übertragung besteht aus folgenden Teilen

![Protokoll](../../_resources/drawio-{_sketch__true})

<br>

1) Idle: im Ruhezustand immer 1
2) Um den Start einer Pbertraguns anzuzeigen: Flanke 1 ⟹ 0 und Beginn des Start-Bits
3) Datenbits (LSB bis MSB)
4) Optional: Parität
5) Stopp-Bit(s): immer 1 (somit ident zum Idle-Zustand)

<br>

Werden 2 Übertragungen znmittelbar hintereinander durchgeführt, folgt nach dem Stopp-Bit (1) sofort das Start-bit (0) mit der zugehörigen Flanke 1 ⟹ 0

## Interfacing zur Aussenwelt
Das UART-Signal der CPU ist leistungsschwach und daher anfällig für Störungen. Da es direkt von einem CPU-Pin abgegriffen wird, ist dieser - und somit die  gesamte empfindliche CPU - für zerstörende Signale (Überspannung, ...) anfällig.
Daher wird zwischen dem Datenkabel, das die kommunizierenden Systeme verbindet, und der CPU ein Interface-Baustein geschalten.

<br>

##### Zwei Möglichkeiten:
* RS232: kann 2 Systeme miteinander verbinden und verwendet $\pm$ 10V
* RS485: kann bis zu 32 Systeme im Master / Slave-Betrieb verbinden und benutzt ein Differenzsignal

# Timer
## Allgemein
zyklische Ausführung, um in definierte Intervalle arbeiten zu können
(zb. 1x in der Sekunde die Uhr um eine Sekunde weitekr führen)

<br>

##### Realisation:
Zählregister, das mit einem definierten Takt getaktet wird.
Achtung: auf Grund der Breite des Zählregisters /8/16/32 Bit) sind dem System Grenzen gesetzt.

<br>

##### Takt
Dieser wird immer vom Systemtakt (Quart) abgelgeitet

<br>

##### SW-Implementierung
Entweder polling (Status-Register) oder Interrupt (ISR)

## Capture
Mit Hilfe der capture-Funktion ermittelt das System, wann ein externes Signal statt gefunden hat.

* Timer started bei 0 (etwa mit Hilfe eines Triggers)
* wird bei einem dedizierten Eingangspin eine ensprechende Flanke erkannt, wird der aktuelle Wert des Zählers gespeichert.

<br>

##### Beispiel:
* Takt: 1µs
* nach dem Starten des Timers wurde beim Zählstand von 103 am Capture-eingang eine positive Flanke registriert und der Zählstand gespeichert
* Ergebnis: die Flanke trat nach 103µs auf

# Counter
## Allgemein
Asfinag würde David nicht anstellen (mentale Probleme).

##### Takt
Dieser wird of auch extern realisiert.
