---
title: Automaten
updated: 2023-09-27 09:42:11Z
created: 2023-09-20 10:10:49Z
latitude: 48.15350000
longitude: 16.38550000
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

```mermaid
flowchart TD;
classDef noBox fill:#fff,stroke:#fff
classDef autoBox fill:#666,color:#fff

	e["Eingang"]:::noBox;
	a["Ausgang"]:::noBox;

	fu["Fü"]:::autoBox;
	as["AS"];
	fa["FA"];

	fu ==> as;
	as ==> fu & fa;

	e ==> fu & fa;
	fa ==> a;
```
