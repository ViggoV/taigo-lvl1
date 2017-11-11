# Taigo Level 1

Et træningsprojekt.

## Setup

Sæt git op og klon repositoriet (det har vi gjort).

* Husk at bruge `$ git pull` for at hente den nyeste version.
* Husk at vi kommer til at gøre de samme ting om og om igen så det er ikke så vigtigt at fange det hele med det samme ;)

## HTML

Tjek filen `index.html`. Det er roden i vores projekt og står for at definere hvad der bliver vist på skærmen i første omgang, foruden at importere vores script og vores stylesheet (mere om dem senere).

### Tags

Alt i HTML består af tags omgivet af krokodilleklammer. De lukkes for langt de fleste tags' vedkommende af et tilsvarende tag, med en skråstreg foran:

`<div></div>`

Tags kan "nestes" indeni hindanden, som så:

```html
<div>
  <h1></h1>
</div>
```

De kan også indeholde tekst:

```html
<div>
  <h1>Yo dawg!</h1>
</div>
```

Og nestes dybere:

```html
<div>
  <h1>Yo <strong>MÅÅÅHFUKKIN</strong> dawg!</h1>
</div>
```

### Grundstruktur

HTML strukturen kan visualiseres som et træ, hvor html-tagget er stammen:

```html
<html>
</html>
```
_(PS: Vi behøver ikke at bekymre om `<!DOCTYPE html>` endnu.)_

Den har to grene, `<head>` og `<body>`:

```html
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

I `<head>` putter vi meta-informationer til browseren, såsom den titel der står i browser-tabben (`<title>`) og import af scripts og styles. `<body>` er der hvor vi putter alt det ind der skal vises i browseren!

```html
<html>
  <head>
    <title>Jeg står i toppen af browseren</title>
  </head>
  <body>
    Jeg står i browser-vinduet
  </body>
</html>
```

### Resten af HTML eksemplet

Vi har lært at et html-dokument består af et `<html>` tag afsluttet med `</html>`, som indeholder et `<head>` tag og et `<body>` tag der også lukkes til hhv. meta-informationer og selve siden. Nu har vi de fornødne ting på plads så herfra er det mere eller mindre freestyle :D

#### `<head>`
Vores `<head>` tag indeholder, foruden `<title>`:

```html
<link rel="stylesheet" href="styles.css" />
<script src="script.js"></script>
```
Det første tag, `<link>`, importerer vores stylesheet (mere om det ganske snart) og det andet vores script (som vi kommer til senere).

Modsat de tidligere tags vi har set har disse her nogle _attributes_ (såsom `src="script.js"`). Andre tags kan også have attributes, men det ser vi på.

`<link>` har hhv. `rel="stylesheet"`, der fortæller browseren hvilken type dokument det linker til/importerer, og `href="styles.css"` der fortæller hvilken sti filen kan findes på. I dette tilfælde i samme mappe.

`<script>` har `src="script.js"` der svarer til `<link>`'s `href`

Bemærk at `<link>` som et af relativt få tags lukkes med en skråstreg i enden i stedet for et separat lukke-tag. Det kan ikke indeholde noget. Script kan også bruges til at skrive javascript direkte:

```html
<script>
  console.log('Uhlala.. En forsmag på javascript!');
</script>
```

#### `<body>`

Vores `<body>` tag indeholder kun ét tag: 

```html
<body>
  <h1>h1 tagget er den største indbyggede heading</h1>
</body>
```

`<h1>` tagget svarer lidt til tekstprogrammer som Word, hvor man kan vælge mellem overskrifter i forskellig størrelse. Det findes i varianter ned til (så vidt jeg husker) `<h5>`.

Hvis vi ser på `index.html` i en browser kan vi se at teksten er stor og med fed skrift. Der er dog en lille ting der er ved siden af! Bemærk at teksten står med en sans-serif font, hvor browseren normalt ville have renderet den med sin standard serif font. Det skyldes at vi har importeret et stylesheet der roder med h1 tagget!

### Forslag til leg

Rod for eksempel med de forskellige `<h1>` størrelser. Brug `<p>` tagget til brødtekst. Prøv `<strong>` for fed tekst og `<i>` for kursiv.

## CSS

**NB: Work in progress **

vi har importeret `styles.css`. CSS er et sprog til at definere hvordan HTML elementer skal se vises. Hvis vi åbner `styles.css` ser vi:

```css
h1 {
  font-family: sans-serif;
}
```