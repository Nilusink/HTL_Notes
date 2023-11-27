---
title: Optik
updated: 2023-11-10 11:23:09Z
created: 2023-09-29 10:08:04Z
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
# Optik
Berechnung an einzelner spärischer Fläche

![Reflektierung in einem kreis](../../_resources/drawio-{_sketch__false})
$$
{ \sin(\alpha) \over \sin(\beta) } = { n_{ P_L } \over n_L } \newline \ \newline
\sin(\alpha) = \frac G r \implies \alpha = \arcsin \bigg( { 2 \over 3.6 } \bigg) = 33.75° \newline \ \newline
\beta = \arcsin \bigg ( { n_L \over n_{ p_L } } * \sin(\alpha) \bigg ) = \arcsin({ 1 \over 1.43 } * \sin(33.75°) \bigg ) = 21.9°
$$

<br>

$$
\gamma = 180 - 90 - \alpha = 34.25° \newline
\delta = 180 - 90 - \gamma - \beta = 11.8° \newline
\tan(\delta) = \frac G x
$$

<br>

Sinussatz Dreieck AFM
$$
{ \sin(\beta) \over f - r } =  { \sin(180-\alpha) \over y } = { \sin(\alpha) \over y }
$$

achsnahe Strahlen => $y \approx f$
$$
{ n_{ p_L } \over n_L } = { \sin(\alpha) \over \sin(\beta) } = { f \over f-r } \implies f * { n_{ p_L } \over n_L } - r * { n_{ p_L } \over n_L } = f
$$
<br><br>

***
<br><br>
$$
\Large \frac 1 f = \frac 1 b + \frac 1 g \newline
\ \newline
f ... Brennweite
$$

![drawio](../../_resources/drawio-{_sketch__true}-3)
x