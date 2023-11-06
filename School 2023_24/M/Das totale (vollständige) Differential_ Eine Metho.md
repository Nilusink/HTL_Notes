---
title: >-
  Das totale (vollständige) Differential: Eine Methode zur Fehlerschätzung und
  Umgang mit Variationen in Funktionen
updated: 2023-10-23 10:46:10Z
created: 2023-10-23 07:13:05Z
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
# Das totale (vollständige) Differential
$$
\LARGE df = { \delta f \over \delta x} dx + { \delta f \over \delta y } dy
$$

$dx$, $dy$, $dz$ (oder $df$) ... "kleine" Abschnitte in die jeweilige Richtung
$df$ ... Gesamtänderung, wenn sich x und y "ein bisschen" ändern (grafisch Buch S. 41)

Anwendung: Fehlersuchung (wenn mehrere Variablen schwanken)

<br>

$$
\LARGE \underbrace { \Delta f }_{ \text { maximaler Gesamtfehler } }  \approx \left | { \delta f \over \delta x } * \Delta x \right | + \left | { \delta f \over \delta y } * \Delta y \right |
$$

Bsp. Buch S. 42 $\rightarrow$ grauer kasten 2.52

#### Bsp von 2.10.2024
$$
\LARGE v = { \Delta s \over \Delta t }
$$
$\Delta s$ und $\Delta t$ schwanken jeweils um $0.5\%$.
?Auswirkung auf v?

$\Large { \delta v \over \delta ( \Delta s ) } = { 1 \over \Delta t }$
$\Large { \delta v \over \delta ( \Delta t ) } = \Delta s (-1 * ( \Delta t)^{ -2 }) = - { \Delta s \over ( \Delta t)^{-2}}$

relativer Fehler $\Large {\Delta v \over v_0}$

$$
\Large \Delta v = \left | { 1 \over \Delta t } * \Delta ( \Delta s) \right | + \left | - { \Delta s \over (\Delta t)^2 } * \Delta ( \Delta t) \right | \newline
\ \newline
{ \Delta v \over v } = { { 1 \over \Delta t } * \Delta (\Delta s) \over { \Delta s \over \Delta t } } + { { \Delta s \over ( \Delta t )^2 } * \Delta (\Delta t) \over { \Delta s \over \Delta t} }= \newline
\ \newline
= { 1 \over \Delta t } * \Delta (\Delta s) * { \Delta t \over \Delta s } + { \Delta s \over (\Delta t)^2 } * \Delta (\Delta t) * { \Delta t \over \Delta s } \newline
\ \newline
= { \Delta (\Delta s) \over \Delta s } + { \Delta ( \Delta t ) \over \Delta t } \newline
\ \newline
= 0.5\% + 0.5\% = \underline { \ \underline { \ 1\% \ } \ }
$$

### Bsp.: Buch S. 42, 2.57

$U = 2h + 2r + \pi * r$
$$
{ \delta u \over \delta) } = 2 + \pi \newline 
\ \newline
{ \delta u \over \delta h } = 2 \newline
\ \newline
\implies \Delta U = \left | ( \pi + 2 ) * 0.3 \right | + \left | 2 * 0.2 \right | = 1.94m \newline
\ \newline 
\ \newline
U_0 = 4.6 * \pi + 18.4 * 2 + 4.6 * 2 = 60.45m \newline
U = 60.45 \pm 1.94m
$$

### Übbung:
Entwickle $y=ln(1+x)$ in eine TR und gib eine Formel an, mit der man ln({0.5, 1.5, 3}) näherungsweise ermitteln kann.

gewählter punkt: 0

$$
f(x) = a_0 * x^3 + a_1 * x^2 + a_2 * x + a_3 \newline
\ \newline
y = ln(1 + x) = ln(1 + 0) = a_0 * 0 + a_1 + 0 + a_2 * 0 + a_3 = a_3 \newline
\implies a_3 = 0 \newline
\ \newline
y' = { 1 \over 1 + x } = { 1 \over 1 + 0 } = 3a_0^2 * 0 + 2a_1 * 0 + a_2 = 0 + 2a_2 + 0 \newline
\implies a_2 = { 1 \over 2 } \newline
\ \newline
y'' = -1 * (1 + x)^{ -2 } * 1 = -1 * 1^{ -2 } = 6a_0 * 0 + 2a_1 \newline
\implies a_1 = { -2 \over 2 } = -1
$$
