# 4.1

## Feladat
Hozzatok létre egy **absztrakt** `Shape` osztályt amelynek van 2 **absztrakt** metódusa: `area()` (terület), `perimeter()` (kerület) ezek **nem egész számot** adjanak vissza, de minnél **precízebb** legyen (`double`). 

Majd hozzatok létre két öröklő osztályt: 
1. `Rectangle`, amelynek van két adattagja: `width`, `height`. Ezeket lehessen megadni **konstruktorral**.
2. `Circle`, ennek egy adattagja van: `radius`. Ezt lehessen megadni **konstruktorral**. 

Az adattagok, metódusok, osztályok legyenek publikusak. Mindkét osztály **írja felül** a metódusokat `area()` és `perimeter()` és adjanak vissza egy nem egész számot, amely a terület (`area()`) és a kerület (`perimeter()`).

## Segédlet
```java
public abstract class ParentClass {
  public abstract int myMethod();
}

public class ChildClass extends ParentClass {
  public int myField;

  public ChildClass(int myField) {
    this.myField = myField;
  }

  @Override
  public int myMethod() {
    return this.myField;
  }
}
```

## Példa 1
Forrás
```java
Rectangle rect = new Rectangle(5, 10);
Circle circle = new Circle(50);

System.out.println(rect.area()+" "+rect.perimeter());
System.out.println(circle.area()+ "+circle.perimeter());
```

Kimenet
```
50 30
7853.981633974483 314.1592653589793
```