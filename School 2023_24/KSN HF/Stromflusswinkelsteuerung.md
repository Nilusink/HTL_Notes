---
title: Stromflusswinkelsteuerung
updated: 2023-10-05 07:44:55Z
created: 2023-10-05 07:09:48Z
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
# Stromflusswinkelsteuerung
Wird die Dieodenkennlinie durch eine Wechselschaltung o weit ausgesteuert, dass ein Übergang von Sperrbereich in den Durchlassbereich sehr schnell erfolgt, so kann man die Diodenkennlinie durch eine Knickkennlinie ersetzen.
$\implies$ Diode in Schulterbetrieb

Je nach Lage des AP sind verschiedene Betriebsarten möglich:

**A-Betrieb**: 2$\theta$ = 360°
![A-Betrieb (©melektron)](../../_resources/dc8b39f426907944ebf7c617764e1ad4.png)

**B-Betrieb**: 2$\theta$ = 180°
![B-Betrieb (©melektron)](../../_resources/95702eabf1aaa8c7621264bba50ac674.png)

**C-Betrieb**: 2$\theta$ < 180°
![C-Betrieb (©melektron)](../../_resources/b470d0c1c04cf54d2fe892cf2b010cee.png)

**AB-Betrieb**: (ein kleines bisschen leitend)
