---
title: Schnitstellen
updated: 2023-09-22 12:56:35Z
created: 2023-09-22 12:37:10Z
latitude: 48.20817430
longitude: 16.37381890
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
		color: #13d426;
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
	.wimageimage {
		flex: 2;
	}
	.wimageimage:hover {
		flex: 3;
	}
	tr {
		background: #333;
	}
	.deftitle {
		color: #FFCF38;
		font-weight: bold;
		font-size: 2vw;
	}
</style>

# Schnitstellen

<div class="wimage" style="align-items: flex-start">
	<div class="wimagetext">

## Analog
* VGA
	</div>
	<div class="wimagetext">

## Digital
* USB
	</div>
</div>

<div class="wimage" style="align-items: flex-start">
	<div class="wimagetext">

## Paralell
\+ gleichzeitige Übertragung mmehrerer Datenbits
\+ einfaches Protokoll
\+ Geschwindigkeit
\- höhere Kosten
\- dickere Kabel
\- breitere Buchse
	</div>
	<div class="wimagetext">

## Digital
\- Langsamer (ein bit nach dem anderen)
\- aufwendigeres Protokoll
\+ Kostengünstiger
\+ breiteres Einsatzgebiet (Auch per Funk, Optisch oder Akustisch)
	</div>
</div>

<br>

Von einer **<or>synchronen</or>** Übertragung spricht man, wenn man neben der Datenleitung eine seperate **<or>Taktleitung</or>** hat, und die Datenübertragung synchronzu diesem Takt erfolgt.

Bei einer **<re>asynchronen<re>** Übertragung fehlt die gemeinsame Tektleitung, hier muss sich der Empfänger **<re>eigenständig</re>** auf den sender synchronisieren (aufwendigere Empfängerschaltung).

<br>

* **Full duplex**: gleichzeitiges senden und Empfangen
* **Halbduplex**: entweder der Sender oder Empfänger, aber nicht gleichzeitig

