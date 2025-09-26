___

**Datums:** 2025-09-21
**Laiks:** 11:13
❚ **Tagi:** #kotlin 

---
### Example of a composable function

**Kas ir Composable funkcija:**

- Tā ir funkcija, kas apzīmēta ar `@Composable` anotāciju.
- Šī anotācija pasaka Compose kompilatoram, ka funkcija paredzēta, lai pārvērstu datus par UI elementiem.

```kotlin
@Composable
fun Greeting(name: String) {
    Text(text = "Hello $name!")
}
```

*Šeit funkcija pieņem argumentu (`name`) un izmanto to, lai izvadītu tekstu.*

**Piezīmes par Composable funkcijām**

- UI tiek aprakstīts programmatiski, nevis konstruēts grafiski.
- Funkcijas var pieņemt argumentus, lai mainītu UI saturu (piemēram, lietotāja vārdu).

**Preview funkcija:**

```kotlin
@Preview(showBackground = true)
@Composable
fun BirthdayCardPreview() {
    HappyBirthdayTheme {
        Greeting("Android")
    }
}
```

**Svarīgi par Preview**:

- `@Preview` anotācija ļauj redzēt, kā UI izskatīsies, nepalaižot aplikāciju.
- `Preview` funkcijas parasti tiek nosauktas pēc to satura (`GreetingPreview`, `BirthdayCardPreview` u.tml.).
- `Preview` funkcija var izsaukt citas `Composable `funkcijas (piem., `Greeting`).

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Anotācijas ar parametriem]]
Nākama lapa >>> [[Teksta atribūti (izmēra maiņa, rindu augstums)]]

---