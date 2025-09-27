___

**Datums:** 2025-09-20
**Laiks:** 16:32
❚ **Tagi:** #kotlin 

---
### onCreate() funkcija

Funkcija `onCreate()` ir ieejas punkts Android lietotnēs un izsauc citas funkcijas, lai izveidotu lietotāja saskarni. Kotlin programmās funkcija `main()` ir ieejas punkts/izpildes sākumpunkts. Android lietotnēs šo lomu pilda funkcija `onCreate()`.

```kotlin
class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            GreetingCardTheme {
                // A surface container using the 'background' color from the theme
                Surface(
                    modifier = Modifier.fillMaxSize(),
                    color = MaterialTheme.colorScheme.background
                ) {
                    Greeting("Android")
                }
            }
        }
    }
}

```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Pirmā android programma]]
Nākama lapa >>> [[setContent() funkcija]]

---