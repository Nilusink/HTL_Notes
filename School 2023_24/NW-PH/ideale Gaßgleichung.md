---
title: ideale Gaßgleichung
updated: 2024-01-19 13:46:15Z
created: 2024-01-19 10:42:39Z
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
    	margin-top: 5vw;
    	margin-bottom: 5vw;
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
	.wimageimage {
		flex: 2;
	}
	.wimageimage:hover {
		flex: 3;
	}
	.deftitle {
		color: #FFCF38;
		font-weight: bold;
		font-size: 3vw;
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
$$
\Large \overbrace{ p }^{ \text { pressure } } * \underbrace { V }_{ volume } = 
\overbrace { N }^{ \text { n particles } } * \underbrace { k }_{  } * \overbrace { T }^{ temperature }
$$

### Historisch
2\. Gesetz von Charles (1783)
$
p = const (Ballon) \newline
isobar \newline
\frac V T = const
$

<br>

2\. Gesetz von Gay-Issac (ca. 1800)
$
v=const \newline
isochor \newline
\frac p T = const
$

3\.
$
T=const \newline
isotherm \newline
p * V = const
$

### Experiment
Glaszylinder, der zusammengeschoben wird

| l (cm) | p (bar) | l * p |
| ------ | ------- | ----- |
| 25     | 1       | 25    |
| 21     | 1.15    | 24.15 |
| 17     | 1.4     | 23.8  |
| 14     | 1.7     | 23.8  |
| 10     | 2.4     | 24    |
| 8      | 2.9     | 23.2  |
| 6      | 3.8     | 22.8  |

Hier kann $l*p$ als Überprüfung gesehen werden. Das Volumen $(V)$ kann hier durch die Länge $(l)$  ersetzt werden, da das Volumen durch $V = l * A$ berechnet wird und die Fläche $(A)$ konstant bleibt.

# Ursprung der Kelvin Skala
Charles hat mit Ballonen experimentiert ($p=const$).

$$
V = V_0 * (1 + \underbrace { \gamma }_{ \text { Wärmedehnungskoeffizient in 3D } } * \Delta T) \newline
\, \newline
V_0 = V_M ... Molvolumen \newline
\text { bei 1 Mol Gas } \newline
V_M = 22.4 dm^3
$$

<br>

für verschiedene Gase ist $\gamma$ gleich.
$$
\gamma = 0.0036609921 = { 1 \over 273.15} \newline \, \newline
V = V_0 * \left ( 1 + { \Delta T \over 273.15 } \right ) = V_0  { 273.15 + \Delta T \over 273.15 } \newline \, \newline
\large \implies \frac V T = const \,\,\,\, ( \text { Gesetz von Charles } )
$$
![Gas Volume over Temperature](../../_resources/drawio-{_sketch__true}-6)

<br>

### Beispiel 1:
Ein Heliumballon hat bei 1 bar Luftdruck ein Volumen $V_1 = 2m^3$. Auf dem Mt. Everest herrschen nur 0.691 bar Luftdruck.
Falls sich die Temperatur beim Aufsteigen nicht ändern würde, wie groß wäre nun $V$ am Gipfel?

<br>

$$
p * V = N * k * T \newline \, \newline
{ p_0 \over p_e } = { V_e \over V_0 } \newline \, \newline
V_e = V_0 * { p_0 \over p_e } \newline \, \newline
V_e = 2m^3 * { 1 \over 0.691 } = 2.894m^3
$$

<br>

bei Temperaturänderung:

$$
{ p_0 \over p_e } = { V_e  * T_0 \over V_0 * T_e }
$$

<br>

### Beispiel 2
Im Winter werden $p_1 = 2.2 bar$ überdruck bei $-20° C$ in den Reifen gefüllt. Wie groß ist $p_2$ im Sommer bei 40°C?

$
V, N, k = constant \newline \, \newline
$
$$
{ p_1 \over p_2 } = { T_1 \over T_0 } \newline \, \newline
p_2 = p_1 + { T_0 \over T_1 } = 2.2bar * { 273.15 + 40 \over 273.15 - 20 } = 2.721 bar
$$

