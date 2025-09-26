___

**Datums:** 2025-08-09
**Laiks:** 13:42
❚ **Tagi:** #css
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Par animācijām

Animāciju īpasību tabula

| Īpašība                     | Apraksts                                                                                              |
| --------------------------- | ----------------------------------------------------------------------------------------------------- |
| `@keyframes`                | Nosaka animācijas kodu.                                                                               |
| `animation`                 | Saīsināta īpašība visu animācijas parametru iestatīšanai.                                             |
| `animation-delay`           | Nosaka aizkavi animācijas sākumam.                                                                    |
| `animation-direction`       | Nosaka, vai animācija tiks atskaņota uz priekšu, atpakaļ vai pārmaiņus ciklos.                        |
| `animation-duration`        | Nosaka, cik ilgi animācijai vajadzētu ilgt, lai pabeigtu vienu ciklu.                                 |
| `animation-fill-mode`       | Nosaka stilu elementam, kad animācija netiek atskaņota (pirms sākuma, pēc beigām vai abos gadījumos). |
| `animation-iteration-count` | Nosaka, cik reizes animācija jāatskaņo.                                                               |
| `animation-name`            | Nosaka `@keyframes` animācijas nosaukumu.                                                             |
| `animation-play-state`      | Nosaka, vai animācija darbojas vai ir pauzēta.                                                        |
| `animation-timing-function` | Nosaka animācijas ātruma līkni.                                                                       |

##### The @keyframes Rule

Animācijas kodu aprakstā `@keyframes` blokā, un tad jau pašā elementā, uz kuru tā attiecas, iestata animācijas parametrus, piem., animācijas ilgumu.

```css
 /* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
} 
```

```css
 /* The animation code */
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
} 
```

###### Nedaudz par katru no animācijas īpašībām...

###### Run Animation in Reverse Direction or Alternate Cycles

`animation-direction` nosakavai, vai animācija jāatskaņo uz priekšu, atpakaļ vai pārmaiņus ciklos:

- `normal` - Animācija tiek atskaņota kā parasti (uz priekšu). Šis ir noklusējuma iestatījums;
- `reverse` - Animācija tiek atskaņota apgrieztā virzienā (atpakaļgaitā);
- `alternate` - Animācija vispirms tiek atskaņota uz priekšu, pēc tam atpakaļ;
- `alternate-reverse` - Animācija vispirms tiek atskaņota atpakaļgaitā, pēc tam uz priekšu.

###### Specify the Speed Curve of the Animation

`animation-timing-function` īpašība norāda animācijas ātruma līkni.

- `ease` - Norāda animāciju ar lēnu sākumu, tad ātru un tad lēnām beigām (šis ir noklusējuma iestatījums);
- `linear` - Norāda animāciju ar vienādu ātrumu no sākuma līdz beigām;
- `ease-in` - Norāda animāciju ar lēnu sākumu;
- `ease-out` - Norāda animāciju ar lēnām beigām;
- `ease-in-out` - Norāda animāciju ar lēnu sākumu un beigām;
- `cubic-bezier(n,n,n,n)` - Ļauj definēt savas vērtības kubiskā bezjē funkcijā.

###### Specify the fill-mode For an Animation

`animation-fill-mode` īpašība norāda mērķa elementa stilu, kad animācija netiek atskaņota (pirms tās sākuma, pēc tās beigām vai abos gadījumos).

- `none` - Noklusējuma vērtība. Animācija nepiemēros elementam nekādus stilus pirms vai pēc tā izpildes;
- `forwards` - Elements saglabās stila vērtības, kas iestatītas pēdējā atslēgas kadrā (atkarībā no animācijas virziena un animācijas iterācijas skaita);
- `backwards` - Elements iegūs stila vērtības, kas noteiktas ar pirmo atslēgas kadru (atkarībā no animācijas virziena), un saglabās tās animācijas aizkaves periodā;
- `both` - Animācija ievēros noteikumus gan uz priekšu, gan atpakaļ, paplašinot animācijas īpašības abos virzienos.

Ieciklētas animācijas īpašību piemērs:

```css
@keyframes example {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}

div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Navigācija - HTML un CSS (2. daļa) strukturēts saturs]]

---
### ⇄ Saistības

Avots >>> [CSS Animations](https://www.w3schools.com/css/css3_animations.asp)
Iepriekšēja lapa >>> [[Pseidoklase hover]]
Nākama lapa >>> [[Navigācija - HTML un CSS]]

---