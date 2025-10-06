___

**Datums:** 2025-10-05
**Laiks:** 18:28
❚ **Tagi:** #kotlin 

---
# Button

Šādi veido pogas priekš Android, tas pieņem `lambda` funkcijas:

```kotlin
Button(onClick = {

                /* Logika, kas atbilst par ekrānu maiņu
                *
                * Pirmajā ekrānā uzģenerē randomTap skaitu,
                * cik reižu būs nepieciešams nospiest uz citronu,
                * lai pāriet uz nākamo ekrānu.
                *
                * Kad userTap sasniedz nepieciešamo skaitu,
                * lietotājs tiek pārvirzīts uz nākamo ekrānu.
                **/

                when (screenNumber) {
                    0 -> {
                        screenNumber = 1
                        randomTap = (2..4).random()
                        userTap = 0
                    }
                    1 -> {
                        userTap++

                        if (userTap == randomTap) {
                            screenNumber = 2
                        }
                    }
                    2 -> {
                        screenNumber = 3
                    }
                    else -> {
                        screenNumber = 0
                    }
                }},
                modifier = Modifier
                    .size(260.dp)
                    .clip(RoundedCornerShape(16.dp))
                    .background(Color(0xFF90EE90)),

                /* Maina pogas stilu:
                * - krāsu
                **/

                colors = ButtonDefaults.buttonColors(
                    containerColor = Color(0xFF90EE90)
                )
            )
```

Šādi var veikt pašas pogas konteinera modifikācijas:

```kotlin
modifier = Modifier
                    .size(260.dp)
                    .clip(RoundedCornerShape(16.dp))
                    .background(Color(0xFF90EE90)),
```

Taču krāsas maiņa esot gana specifiska:

```kotlin
colors = ButtonDefaults.buttonColors(
                    containerColor = Color(0xFF90EE90)
                )
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Globālie mainīgie]]
Nākama lapa >>> [[Spacer]]

---