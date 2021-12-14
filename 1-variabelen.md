**Korte recap vorige les**  
Vraag de leerlingen een aantal gerichte vragen en/of laat ze een klein element programmeren.
Bijv. maak een rode vierkant in het midden van het scherm.

---
# Variabelen

Deze les gaan we gebruik maken van variabelen (variables (ENG)).
We kunnen een waarde ergens anders declareren/beschrijven en gebruiken op verschillende plekken.

## Start programma samen maken:

```javaScript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(200,100,50);
  ellipse(200,200,50);
  ellipse(200,300,50);  
}
```

? Wat als we alle 3 de rondjes in grootte willen veranderen?  
Dan kunnen we een variabele maken.   
Deze kan globaal, bovenaan gezet worden, of lokaal in de draw functie.

```javaScript
let afmetingRondjes = 50;
```

Een variabele kan je van alles noemen, behalve die al gebruikt worden in de library zelf. Goed om te zetten wat het is, zodat je sneller snapt waar je de variabele voor kan gebruiken.

```javaScript
let afmetingRondjes = 25;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(200,100,afmetingRondjes);
  ellipse(200,200,50);
  ellipse(200,300,50);

}
```

- [ ]  voeg toe aan 1 ellipse  
- [ ]  verander de waarde van de variabel
- [ ]  voeg ook toe aan de anderen ellipses.

```javaScript
var afmetingRondjes = 100;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(200,100,afmetingRondjes);
  ellipse(200,200,afmetingRondjes);
  ellipse(200,300,afmetingRondjes);

}
```
---
## in het midden

Wanneer we `createCanvas()` doen, maken we een canvas aan van een x breedte en een x hoogte. Deze waardes worden gelijk in variabelen opgeslagen die al zijn gedefineerd door het programma. Voor de breedte `width` en voor de hoogte `height`.

- [ ] voeg `width` toe als x positie
- [ ] de helft van de breedte door `width/2`

```javaScript
ellipse(width,100,afmetingRondjes);
ellipse(width,200,afmetingRondjes);
ellipse(width,300,afmetingRondjes);

```

- [ ] verander de breedte in `createCanvas()`, je ziet dat de cirkels in het midden blijven staan.


```javaScript
 createCanvas(500, 400);
```

---

## nog meer cirkels

Voor het maken van nog meer cirkels kunnen we nog meer cirkels kopiëren en plakken, en dan een waarde aanpassen.
Er is ook een andere mogelijkheid genaamd een **for loop**

Kijk eventueel naar de voorbeelden:  
[Example: Iteration](https://p5js.org/examples/control-iteration.html)


Een **for loop** wilt 3 statements hebben.
- 1: start input
- 2: eind input
- 3: iteratie grootte


- [ ] neem stapsgewijs over in `draw()`   

een `for loop` beginnen we met `for` functie, die geven we 3x informatie. Tussen twee `{ }` / accolades. Accolades geven aan wat bij elkaar hoort. De accolades geven de begrenzing van een blok aan.


```javaScript

for ( 1 ; 2 ; 3 ){

}

```

Als eerste geven we de start input. Daarin declareren we een variabele die we willen gebruiken.  Bijvoorbeeld `posY`, voor de positie van de y-as. Deze geven we als start waarde `0`.

```javaScript

for ( let posY = 0 ; 2 ; 3 ){

}

```


Als volgende waarde, de eind waarde. Als voorbeeld `posY < 200`, zolang `posY` kleiner blijft dan `200` blijven we de for loop door laten gaan.

```javaScript

for ( let posY = 0 ; posY < 200 ; 3 ){

}

```
als laatste geven we aan hoe groot we de stappen willen hebben. Als voorbeeld doen we `posY+= 25`, we zeggen hiermee, tel bij `posY` steeds `25` erbij.

```javaScript

for ( let posY = 0 ; posY < 200 ; posY+= 25 ){

}

```

Als volgende willen we die variabele `posY` gaan gebruiken. We maken wat meer cirkels.

```javaScript

for ( let posY = 0 ; posY < 200 ; posY+= 25 ){
    circle(100,posY,20);
}
```

- [ ] laat de leerlingen verder spelen met deze functie doormiddel van waardes te veranderen.

---
**Aantal vragen en opdrachten:**  
*welke variabele kunnen we gebruiken om tot helemaal onderaan te gaan?*  
*maak de stappen groter*  
*gebruik de `posY` ook voor het formaat van de cirkel*  
