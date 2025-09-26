___

**Datums:** 2025-09-13
**Laiks:** 20:11
❚ **Tagi:** #java #OOP 

---
### packages

`packages` ļauj strukturēt programmu, tas ir kā `namespace` `C#` valodā, kas ļauj nodalīt klases vienu no otras.

Lai izveidot `package`, projekta `src` direktorija -> `New` -> `Package`.

Kad tu tajā `package` veido jauno klasi, tās sākumā obligāti raksti šādu rindu:

```java
package packageName;
```

Pēc tam, kad vajadzēs pielietot kādas `package` klases `main` blokā vai kādā citā klasē, kods izskatīsies apmēram šādi:

```java
import samples.Vehicle;

class MyClass {
  public static void main(String[ ] args) {
    Vehicle v1 = new Vehicle();
    v1.horn();
  }
}
```

Šajā gadījumā `import.sapmles.Vehicle` norāda, kā no `package` ar nosaukumu `samples` tiek importēta klase `Vehicle`.

Ja vēlies importēt visas klases, kas atrodas tajā `package`, tad šajā piemērā būtu `import samples`.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[packages]]
Nākama lapa >>> [[Navigācija - Modulis 1]]

---