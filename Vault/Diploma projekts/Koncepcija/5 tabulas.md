___

**Datums:** 2025-09-04
**Laiks:** 20:36
❚ **Tagi:** #diploms 

---
### Kopējs idejas apraksts

Projektā tiks izmantotas 5 tabulas:

| Tabula     | Par ko atbild                           |
| ---------- | --------------------------------------- |
| Users      | Lietotāja dati                          |
| Notes      | Piezīmes                                |
| Categories | Piezīmju kategorijas                    |
| Events     | Kalendāra notikumi                      |
| Reminders  | Atgādinājumi (par kalendāra notikumiem) |

Tabulu struktūra:

| Tabula     | Struktūra                                                                                                                                                                                       |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Users      | - `id` (PK)<br>- `username`<br>- `email`<br>- `password_hash`                                                                                                                                   |
| Notes      | - `id` (PK)<br>- `user_id` (FK → Users.id)<br>- `title`<br>- `content`<br>- `date` (datums, pie kura piesaistīta piezīme)<br>- `category_id` (FK → Categories.id, var `null`)<br>- `created_at` |
| Categories | - `id` (PK)<br>- `name`<br>- `user_id` (FK → Users.id) - lai katram lietotājam būtu sava kategorija                                                                                             |
| Events     | - `id` (PK)<br>- `user_id` (FK → Users.id)<br>- `title`<br>- `description`<br>- `start_time` (datums un sākuma laiks)<br>- `end_time` (datums un beigu laiks)                                   |
| Reminders  | - `id` (PK)<br>- `event_id` (FK → Events.id)<br>- `remind_at` (laiks, līdz atgādinājumam)                                                                                                       |

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[3 CRUD funkcijas]]
Nākama lapa >>> [[Tehnoloģijas (front-end)]]

---