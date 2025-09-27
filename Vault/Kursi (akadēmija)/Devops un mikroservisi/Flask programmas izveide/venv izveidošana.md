___

**Datums:** 2025-09-27
**Laiks:** 15:28
❚ **Tagi:** #devops #linux

---
# venv izveidošana

`venv` tā ir virtuāla vide, kas ļauj izmantot `pip` menedžeru, lai instalēt `python` paķetes, bibliotēkas priekš projekta. Daudzos linux distributīvos tā esot iebūvēta, tev tikai atliek to izveidot pašā projektā:

```bash
python3 -m venv venv
```

Šeit pēdējais parametrs ir ceļš līdz `venv`, ja tu atkārtoti to ieadi, tiks izveidota `venv` mape, kas satur visus nepieciešamus failus priekš virtuālas vides.

Lai aktivizēt virtuālo vidi, izmanto šādu komandu:

```bash
source venv/bin/activate
```

Lai to izslēgt:

```bash
deactivate
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Flask]]
Nākama lapa >>> [[Projekta izveide (bibliotēku instalācija)]]

---