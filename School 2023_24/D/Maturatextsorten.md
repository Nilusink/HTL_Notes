---
title: Maturatextsorten
updated: 2023-09-29 11:45:42Z
created: 2023-09-13 10:08:47Z
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

# Maturatextsorten
```mermaid
%%{init: {"flowchart": {"htmlLabels": false, 'curve': 'stepBefore'}} }%%
flowchart LR;
classDef heading fill:#fff,stroke:#fff
classDef item fill:#ccc,stroke:#ccc

0((Maturatextsorten))
style 0 fill:#000,color:#fff,stroke:#000

subgraph 3
	direction LR
	1([beschreibende, analytische + interpretatorische Textsorten]):::heading

	10("Zusammenfassung WAS?
		(Sachtext)"):::item
	11("Textanalyse WAS + WIE?
		(Sachtext)"):::item
	12(Textinterpretation WAS + WIE + Denkung):::item
end
style 3 fill:#eee,stroke:#eee


subgraph 4
	direction LR
	2([argumentative Textssorten]):::heading

	20(Texterörterung):::item
	21("Kommentar
		(Meinungstext in Form
		eines Artikels)"):::item
	22("Leserbrief
		(Meinungstext in
		Briefform)"):::item
	23("Meinungsrede
		(Meinungsrede in der
		Form einer öffentlichen
		Rede)"):::item
end
style 4 fill:#eee,stroke:#eee

0 --- 1 & 2

1 --- 10 & 11 & 12
2 --- 20 & 21 & 22 & 23
```

# Textanalyse
Eine Textanalyse beschreibt und analysiert einen Sachtext nach
* Inhalt
* Form
* Sprache

um seine Wirkung zu erklären
