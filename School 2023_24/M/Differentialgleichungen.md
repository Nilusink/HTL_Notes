---
title: Differentialgleichungen
updated: 2024-01-09 09:28:57Z
created: 2024-01-08 08:37:15Z
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
      .defpron {
    	color: #FACA32;
        font-weight: 100;
    	font-size: 1.8vw;
    }

        mark {
		border-radius: 5px;
    	padding: 2px;
    }
</style>
<div class="wimage">
<img class="wimageimage" src="../../_resources/455571dcd52444ddf24eb3cb78733f99.png" width=400>
<div class="wimagetext">

## Maschenregel
$$
\Large -U_0 + R \circ i + \underbrace { U_c }_{ U_C = { q \over C } }
$$
$$
-U_0 + R \circ C \circ U_C'(t) + U_C(t) = 0 \text { und } U_C(t) \newline
\ \newline
\text {Näherung } U_C' \approx { \Delta U_C \over \Delta t } \approx { U_{ C_{ n+1 } } - U_{ C_n }  \over \Delta t }
$$
</div>

</div>

## Beispiel
$$
U_0 = 5 \newline
\Delta t  =0.1 \newline
RC = 1
$$
ggb $\implies$ Tabelle

### Radioaktiver Zerfall
$$
{ dN_{ (t) } \over dt } = c * N_{ (t) }
$$
homogene lineare Differentialgleichung 1. Ordnung (max erste Ableitung) (mit konstanten Koeffizienten)

Fall:
$$
m * { d^2 \over dt^2 } = m * g - k * \left ( { ds \over dt } \right )^2
$$
***
<br>
<div class="infobox">
  <div class="deftitle">Dgl - Differentialgleichung</div>
</div>
<br>

Die Lösung von Differentialgleichung hängt von der Art der Differentialgleichung ab, daher gibt es einige Begriffe zur Klssifizierung
* homogen
  * es sind Summanden enthalten, die die gesuchte Funktion enthalten
* inhomogen
	* es gibt zusätzlich ein Störglied (= Teil, der die gesuchte Funktion NICHT enthält)
* Ordnung der Differentialgleichung
  * höchste vorkommende Ableitung
* linear | nichtlinear
* mit Konstanten / variablen Koeffizienten

# 1. Ordnung
Viele Differentialgleichungen lassen sich mit Hilfe von Seperation (= "Trennung der Variablen") lösen (**alle** ) homogenen und manche inhomogene

z.B: $y' = \frac x y$
Sep: 
$$
{ dy \over dx } = \frac y x \newline
\ \newline
\int { 1 \over y } * dy = \int { 1 \over x } * dx \newline
\ \newline
\ln(|y|) = \ln(|x|) + c \newline
\ \newline
|y| = e^{ \ln(|x|)} + c = e^c * e^{ \ln(|x|)} = \widetilde c * |x|
$$

## Allgemeine Lösung
$y = \underbrace c_ { \text { offene Konstante } } * x \text { (für } x \ge 0)$

falls man eine Zusatzinformationen hat, z.B. dass P(3|4) auf den Graf liegen soll, ergibt sich daraus die "spezielle Lösung"
$4 = c * 3 \implies c = \frac 4 3$
$\implies y_s = \frac 4 3 * x$

### Buch S. 98
#### 4.53a
$$
y' + 6y = 0 \newline
\ \newline
{ dy \over dx } = -6y \newline
\ \newline
\frac 1 y * dy = -6 * dx \newline
\ \newline
\int \frac 1 y * dy = \int -6 * dx \newline
\ \newline
\ln (|y|) = -6x + c \newline
\ \newline
|y| = e^{ -6x + c } = e^c * e^{ -6x } \newline
\ \newline
|y| = \widetilde c * e^{ -6x }
$$

<br>

#### 4.57 a
<div class="infobox">

Trick:
$y' = 3-0.5y$
Dividiere durch die ganze rechte seite (und *dx)
</div>

<br>

$$
y' + 0.5y = 3; \; y_0 = -1 \newline
\ \newline \ \newline
y' = 3 - 0.5y \newline
\ \newline
{ dy \over 3 - 0.5 y} = dx \newline
\ \newline
\int {dy \over 3 - 0.5y } = \int { 1 * dx } \newline
\ \newline
({ -1 \over 0.5})\ln(3-0.5y) = x + c
$$

HÜ: foto von lilo
