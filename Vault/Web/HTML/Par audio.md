___

**Datums:** 2025-08-07
**Laiks:** 20:41
❚ **Tagi:** #html 
⌬ **Priekšmets:**  `HTML`

---
### ⬢ Detalizēts apraksts
#### `<audio>` tags

Šis tags tiek izmantots, lai izvietotu audio failus uz tīmekļa lapas.

```html
 <audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  Your browser does not support the audio tag.
</audio> 
```

Tam ir tādi atribūti:

| Atribūts   | Vērtība                    | Apraksts                                                                             |
| ---------- | -------------------------- | ------------------------------------------------------------------------------------ |
| `autoplay` | `autoplay`                 | Norāda, ka audio sāks atskaņot uzreiz pēc tam, kad tas būs gatavs                    |
| `controls` | `controls`                 | Norāda, ka jāparāda audio vadības elementi (piemēram, atskaņošanas/pauzes poga u.c.) |
| `loop`     | `loop`                     | Norāda, ka audio sāks atskaņoties no sākuma katru reizi, kad tas beidzas             |
| `muted`    | `muted`                    | Norāda, ka audio jāatskaņo bez skaņas (izslēgts)                                     |
| `preload`  | `auto`, `metadata`, `none` | Norāda, vai un kā autors domā, ka audio būtu jāielādē lapas ielādes laikā            |
| `src`      | URL                        | Norāda audio faila URL adresi                                                        |

  Principā tādi paši atribūti ir arī tagam `<video>`, kas tiek izmantots video attēlošanai.

---
### ⇄ Saistības

Avots >>> [HTML audio tag](https://www.w3schools.com/tags/tag_audio.asp)
Iepriekšēja lapa >>> [[Par time]]
Nākama lapa >>> [[Navigācija - HTML]]

---