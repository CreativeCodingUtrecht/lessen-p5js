**Korte recap vorige les**  
Vraag de leerlingen een aantal gerichte vragen en/of laat ze een klein element programmeren.


# Eigen functie schrijven

In de library(bibliotheek) van p5.js staan allemaal functies die je kan gebruiken. Zoals `rect`, `ellipse` enz..
Zelf kan je ook je eigen functies schrijven.


## Start programma samen maken:

```javaScript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

}
```

- [ ] Voeg een functie toe onderaan het programma. Dit kan je zelf een naam geven

```javaScript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}

function poppetje(){

}
```

- [ ] begin met een ellipse te maken in de functie

```javaScript
function poppetje(){
  ellipse(100,100,50,50);
}
```
Wanneer je de functie hebt gemaakt zal deze niet gelijk te zien zijn. Je moet in `draw()` nog de functie oproepen: `poppetje();`.

```javaScript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  poppetje();
}

function poppetje(){
  ellipse(100,100,50,50);
}
```

Bij o.a. `rect()` en `ellipse` functies zie je dat er een aantal parameters worden gevraagd om iets te tekenen. Om meerdere poppetjes op verschillende plekken te tekenen gaan we ook dat zelf toevoegen aan ons `poppetje()`

We beginnen met de positie.


```javaScript
function poppetje(_x, _y){
  ellipse(_x,_y,50,50);
}
```

De `_x` en `_y` parameters schrijf ik zo met een onderstreepje ervoor om iets makkelijker te zien dat het een parameter variabele is.
De variabels gebruik ik dan in de `ellipse()`.

in `draw()` geef ik nu de informatie van de positie toe

```javaScript
function draw() {
  background(220);

  poppetje(100,100);
}
```

en kunnen we ook meerdere poppetjes doen:
```javaScript
function draw() {
  background(220);

  poppetje(100,100);
  poppetje(150,200);
}

```

**opdracht:**
Laat de leerlingen voor de grootte van de cirkel een parameter maken en deze gebruiken.


---

### Push - translate - pop
Of het tekenen voor ons iets makkelijker te maken, gebruiken we de functie `translate()`  
Reference: [p5js.org / reference / translate](https://p5js.org/reference/#/p5/translate)

```javaScript
function poppetje(_x, _y, _sz){
  push();
  translate(_x,_y);
    ellipse(0,0,_sz,_sz);
  pop();
}
```

### opdracht
Teken het poppetje verder. Geef bijv. ogen en een mond.



---
**Extra**
Mooi voorbeeld van een functie die op verschillende manieren gebruikt kan worden.

[p5js.org / examples / Star](https://p5js.org/examples/form-star.html)

---
### referenties
[p5js.org / reference / translate](https://p5js.org/reference/#/p5/translate)
[p5js.org / reference / push](https://p5js.org/reference/#/p5/push)
