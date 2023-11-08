---
title: Fourier Analyse
updated: 2023-11-08 08:58:15Z
created: 2023-11-06 09:29:53Z
latitude: 47.26921240
longitude: 11.40410240
altitude: 0.0000
---

<!-- jarvis-summary-start -->
# Summary
The note discusses the concepts of distribution and density in geography. It explains that distribution refers to the way people are spread out across the surface, often shown through a dot map, while density refers to the number of people living in a certain area, usually shown through a choropleth map. The note also highlights the factors that affect distribution and density, including physical factors like relief and climate, and human factors like social and economic factors. Additionally, the note introduces the demographic transition model, which explains population growth patterns in different stages, with factors like birth rates, death rates, and societal changes playing a role.
<!-- jarvis-summary-end -->

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
\Large f(t) = { a_0 \over 2 } + \sum^{ \infty }_{ n=1 } ( a_n * \cos( n \omega_0 t ) + b_n * \sin( n \omega_0 t) ) \ \bigg |_{ \Large { \omega_0 = { 2\pi \over T } } }
$$
