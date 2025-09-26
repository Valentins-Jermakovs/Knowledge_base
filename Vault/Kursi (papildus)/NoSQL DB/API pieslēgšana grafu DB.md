⏲ **Datums:** 2025-05-10   
⏲ **Laiks:** 13:34 

❚ **Tagi:**  #NoSQL 
⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Visual Studio konfigurēšana

Paķešu menedžerī ievadi šo komandu, lai instalēt plaginu:
`NuGet\Install-Package Neo4j.Driver -Version 5.28.1`

Projektā ielīme šo kodu:

```cs
using Neo4j.Driver;

const string uri = "neo4j+s://96b742b0.databases.neo4j.io";
const string user = "<Username>";
const string password = "<Password>";

await using var driver = GraphDatabase.Driver(uri, AuthTokens.Basic(user, password));
await driver.VerifyConnectivityAsync();
```

Šeit ievadi savu lietotājvārdu `"<Username>"`
Šeit paroli `"<Password>"`
#### Mans piemērs

```cs
using Neo4j.Driver;

const string uri = "neo4j+s://96b742b0.databases.neo4j.io";
const string user = "neo4j";
const string password = "oriEpQ082iB6bUHxZ2p4yX_HncUafYZHXjlBmz7d5vg";

await using var driver = GraphDatabase.Driver(uri, AuthTokens.Basic(user, password));
await driver.VerifyConnectivityAsync();

try
{
    await using var session = driver.AsyncSession(o=> o.WithDatabase("neo4j"));
    var cypherQuery = @"
            MATCH(a:Actor)
            RETURN a.name AS Name
            ORDER BY a.name";
    var result = await session.RunAsync(cypherQuery);
    await result.ForEachAsync(record =>
    {
        var name = record["Name"]as string;
        Console.WriteLine(name);
    });
}
catch
{
    Console.WriteLine("Error!");
}
finally
{
    driver.Dispose();
}
```
#### Lekcijas piemērs

![[Pasted image 20250510134835.png]]
#### DB username un parole no txt faila

```txt
# Wait 60 seconds before connecting using these details, or login to https://console.neo4j.io to validate the Aura Instance is available
NEO4J_URI=neo4j+s://96b742b0.databases.neo4j.io

NEO4J_USERNAME=neo4j
NEO4J_PASSWORD=oriEpQ082iB6bUHxZ2p4yX_HncUafYZHXjlBmz7d5vg

AURA_INSTANCEID=96b742b0
AURA_INSTANCENAME=Free instance
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Neo4js Aura DB]]
Nākama lapa >>> [[Navigācija - NoSQL DB]]

---