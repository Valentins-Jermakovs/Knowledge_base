___

**Datums:** 2025-09-13
**Laiks:** 21:52
❚ **Tagi:** #java #OOP 

---
### Mantošana

Apakšklase mato virsklases ne `private` atribūtus un metodes.

```java
class Animal {
  protected int legs;
  public void eat() {
    System.out.println("Animal eats");
  }
}

class Dog [b]extends [/b]Animal {
  Dog() {
    legs = 4;
  }
}
```

Šeit apakšklase `Dog` manto gan atribūtu, gan metodi:

```java
class MyClass {
	public static void main (String [] args) {
		Dog dog = new Dog();
		dog.eat();
	}
}
```


> [!NOTE] Par `protected`
> Pieejas modifikators `protected` ir pieejams apakšklasēs!


---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Mantošana ievads]]
Nākama lapa >>> [[Polimorfisms]]

---