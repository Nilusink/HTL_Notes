---
title: Arbeitsblatt
updated: 2023-10-19 07:14:47Z
created: 2023-10-05 09:26:11Z
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
# Dateioperationen
### Ins Homeverzeichnis wechseln
![console output](../../_resources/b914cbe8ad6bd29f0e34c6e18894c303.png)

### Alle Dateien an deren 2ter stelle ein "o" liegt
![console output](../../_resources/d564a30bf030d99d09e2cd4b97f0b61f.png)
Einen ordner ersetllen und in in hinein wechseln
![2c0ba218f96f753ca02abc34f22d2c57.png](../../_resources/2c0ba218f96f753ca02abc34f22d2c57.png)
oder (mittels hilfs-function):
![4c407d89b410e04c2b4a38ce073119d4.png](../../_resources/4c407d89b410e04c2b4a38ce073119d4.png)
![2cba6c87c15f396a55b81bcb1cea5fae.png](../../_resources/2cba6c87c15f396a55b81bcb1cea5fae.png)
### 2: Eingabe / Ausgabe
![9c28f5de8feed8f268dc7f6bdb8365f1.png](../../_resources/9c28f5de8feed8f268dc7f6bdb8365f1.png)
### 3: Hilfe
```bash
man chmod
```
![001cdbb1407a3faa1f9973fbd7d5e5d2.png](../../_resources/001cdbb1407a3faa1f9973fbd7d5e5d2.png)
``` bash
man groups
```
![18701383b16c85a11a9658f8f172014e.png](../../_resources/18701383b16c85a11a9658f8f172014e.png)
Befehle
* cat

### C-Programme
```
nvim add.c
```
![830d28df3aab21ac22cf7949586c71d6.png](../../_resources/830d28df3aab21ac22cf7949586c71d6.png)
Berechtigungen wurden nicht geändert, da eine .c Datei auf **keinen** Fall execute-Berechtigungen besitzen sollte.
![487e07027c9b8819cf9cc3f7e22f99a1.png](../../_resources/487e07027c9b8819cf9cc3f7e22f99a1.png)
![34de6103d3ff0dc27cbbeba69e777811.png](../../_resources/34de6103d3ff0dc27cbbeba69e777811.png)
![b0cd3bf908c6d5dc9f8bbd98068dd147.png](../../_resources/b0cd3bf908c6d5dc9f8bbd98068dd147.png)
### Berechtigungen und Benutzergruppen
![5ba1eb07f53d4b3d1e8be02f210ad16a.png](../../_resources/5ba1eb07f53d4b3d1e8be02f210ad16a.png)
![ef81f98ef48da856612c940179cff947.png](../../_resources/ef81f98ef48da856612c940179cff947.png)
![709f6679414ff80f7a7fe7ef37a5decf.png](../../_resources/709f6679414ff80f7a7fe7ef37a5decf.png)
![95836bd42512befffd3eb8a9d89e2baf.png](../../_resources/95836bd42512befffd3eb8a9d89e2baf.png)
![3a8cecc10b3384aff1db8e8cb67ce3c7.png](../../_resources/3a8cecc10b3384aff1db8e8cb67ce3c7.png)

### Updates
![3d24794ab809fc5fe4faf63ef1e01187.png](../../_resources/3d24794ab809fc5fe4faf63ef1e01187.png)
![a4601dfbacc2fb49ba1d3800f7a2b415.png](../../_resources/a4601dfbacc2fb49ba1d3800f7a2b415.png)
#### Was ist busybox?
Busybox ist eine Ansammlung an tools, die Original für Linux entwickelt wurde.

<br>

### Prozesse beenden
```bash
# sofort  (SIGKILL)
sudo kill -s 9 2333

# mit aufräumarbeiten  (SIGINT)
sudo kill -s 15 2333
```

#### Reboot in 2 minuten
```
sudo shutdown -r 2

```

<br>

### Netzwerkverbindungen
#### Informationen Anzeigen
![44bd4c4f69351a9ae2bd06710a49761f.png](../../_resources/44bd4c4f69351a9ae2bd06710a49761f.png)

#### Trennen / Herstellen der verbindung
![0d472e49596d93f14f996f35b1e6c3ca.png](../../_resources/0d472e49596d93f14f996f35b1e6c3ca.png)

### Archivieren und komprimieren
![fa01e0ecb5f954115c747ff804dbb5b9.png](../../_resources/fa01e0ecb5f954115c747ff804dbb5b9.png)
![1e375c392a124cdfc88cadcc3d522c2c.png](../../_resources/1e375c392a124cdfc88cadcc3d522c2c.png)
![8142b92b7fbbd2ad74a95a92815eb008.png](../../_resources/8142b92b7fbbd2ad74a95a92815eb008.png)
![fc8a0018d2fab5905ded29c4bdbd6c33.png](../../_resources/fc8a0018d2fab5905ded29c4bdbd6c33.png)
Das Verzeichnis enthält nicht die Ursrüngliche Dateien, da diese noch in einem TAR-Archiev gespeichert sind.
