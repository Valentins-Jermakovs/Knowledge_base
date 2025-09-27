___

**Datums:** 2025-09-27
**Laiks:** 18:34
❚ **Tagi:** #kotlin 

---
# Teksta noformēšana

**Jetpack Compose teksta parametri**

| Parametrs        | Paskaidrojums                                                         |
| ---------------- | --------------------------------------------------------------------- |
| `fontSize`       | Teksta izmērs (`sp` – scale-independent pixels)                       |
| `fontWeight`     | Teksta biezums (`Thin`, `Normal`, `Medium`, `Bold`, `Black`)          |
| `fontStyle`      | Stils – parasts (`Normal`) vai kursīvs (`Italic`)                     |
| `fontFamily`     | Šrifta ģimene (`Serif`, `SansSerif`, `Monospace` vai pielāgots fonts) |
| `color`          | Teksta krāsa (`Color.Red`, `Color(0xFF123456)`)                       |
| `letterSpacing`  | Atstatums starp burtiem                                               |
| `lineHeight`     | Rindas augstums (interline spacing)                                   |
| `textAlign`      | Teksta līdzinājums (`Left`, `Right`, `Center`, `Justify`)             |
| `textDecoration` | Teksta dekorācija (piem., `Underline`, `LineThrough`)                 |
| `shadow`         | Ēna aiz teksta (krāsa, novietojums, izplūdums)                        |
| `background`     | Fons aiz teksta                                                       |
| `drawStyle`      | Teksta uzzīmēšanas stils (`Fill`, `Stroke`, `FillAndStroke`)          |
| `lineBreak`      | Rindas laušanas noteikumi (`Simple`, `Word`, `Paragraph`)             |
| `textMotion`     | Teksta kustība pie izmaiņām (`Static`, `Animated`)                    |

**Koda piemērs ar parametriem priekš `Text(...)` komponentēm**

```kotlin
Text(
    text = "Sveiki, pasaule!",
    fontSize = 20.sp,
    fontWeight = FontWeight.Bold,
    fontStyle = FontStyle.Italic,
    fontFamily = FontFamily.Serif,
    color = Color.Red,
    letterSpacing = 2.sp,
    lineHeight = 24.sp,
    textAlign = TextAlign.Center,
    textDecoration = TextDecoration.Underline,
    shadow = Shadow(
        color = Color.Black,
        offset = Offset(2f, 2f),
        blurRadius = 4f
    ),
    background = Color.Yellow,
    drawStyle = Fill,
    lineBreak = LineBreak.Paragraph,
    textMotion = TextMotion.Animated
)
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Komponenšu noformēšana]]
Nākama lapa >>> [[Attēla noformēšana]]

---