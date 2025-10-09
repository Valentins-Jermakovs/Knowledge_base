___

**Datums:** 2025-10-09
**Laiks:** 20:07
❚ **Tagi:** #back-end #NET 

---
# Fluent API

Fluent API ir **alternatīva Data Annotations**, un tas ļauj **pilnībā konfigurēt modeļus** programmatiski, neizmantojot atribūtus klasēs. Tas tiek **definēts `DbContext` iekš `OnModelCreating` metodē**.

![[Pasted image 20251009201159.png]]

| Funkcija                      | Fluent API piemērs                                                                                | Piezīme                           |
| ----------------------------- | ------------------------------------------------------------------------------------------------- | --------------------------------- |
| **Primārā atslēga**           | `modelBuilder.Entity<Product>().HasKey(p => p.Id);`                                               | Tāpat kā `[Key]`                  |
| **Obligāts lauks (NOT NULL)** | `modelBuilder.Entity<Product>().Property(p => p.Name).IsRequired();`                              | Tāpat kā `[Required]`             |
| **Maksimālais lauka garums**  | `modelBuilder.Entity<Product>().Property(p => p.Name).HasMaxLength(100);`                         | Tāpat kā `[MaxLength]`            |
| **Kolonnas nosaukums**        | `modelBuilder.Entity<Product>().Property(p => p.Name).HasColumnName("sName");`                    | Tāpat kā `[Column]`               |
| **Tabulas nosaukums / shēma** | `modelBuilder.Entity<Product>().ToTable("tbl_Product", "catalog");`                               | Tāpat kā `[Table]`                |
| **Ārējā atslēga**             | `modelBuilder.Entity<Order>().HasOne(o => o.Product).WithMany().HasForeignKey(o => o.ProductId);` | Tāpat kā `[ForeignKey]`           |
| **Unikāls indekss**           | `modelBuilder.Entity<Product>().HasIndex(p => p.SKU).IsUnique();`                                 | Tāpat kā `[Index(IsUnique=true)]` |

Koda piemērs:

```cs
public class ApplicationDbContext : DbContext
{
    public DbSet<Product> Products { get; set; }

    protected override void OnModelCreating(ModelBuilder modelBuilder)
    {
        // Tabulas nosaukums un shēma
        // tbl_Product - tabulas nosaukums
        // catalog - shēmas nosaukums
        modelBuilder.Entity<Product>()
            .ToTable("tbl_Product", "catalog");

        // Primārā atslēga
        modelBuilder.Entity<Product>()
            .HasKey(p => p.Id);

        // Lauki
        modelBuilder.Entity<Product>()
            .Property(p => p.Name) // atlasam lauku Name
            .IsRequired() // lauks ir obligāt NOT NULL
            .HasMaxLength(100) // ierobežo garumu
            .HasColumnName("sName"); // maina nosaukumu

        // Unikāls indekss
        modelBuilder.Entity<Product>()
            .HasIndex(p => p.SKU) // iestatam indeksu uz lauku
            .IsUnique(); // indekss ir unikāls
    }
}

public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string SKU { get; set; }
}

```

Fluent API **pārspēj Data Annotations**, ja tie abi ir lietoti vienlaicīgi.

Izmanto vienu no diviem:

- **Mazs projekts / vienkārša konfigurācija → Data Annotations**
- **Liels projekts / sarežģīti ierobežojumi → Fluent API**

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Data Annotation]]
Nākama lapa >>> [[šablons]]

---