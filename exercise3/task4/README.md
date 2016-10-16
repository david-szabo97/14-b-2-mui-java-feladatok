# 3.4

## Feladat
Neveket kér be mindaddig amíg nem írunk be `x` -et.

Kiírja hány nevet írtunk be, és ezek mennyi karakterből áll összesen, leghosszabb nevet, legrövidebb nevet.

## Segédlet
```java
ArrayList<String> names = new ArrayList<>();
names.add("Pityu");

for (String name : names) {
  System.out.println(name+" :  "+name.length());
}
```

## Példa #1
Bemenet
```
Norbert
Pityu
Lajos
Béla
x
```

Kimenet
```Nevek száma: 3
Karakterek száma: 14
Leghosszabb név: Norbert
Legrövidebb név: Béla
```