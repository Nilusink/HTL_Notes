---
title: Fourier Analyse
updated: 2023-12-04 09:10:42Z
created: 2023-11-06 09:29:53Z
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
      mark {
		border-radius: 5px;
    	padding: 2px;
    }
</style>

![Einführung Fourier Analyse](../../_resources/88fafd0674df3717a9af34da46f91ba0.png)
B.S. 64
$$
\Large f(t) = { a_0 \over 2 } + \sum^{ \infty }_{ n=1 } ( a_n * \cos( n \omega_0 t ) + b_n * \sin( n \omega_0 t) ) \ \bigg |_{ \Large { \omega_0 = { 2\pi \over T } } } \newline
\ \newline
a_0 = \frac 2 T * \int_{ 0 }^{ \text { periodendauer } } { f }
$$

## 3.43b
(BS. 63)

![Trapezkurve](../../_resources/3760658494adde3fb613dbb77980a167.png)
$$
T = 3\newline
\ \newline \ \newline
\text { Gerader Teil } \newline
y = 2 \newline
\ \newline \ \newline
\text { Gefälle (Periode von -1 bis 2)} \newline
y = -2 x + 0 \newline
\ \newline \ \newline
a_0 = \frac 2 T * \int_{ -1 }^{ 2 } f(x) \newline
\ \newline \ \newline
\text { Aus dem Buch: } \newline
a(n) \, := \frac 2 T * \int_{ -1 }^{ 2 } f(x) * \cos(n * w * x) \newline \ \newline
b(n) \, := \frac 2 T * \int_{ -1 }^{ 2 } f(x) * \sin(n * w * x) \newline \ \newline
t(x) \, :={ a_0 \over 2 } + \sum_{ 1 }^{ 10 } (a(n) * cos(n*w*x) + b(n) * sin(n*w*x), n, 1, 10)
$$
![Geogebra](../../_resources/c8acf517cbcbcfd5c5024cb84030e746.png)


[Bsp. 3.43](../../_resources/27_11_2023.ggb)

Für das Ergebnis ("Spektrum") wird meist die "Amplituden-Phasen form" verwendet (Buch S. 70) = 
$$
A_0 + \sum_{ n = 1 }^{ \infty } A_n + \sin ( n * \omega_0 * t + \phi_n)
$$

##### "Amplituden- & Phasenspektrum": 
![648e58596708623354046812db43a3f9.png](../../_resources/648e58596708623354046812db43a3f9.png)
$$
\phi_n = 0 \implies \text { reiner Snus } \newline
\phi_n = \pm \frac \pi 2 \implies reiner Cosinus
$$

#### Übung
Bsp 3:
$$
f_{ (t) } ... "Einweg-Gleichrichter"
$$
* FR ?
* Spektrum

![8f86532fec0196122b94c839d82054d5.png](../../_resources/8f86532fec0196122b94c839d82054d5.png)
a~1~ und b~1~ mussten extra ausgerechnet werden, da geogebra keine allgemeine Formel fand, sondern nur eine die ab 2 gilt.
