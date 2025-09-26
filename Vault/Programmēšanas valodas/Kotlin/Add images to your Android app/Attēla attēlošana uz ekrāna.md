___

**Datums:** 2025-09-21
**Laiks:** 18:40
❚ **Tagi:** #kotlin 

---
# Attēla attēlošana uz ekrāna

![[7f95dd836a249cdc_1440.png]]

Pirmām kārtām, piekļūšana pie resursiem no tiek caur speciāli tam paredzētu `R` klasi:

```kotlin
R.drawable.androidparty
```

Un tad jau pašā funkcijā, kas tiks izmantota priekš attēla rendera, izveido šādu te mainīgo:

```kotlin
val image = painterResource(R.drawable.tava_faila_nosaukums)
```

Izveidoo `Image` elementu un nodod tam attēlu:

```kotlin
Image(
    painter = image,
    contentDescription = null
)
```

`contentDescription = null` nozīmē, ka TalkBack (balss lasītājs) ignorēs šo attēlu, jo tas ir tikai dekoratīvs.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Attēla faila pievienošana projektam]]
Nākama lapa >>> [[Box izmantošana]]

---