⏲ **Datums:** 2025-05-09   
⏲ **Laiks:** 10:27 

❚ **Tagi:**  #NoSQL  
⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Visual Studio konfigurēšana
Sākumā izveido jauno konsoles projektu.

Pirmām kārtām nepieciešams instalēt plaginu, to var izdarīt divos veidos:
- grafiski;
- caur paķešu menedžeri: `dotnet add package CassandraCSharpDriver`

Lai turpināt tālāko darbību, ir nepieciešams tokens ar administratora un `secure-connect-your-db.zip` arhīvs, abus vajag iegūt no DataStax.

Pēc tam projektā ievieto šo te kodu:

```cs
using System;
using Cassandra;
using System.Linq;

namespace astraconnect
{
    class Program
    {
        static void Main(string[] args)
        {
            var session =
                Cluster.Builder()
                    .WithCloudSecureConnectionBundle(@"C:\Path\To\secure-connect-sesija.zip") //ceļš līdz arhīvam
                    .WithCredentials("your-client-id", "your-client-secret") //tokena dati
                    .Build()
                    .Connect("mans-keyspace"); //šeit ievadi savu keyspace

            //vaicājums
            var rowSet = session.Execute("SELECT * FROM books");

            //iterācija pa ierakstiem (rindām)
            foreach (var row in rowSet)
            {
                //datu izvilkšana
                 var id = row.GetValue<Guid>("id"); //id iegūšana
				 var title = row.GetValue<string>("title"); //string
				 var author = row.GetValue<string>("author"); //string
			     var year = row.GetValue<int>("year"); //int dati
			     var topics = row.GetValue<List<string>>("topics"); //saraksti
			     var topicsFormatted = string.Join(", ", topics); //sarakstu apvienošana
				 //informācijas izvads
			     Console.WriteLine($"ID: {id} | Title: {title} | Author: {author} | Year: {year} | Topics: {topicsFormatted}");
            }
        }
    }
}
```

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Cassandra CQL]]
Nākama lapa >>> [[Navigācija - NoSQL DB]]

---