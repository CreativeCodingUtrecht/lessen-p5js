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
**Opdracht:**  
Maak een variabele voor de x positie van de ellipse.
