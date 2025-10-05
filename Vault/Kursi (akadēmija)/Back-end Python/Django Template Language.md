___

**Datums:** 2025-10-05
**Laiks:** 14:39
❚ **Tagi:** #back-end #python 

---
# Django Template Language

`Django` pastāv 3 noderīgas lietas, ko var izmantot šablonos:

- `{{ variable }}` - mainīgie, ko var attēlot šablonos;
- `{%  %}` un `{% end %}` - dažādi noderīgie tagi;
- `{{ variable | filter}}` - filtri.

## Cikls `for`

`{% for %}` - šīs tags ļauj apstrādāt vairākus objektus, sarakstu, vārdnīcas. Tā beigās obligāti jāizvieto `{% endfor %}`. Papildums var pieminēt par tagu `{% empty %}`, kas attēlo `html` elementus, ja masīvs, saraksts, kas tiek nodots `for` ciklam, neeksistē.

Piemērs no projekta:

```django
{% for item in data %}
            <div class="w-auto rounded-md flex flex-col
            items-center mx-2">
                <!-- Cena  -->
                <p class="font-semibold text-gray-800 text-xs text-center">{{ item.value }} EUR</p>

                <!-- Progress bar -->
                <div class="w-2 rounded-full bg-gray-300 h-32 overflow-hidden 
                flex flex-col justify-end">
                    <div class="w-2 rounded-full {% if item.isActiveHourNow == True %} 
                    bg-green-400 {% else %} bg-orange-400 {% endif %} " style="height: {{ item.levelInDailyView }}%"></div>
                </div>
                <!-- Laiks -->
                <p class="font-semibold text-gray-800 text-xs text-center">{{ item.priceStartTime }} - {{ item.priceEndTime }}</p>
            </div>
            {% empty %}
            <!-- Šeit tiek izvietots kods, ja masīvs neeksistē -->
            {% endfor %}
```

Papildus eksistē tāds tags kā `{{ forloop.Counter }}`, tas ļauj skaitīt no viens, ja vajag no nulles, tad `{{ forloop.Counter0 }}`.

```django
{% for order in order_list %}
    {% if order.transaction_id %}
	<tr>
	<td>{{ forloop.counter }}</td>
	<td>{{order.id}}</td>
	<td>{{order.transaction_id}}</td>
	<td>{{order.customer}}</td>
	<td>{{order.date_ordered}}</td>
	<td><a href="{% url 'detailed-transactions' order.id %}">{{ order.transaction_id }}</a></td>
	</tr>
    {% endif %}
{% endfor %}
```

## `if` operators

Nosacījuma tagi `{% if %}`, `{% elif %}`, `{% else %}` ļauj veidot loģiku šablonus. Pašās beigās izvieto tagu `{% endif %}`.

```django
<div class="w-2 rounded-full {% if item.isActiveHourNow == True %} 
bg-green-400 {% else %} bg-orange-400 {% endif %} " style="height: {{ item.levelInDailyView }}%"></div>
```

*Šādu tagu var likt arī stilos.*

Eksistē arī pārbaude uz pēdējo/pirmo elementu:

- `{% if forloop.first %}` - pārbaude uz pirmo elementu;
- `{% if forloop.last %}` - pārbaude uz pēdējo elementu;
- `{% if not forloop.last %}` - pārbaude uz **nav** pēdējais elements.
- `{% endif %}` - obligāti likt to beigās.

## Komentāri

Šādi veido komentāru -> `{# Tas ir komentārs #}`.

## Lorem ipsum

`Django` ļauj veidot arī `lorem ipsum` tekstu.

```django
<p>{% lorem [count] [w/p] %}</p>
```

`[count]` - šīs parametrs nosaka skaitu
`[w]` - vārds
`[p]` - paragrāfs

```django
<p>{% lorem 100 w random %}</p>
```

Šis piemērs veidos tekstu 100 vārdu garumā, katru reizi unikālu, jo `random`.

## Laiks

Lai attēlot tekošu laiku, izmanto tagu `{% now %}`. Tam var piešķirt dažādus formātus.

## Filtri

Kopumā var izcelt šādu popularākos filtrus:

- `{{ value|format:"0" }}` - aiz komata nav ciparu;
- `{{ value|format:2 }}` - 2 cipari aiz komata;
- `{{ value|copfirst }}` - pirmo burdu izvada `Upcase`;
- `{{ value|dictsort:"atslēga" }}` - kārto vārdnīcas vērtības augošā;
- `{{ value|dictsortreversed:"atslēga" }}` - - kārto vārdnīcas vērtības dilstošā.

---

Informācija par tagiem >>> [Built-in template tags and filters \| Django documentation \| Django](https://docs.djangoproject.com/en/5.2/ref/templates/builtins/)

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Kursi (akadēmija)/Back-end Python/Šablona izveide|Šablona izveide]]
Nākama lapa >>> [[Kursi (akadēmija)/Back-end Python/Mantošana|Mantošana]]

---