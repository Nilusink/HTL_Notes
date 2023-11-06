---
title: Leistungsverstärker
updated: 2023-09-19 14:38:46Z
created: 2023-09-19 12:32:38Z
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
<date>19/09/2023 14:37</date>
# Leistungsverstärker
Eingang
* Eingang
	* $U_{ q_1 }$ ... Quellwiederstand
	* $r_{ q_1 }$ ... Spannung
	* $B$ ... Bandbreite

<br>

* Ausgang
	* $R_L$ ... Lastwiderstand
	* $P_L$ ... Leistung (des Lastwiderstandes)

<br>

* Schaltung
	* $r_{ ev }$ ... Eingangswiderstand
		* soll mindestend 20x so hoch sein
	* $r_{ av }$ ... Ausgangswiderstand
	* soll maximal 10 so hoch sein.

$$
P_L  = { U_a^2 \over R_L } \newline
\ \newline
U_a = \sqrt { P_L * R_L } = U_{ a_{ eff } } \newline
\ \newline
\rightarrow \hat U_a = U_{ a_{ eff } } * \sqrt 2
$$

<br>

* Versorgung
	* V~CC~
	* GND
	* C~EE~

$$
|V_{ CC }| = |V_{ EE }| \cong 1.3 * \hat U_a
$$
Aufgrund von Spannungsabfällen sollte die Versorgunsspannung etwa 1.3 * der Spitzenspannung entwprechen

### 2 wesentliche Anforderungen an den Leistungsverstärker:
<div style="font-size: 2.5vw; font-weight: bold;">Linearität</div>

$$
U_a = \overbrace { V_0 }^{ \text { konstant } } * U_E \implies \text { Gegenkopplung! } \newline
\implies \text {Eingangsdifferenzstufe}
$$

#### Wirkungsgrad
$$
\eta = { P_L \over P_{ ges } } \rightarrow \text { mind.  }60\% \implies \text { Gegentackt-Endstufe (AB-Betrieb) }
$$

<br>

Aus den Angaben $P_{ R_L }$ und $R_L$ erfolgt die Auswahl des Leistungstransisors. $P_{ R_L }= xU_{ R_L } \over R_L$

⟹ Darlington AB-Schlatung, S. 188