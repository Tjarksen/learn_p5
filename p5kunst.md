# p5js Tutorial "Moderne Kunst"  #

Wir kreieren moderne Kunst, die wie von Zaubehand vom Computer erzeugt wird.

## Schritt 1 Startschuss ##

Öffne zunächst den P5 [Online Editor](https://editor.p5js.org/)
Dort müsste bereits folgendes zu sehen sein:
```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```
## Schritt 2 Hintergrund ## 

Ändere die Hintergrundfarbe auf weiss: `background(255)`

## Schritt 3 Circle ## 


Nun lassen wir jeden Loop einen Kreis zeichnen. Füge dazu die folgende Zeile in die `draw()` Funktion ein:
```javascript
circle(width/2, height/2, 50);
```
`width/2, height/2` ist die Position des Kreises auf die exakte Mitte der Leinwand. Die `50` ist der Durchmesser des Kreises.

Dein Code müsste jetzt so aussehen:

```javascript
function setup() {
  createCanvas(400, 400);
   
}

function draw() { 
    background(255);
    circle(width/2, height/2, 50);
}
```
__Drücke auf den Playknopf!__ Es müsste ein Kreis mit schwarzem Rand erscheinen.

 ## Schritt 4 Zufall ## 

Das sieht ja noch recht langweilig aus. Doch nun wird es spannend!  

Ersetze im `cirlce()` die Positionsdaten und den Durchmesser durch `random(0, width), random(0, height), random(5,50);`.
Random bedeutet 'Zufall'. Wie der Name schon sagt, berechnet dieser Befehl eine zufällige Zahl zwischen den beiden Werten, die man angeben hat. Die `circle` Zeile sollte nun so aussehen: 
```javascript
circle(random(0,width),random(0,height), random(5,50));
```
__Drücke auf den Playknopf!__ Jetzt müsste der Kreis wie verrückt über die Leinwand hüpfen.

Aber der Code sieht etwas unübersichtlich aus, nicht war? Darum lagern die Positionsdaten im nächsten Schritt in Variablen aus. 

 ## Schritt 5 Variablen ## 

Erzeuge drei Variablen mit den Namen `PositionX, PositionY, Durchmesser` und übergebe diesen jeweils einen zufälligen Wert mit `random`. Schreibe diese Zeilen in die `draw()` Funtion. 

```javascript
let PositionX = random(0, width);
let PositionY = random(0, height);
let Durchmesser = random(5, 50);
```

Ersetze die Werte im Circle-Befehl mit den Variablen:
```javascript
circle(PositionX, PositionY, Durchmesser);
```
Viel Besser!

 ## Schritt 6 Farben ## 

Mit dem `fill()` Befehl können wir dem Kreis eine Füll-Farbe verpassen. Dazu benötigt er drei Werte für die drei Farben __rot, grün und blau__. Die Werte gehen von __0 bis 255__;
Dieser Befehl muss _über_ dem circle() Befehl stehen. Möchten wir den Kreis zum Beispiel Rot malen, muss der Befehl lauten: `fill(255,0,0);`. Für Blau `fill(0,0,255);` Für Gelb muss man Rot und Grün auf 255 setzen: `fill(255,255,0)`. 

Spiele einfach ein wenig mit den Farben rum.
```javascript
fill(123,255,50);
circle(PositionX, PositionY, Durchmesser);
```

 ## Schritt 7 Bunt ## 

Jetzt wirds bunt! Ersetze die "hart codierten" Werte von den Fill Befehl wieder in zufällige. Nutze dabei das gleiche Schema, wie mit den Positions-Daten. Erzeuge dazu drei Variablen (__R,G,B__)und befülle sie mit zufälligen Werten. 
```javascript
let R = random(0,255);
let G = random(0,255);
let B = random(0,255);
fill(R,G,B);
```
 ## Schritt 8 KUUUUUNST ## 

Verschiebe den Befehl `background(255)` in die `setup()` Funktion. Nun wird bei jedem Durchlauf der Hintergrund nicht mit weiß übermalt.
Die setup-Funktion müsste nun so aussehen:
```javascript
function setup() {
  createCanvas(400, 400);`
  background(255);
   
}
```

__Drücke auf den Playknopf!__

## Extra ##
Gratulation! Du hast mittels Computer KUUUUUNST erschaffen! Aber hier ist noch lange nich Schluss. Es gibt noch so viel zum Experimentieren. Hier gebe ich dir ein paar Tips, was du an deinem Code ändern könntest.
* Vergrößere die Leinwand mit `createCanvas(600,600);`
* verändere die Umrandungsfarbe des Kreises mit `stroke(r,g,b)` oder lasse die Randfarbe weg: `noStroke();`
* Lasse die Kreise auch Transparent werden indem du dem fill noch einen Alphawert hinzugibts: fill(R,G,B,A);
* Füge weitere Formen hinzu: `rect(), ellipse(), triangle()`
* Schaue dir die Beispiele an. Klicke dazu auf File und dann Examples oben links im Menü.
* 