# Start: basics

# Introductie

- Introduceer jezelf
- Introduceer CCU [https://creativecodingutrecht.nl/](https://creativecodingutrecht.nl/)
- Introduceer p5.js. JavaScript. Code voor het web. Interactief. animaties.
Processing Foundation, sinds 2001.
- Open Source software, wat betekend dat?


- Wat gaan we doen?
(Als er een thema, een expositie, of een fysiek element aanwezig is bij de workshop (reeks) kan je dit ook behandelen)

---
# Creativiteit & Code

Aantal voorbeelden laten zien, van jezelf of andere kunstenaars.

- Saskia Freeke [https://sasj.tumblr.com](https://sasj.tumblr.com/) | maakt elke dag een kunstwerk met code
- Carolien Teunissen [https://vimeo.com/carolien](https://vimeo.com/carolien)
- ...

Als je gaat programmeren zal je vooral veel moeten opzoeken hoe je een onderdeel kan maken. Je hoeft het niet uit je hoofd te weten, je moet vooral snappen waar je het antwoord kan vinden en hoe code kan structureren.

De code hoeft ook niet heel moeilijk of ingewikkeld te zijn. Het gaat erom hoe je code gebruikt als een artistiek gereedschap.

**Tips aan de studenten:**  
Maak aantekeningen in een schrift, handig om iets uit te tekenen voordat je het gaat coderen. Kijk naar de referentie op de website.

---
# Editor

- [ ] Laat iedereen de editor openen: editor.p5js.org
Account aanmaken is handig zodat je je werk kan opslaan. Geheel gratis.

- [ ] Leg globaal uit wat en hoe de editor in elkaar zit
    - editor / preview
    - save / open
    - examples (voorbeelden)
    - Comments in de editor schrijven
    - errors - hoe worden die aangegeven
    - sidebar openen en structuur van de benodigde bestanden laten zien
    html.index / sketch.js / ...


# Reference & voorbeelden

Altijd open hebben:

- [https://p5js.org/reference/](https://p5js.org/reference/)
- p5js voorbeelden
Laat iedereen even zelf rondkijken bij de voorbeelden voor een aantal minuten.
Laat een aantal zelf uitleggen wat ze zien bij een voorbeeld.

# Start

Wanneer je [editor.p5js.org](http://editor.p5js.org) opent zie je een basis structuur van een programma.

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

*Vraag: Wat doet setup?*  
*Vraag: Wat doet draw?*  
*Vraag: CreateCanvas?*  
*Vraag: en background?*   

`setup()` zal 1x worden uitgevoerd, terwijl `draw()` continu uitgevoerd wordt. Van onder naar boven.

`createCanvas` maakt de canvas waarin we kunnen tekenen. Kijk wat er gebeurt als de de cijfers verandert.   

Gebruik de reference om erachter te komen wat we allemaal met `background()` kunnen doen.

Referentie:  
[https://p5js.org/reference/#/p5/setup](https://p5js.org/reference/#/p5/setup)   
[https://p5js.org/reference/#/p5/draw](https://p5js.org/reference/#/p5/draw)  
[https://p5js.org/reference/#/p5/createCanvas](https://p5js.org/reference/#/p5/createCanvas)  
[https://p5js.org/reference/#/p5/background](https://p5js.org/reference/#/p5/background)

**Opdracht:**   
Gebruik de background referentie om de achtergrond kleur aan te passen.

Je kan verder vertellen hoe de verschillende waardes iets doen. 1 waarde is grijstinten. 3 waardes RGB kleuren. Deze gaan van 0-255. Wat staat aangegeven in de beschrijving.

---
## `createCanvas()`

- [ ] maak canvas: `500 x 500`  
- [ ] `background(255);` een kleur naar keuze

---
## Rondje / cirkel

We gaan een rondje tekenen, daarvoor kunnen we kiezen tussen twee functies: `ellipse()` of `circle()`

- [ ] Ga naar reference en naar de vorm ellipse  
[https://p5js.org/reference/#/p5/ellipse](https://p5js.org/reference/#/p5/ellipse)   
- [ ] Leg uit wat de voorbeelden laten zien, wat de syntax is en argumenten doen.

**Goed om te weten:**  
Het coördinatie systeem begint hier links bovenin met de waarde 0,0.

Eventueel uitleggen met learn pagina [https://p5js.org/learn/coordinate-system-and-shapes.html](https://p5js.org/learn/coordinate-system-and-shapes.html)

zorg dat iedereen een rondje op zijn scherm heeft.

---
## Vierkant - `rect()`
- [ ] Ga naar reference van `rect()`  
[https://p5js.org/reference/#/p5/rect](https://p5js.org/reference/#/p5/rect)

- voorbeeld 1 legt uit waar de lokatie is en hoe groot het vierkant is  
- ronde hoeken zijn mogelijk met een extra argument.

*wat is het verschil met `ellipse()`?*  
Bij `ellipse()` is de `0,0` positie in het midden, bij `rect()` is dat standaard (default) links bovenin.

Dit kunnen we aanpassen door de functie `rectMode()` te gebruiken.  
[https://p5js.org/reference/#/p5/rectMode](https://p5js.org/reference/#/p5/rectMode)

- [ ] gebruik `rectMode()` in de `setup()`

```javaScript
function setup() {
  createCanvas(400, 400);
  rectMode(CENTER);
}

function draw() {
  background(220);

  ellipse(200,100,50,50);
  rect(200,200,50,50);
}
```


---
## Kleur

Kijk naar de volgende functies in de reference, bespreek met ze wat deze doen.

- `fill()` [https://p5js.org/reference/#/p5/fill](https://p5js.org/reference/#/p5/fill)
- `stroke()` [https://p5js.org/reference/#/p5/stroke](https://p5js.org/reference/#/p5/stroke)
- `strokeWeight()` [https://p5js.org/reference/#/p5/strokeWeight](https://p5js.org/reference/#/p5/strokeWeight)


- [ ] Maak een voorbeeld zodat je kan zien hoe de kleuren werken:
- altijd de kleur boven de vorm zetten die je wilt kleuren
- als je 1 kleur toevoegt, worden de anderen ook die kleur

```javaScript
function setup() {
  createCanvas(400, 400);
  rectMode(CENTER);
}

function draw() {
  background(220);

  fill(200,20,50);
  ellipse(200,100,50,50);

  fill(100,20,150)
  strokeWeight(20);
  stroke(255);
  rect(200,200,50,50);
}

```

---
### Opdracht:  
Laat de leerlingen iets tekenen zoals een figuur, huis of verschillende vormen bij elkaar.
