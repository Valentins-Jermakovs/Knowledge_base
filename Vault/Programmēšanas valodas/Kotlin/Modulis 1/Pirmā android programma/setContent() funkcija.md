___

**Datums:** 2025-09-20
**Laiks:** 16:35
❚ **Tagi:** #kotlin 

---
### setContent() funkcija

Funkcija `setContent()` funkcijā `onCreate()` tiek izmantota, lai definētu izkārtojumu, izmantojot saliekamās funkcijas. 

Visas funkcijas, kas atzīmētas ar anotāciju `@Composable`, var izsaukt no funkcijas `setContent()` vai no citām saliekamajām funkcijām. 

Anotācija `@Composable` norāda Kotlin kompilatoram, ka Jetpack Compose šo funkciju izmanto lietotāja saskarnes ģenerēšanai.

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


Iepriekšēja lapa >>> [[onCreate() funkcija]]
Nākama lapa >>> [[Preview]]

---