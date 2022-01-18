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

- [ ] maak een variabele boven aan `int richting = 1`
- [ ] gebruik `richting` om bij `xPos` op te tellen


```javaScript
let xPos = 0;
let richting = 1;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(xPos,100,20);

  xPos = xPos + richting;

  if (xPos === width){
      xPos = 0;
  }
}
```


- [ ] verander wat er in de statement moet gebeuren

```javaScript
if (xPos === width){
      richting = -1;
  }
 ```

*vraag: Werkt het? Wat moeten we nu doen om ook weer de andere kant op te gaan*

```javaScript
if (xPos === 0){
    richting = 1;
}
```

Eind programma:


```javaScript
let xPos = 0;
let richting = 1;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  ellipse(xPos,100,20);

  xPos = xPos + richting;

  if (xPos === width){
      richting = -1;
  }

  if (xPos === 0){
      richting = 1;
  }
}
```


---
**Extra**

Bij het volgende voorbeeld komt er meer beweging en variabelen aan pas.   
Ook is de if statement anders geschreven, kan je erachter komen wat er gebeurd en hoe het werkt?   

[p5js.org / examples / Bounce](https://p5js.org/examples/motion-bounce.html)


---
### referenties

Voorbeeld:   
[p5js.org / examples / Linear](https://p5js.org/examples/motion-linear.html)
[p5js.org / examples / Bounce](https://p5js.org/examples/motion-bounce.html)
