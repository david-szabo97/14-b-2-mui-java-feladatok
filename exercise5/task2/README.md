# 5.2 / Fájl olvasás - Adatok

## Feladat
Olvassunk be minden személyt és adatait az `e5_t2_input.txt` fájlból.
Az adatok ebben a formában vannak a fájlban:
```
név;kor;magasság
név;kor;magasság
név;kor;magasság
....
```
Tehát pontosvessző választja el egy személy adatait és újsor választja el a személyeket
 - Hozzunk létre egy osztályt amiben tároljuk az adatokat.
   - **Osztály neve: Person**
   - **Konstruktor**
     - Képes minden adott adatból (név, kor, magasság) (**ebben a sorrendben legyenek a paraméterek**) feltölti az adott példányt.
   - **Metódusok**:
     - getName() - Visszaadja a személy nevét
     - getAge() - Visszaadja a személy korát
     - getHeight() - Visszaadja a személy magasságát
   - Az adatok privátak legyenek és ne legyenek megváltoztathatóak. (ne legyen megváltoztatható kulcsszó: **final**)
 - A beolvasott adatokat tároljuk el egy gyűjteményben (**ArrayList**)
 - Írjuk ki hány személy adatát olvastuk be
 - Írjuk ki az átlag életkort
 - Írjuk ki az átlag magasságot
 - Írjuk ki a legfiatalabb, legöregebb, legalacsonyabb, legmagasbb személy adatait
 - Írjuk ki a legrövidebb és leghosszabb nevű személy adatait
 

## Segédlet
```java
// Beolvasáshoz
Scanner s = new Scanner(new File("file.txt"));

// Beállítjuk hogy Scanner a ";" és "\n" használja elválasztóként.
// Tehát ha találkozik egy ";" vagy "\n"-val akkor onnantól új adatnak tekinti a többit
// "|" (pipe) több elválasztót is megadhatunk, itt jól látszik hogy a kettő között pipe van
// Tehát pontosvessző(;) VAGY(pipe) újsor(\\n)
s.useDelimiter(";|\\n");

// Példa a megváltoztathatlan mezőre
// Ezeknek a mezőknek CSAK konstruktorból lehet értéket adni
public final int youCantChangeMe;
```

## Példa 1
Kimenet
```
Személyek száma: 50
Átlag életkor: 41.32
Átlag magasság: 173.28
Legfiatalabb: Jake Watson;18;190
Legöregebb: Allison Ingram;65;169
Legalacsonyabb: Cora Wheeler;59;150
Legmagasabb: Claude Kelley;38;198
Legrövidebb nevű: Toby Cook;26;182
Leghosszabb nevű: Priscilla Robertson;49;170
```