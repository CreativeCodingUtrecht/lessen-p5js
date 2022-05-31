# Animatie met p5js

Les: ca 1.5 uur  
beginners zonder ervaring  

---
# p5js introductie NL animatie

+ Stel jezelf voor
+ Vertel over CCU
+ Wat gaan we doen: Een animatie maken door code te schrijven
+ Wat is Creative Coding  
Q: vraag of de deelnemers een idee hebben of ervaring  
A: Kunstzinnige uitingen maken met het gebruik van technologie, o.a. schrijven van code.  

### wat is P5.js  

P5js is vanuit Processing ontstaan, Processing is ontwikkeld vanaf 2001 door Casey Reas & Ben Fry in het MIT Media LAB. Ze wilde een tool maken waarmee je op kunst kan maken door middel van code en daarbij jezelf uitdrukken.  

Processing is een bibliotheek ontwikkel op Java   
p5js is gemaakt voor JavaScript, voor de web.

---
## p5js.org

[https://p5js.org](https://p5js.org)  
Website waar je veel kan vinden, zoals referentie, voorbeelden en meer.


[https://p5js.org/reference/](https://p5js.org/reference/)  
De referentie van alle functies die je kan gebruiken is handig om erbij te hebben tijdens het uitleggen.

---


## Editor
Ga naar [editor.p5js.org](http://editor.p5js.org/)

Laat zien hoe de editor werkt, waar je wat vind.
- *Code editor* en de preview
- save en open (je kan alleen je voorbeeld bewaren als je account hebt en bent ingelogged.)
- examples: in het menu onder *file*
- comment: schrijf je door `//` voor een regel te gebruiken
- error veld onderaan in de *console*
- sidebar met *html.index / sketch.js / ...* files


---
## start
Wat er al staat:

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```


## createCanvas

- 500 x 500
- background(55);
- [ ] zoek op background in de reference

## vormen

- [ ] zoek op `ellipse` in de reference
- ellipse
- center - width + height

## rect
Zoek op `rect` in de reference
- Veel opties
- afgeronde hoeken
- `rectMode()` functie  voor de 0,0 positie  center

## variable de grote
Maak een variable voor de grote  

`let sz = 50;`

## Kleur

- `fill()`
- `stroke()`
- `strokeWeight()`

## Meerdere vormen op 1 lijn

```javaScript
function setup() {
  createCanvas(400, 400);
  rectMode(CENTER);
}

function draw() {
  background(220);

  fill(100,20,150)

  rect(100,200,50,50);
  rect(200,200,50,50);
  rect(300,200,50,50);
}

```

Q: Wat als we er 100 willen?  
A: daar voor hebben we for loop functie  

```javaScript
// (start, eind, toeneming);
for (var x = 0; x <= 200; x += 25){
    rect(x,200,50,50);

}

```
- [ ] gebruik de x ook voor de `width` en `height` van de `rect()`
- [ ] of voor de `fill()`  


---

# het laten bewegen

Begin samen met het onderzoeken wat je in dit voorbeeld ziet en hoe de code werkt.  
[https://p5js.org/examples/math-sine.html](https://p5js.org/examples/math-sine.html)


- [ ] start met het toevoegen
- `let diameter` en `angle = 0;`
- geef de `diameter` ook een start waarde
- kopieer een van `d1 d2 d3`
- gebruik die variabel in de vorm zoals `rect(x,200,d1,50)`
- vergeet niet `angle += 0.02` buiten de for loop
- voeg een variabel toe: `let = offSet`
- gebruik deze in de `sin()` zoals `(sin(angle + offset) * diameter);`
- speel en ontdek verder



```javascript
// variables
var diameter = 100;
var angle = 0;

function setup() {
  createCanvas(500, 500);
  noFill();
}

function draw() {
  background(240);

  // for loop = (start;eind;iteratie)
  for (var x = 100; x < 400; x += 5) {

    var offset = x / 2; // speel met de nummers om aan te passen
    var d1 = (sin(angle + offset) * diameter); // sin functie voor de animatie

    // ellipse(x positie, y positie, width, height)  
    ellipse(x, (height / 2) + d1, d1, d1);
    angle += 0.0002; // snelheid animatie

    //print(d1); // print informatie naar de console
  }

}
```
[final in de p5js editor](https://editor.p5js.org/sasj/sketches/PCeRuDats)


- [ ] laat de leerlingen verder spelen met deze functie doormiddel van waardes te veranderen.

---
**Aantal vragen en opdrachten:**  
*maak de stappen groter*  
*gebruik de `x` ook voor iets anders*  
*maak meerdere variabels met animerende functies en gebruik ze voor een ander element*  
