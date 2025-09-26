___

**Datums:** 2025-08-10
**Laiks:** 15:51
❚ **Tagi:** #css #html 
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Tabulas

Tabulas tiek izmantotas, lai prezentēt kādus datus.

Tabulām izmanto šādus tagus:

- `<table>` - pati tabula, kas satur apakštagus;
- `<caption>` - tabulas nosaukums;
- `<thead>` - tabulas galvene;
- `<th>` - tabulas galvenes šūnas;
- `<tbody>` - tabulas ķermenis;
- `<tr>` - tabulas rinda;
- `<td>` - tabulas šūna;
- `<tfoot>` - tabulas kājene;

Papildus, pie `<td>` var pievienot atribūtus:

- `colspan='2'` - šeit šūna aizņems pa horizontāli 2 šūnas;
- `rowspan='2'` - šeit šūna aizņems pa vertikāli divas rindas.

```html
<table>
	<caption> Tabulas nosaukums </caption>
	<thead>
		<th>Galvenes 1. šūna</th>
		<th>Galvenes 2. šūna</th>
		<th>Galvenes 3. šūna</th>
	</thead>
	<tbody>
		<tr>
			<td>Ieraksts 1</td>
			<td>Ieraksts 2</td>
			<td>Ieraksts 3</td>
		</tr>
	</tbody>
	<tfooter>
		<tr>
			<td colspan='3'>3 šūnas pa horizontālei.</td>
		</tr>
	</tfooter>
</table>
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Relatīvie ceļi]]
Nākama lapa >>> [[Web/HTML un CSS/Pozicionēšana]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Grupas selektors]]
Nākama lapa >>> [[Navigācija - HTML un CSS]]

---