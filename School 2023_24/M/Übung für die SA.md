---
title: Übung für die SA
updated: 2023-11-12 17:40:53Z
created: 2023-11-06 08:26:45Z
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
### Bsp. 1
$$
r = 69 \pm 1 mm \newline
h = 132 \pm 1 mm \newline
\ \newline
M = 2 * r * \pi * h = ? \newline
\ \newline
\Delta f_{ (x, y) } = \left | {\delta f \over \delta x } * \Delta x \right | + \left | { \delta f \over \delta y } * \Delta y \right | \newline
\ \newline \ \newline
{ \delta f \over \delta r } = 2 \pi h \newline
 \ \newline
{ \delta f  \over \delta h } = 2 \pi r \newline
\ \newline
= \left | 2 \pi * 132 * 1 \right | + \left | 2 \pi * 69 * 1 \right | \newline
$$
#### relativer Fehler (in r)
$$
{ \Delta y \over y } = { 2 \pi h * \Delta r \over 2 r \pi h } = { \Delta r \over r} \implies { \text { fehler wirkt sich direkt aus (1\% = 1\%) } }
$$
