___

**Datums:** 2025-09-20
**Laiks:** 16:39
❚ **Tagi:** #šabloni

---
### `@Preview` anotācija

Funkcija `GreetingPreview()` ļauj redzēt, kā izskatās jūsu saliekamais fails, neveidojot visu lietotni. 

Lai iespējotu saliekamā faila priekšskatījumu, anotējiet to ar `@Composable` un `@Preview`. `@Preview` anotācija norāda *Android Studio*, ka šim saliekamajam failam ir jābūt **redzamam** šī faila **dizaina skatā**. Kā redzat, `@Preview` anotācija pieņem parametru ar nosaukumu `showBackground`. 

Ja showBackground ir iestatīts uz `true`, tas pievienos fonu jūsu saliekamā faila priekšskatījumam.

```kotlin
@Preview(showBackground = true)
@Composable
fun GreetingPreview() {
    GreetingCardTheme {
        Greeting("Meghan")
    }
}

```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[setContent() funkcija]]
Nākama lapa >>> [[Navigācija - Pirmā android programma]]

---