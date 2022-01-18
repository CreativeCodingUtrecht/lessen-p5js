**Korte recap vorige les**  
Vraag de leerlingen een aantal gerichte vragen en/of laat ze een klein element programmeren.


# Beweging



## Start programma samen maken:

```javaScript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(0,100,20);
}
```

- [ ] Voeg een variabele toe voor de x positie van de cirkel.

```javaScript
let xPos = 0;
```

- [ ] Gebruik de variabele voor de x positie.  

```javaScript
let xPos = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(xPos,100,20);
}
```

Omdat de `draw()` functie continu wordt uitgevoerd kunnen we elke keer iets toevoegen.

- [ ] voeg `  xPos = xPos + 1;` toe

```javaScript
let xPos = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(xPos,100,20);

  xPos = xPos + 1;
}
```

*vraag: wat gebeurt er?*
*vraag: hoe kunnen we deze stoppen?*


---
## if statement: als dit zoveel is, doe dit

- [ ] voeg if statement toe

```javaScript
let xPos = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(xPos,100,20);

  xPos = xPos + 1;

  if (xPos === width){
      xPos = 0;
  }
}
```

### verschil `=` en `===`

`=` wijst iets toe aan een variabele   
`===` vergelijkt de waardes met elkaar, geeft true of false terug



---
## Heen en weer

Een goed moment om samen met de leerlingen te onderzoeken hoe we het voor elkaar kunnen krijgen om de cirkel heen en weer te laten gaan.


Een eerste idee is vaak als `xPos === width` dan inplaats van `+` juist `-` gebruiken.

```javaScript
xPos = xPos - 1;
```

Dit werkt helaas niet. de `xPos` is maar 1 frame zelfde aan `width` en daarna zal deze niet meer luisteren naar wat er in het if statement staat.


*vraag: wat willen we veranderen?*  
antwoord: de richting.








---
**opdracht**




---
### referenties

Voorbeeld:   
[p5js.org / examples / Linear](https://p5js.org/examples/motion-linear.html)
