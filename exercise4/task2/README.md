# 4.2

## Feladat
Hozzatok létre egy `MathHelper` osztályt. Ez az osztály néhány egyszerű matematikai műveletet fog elvégezni nekünk egész számú tömbökön.

**Metódusok**:
- **min**
	- Visszadja a **legkisebb** egész számot a tömbböl.
- **max**
	- Viszaadja a **legnagyobb** egész számot a tömbböl.
- **avg**
	- Visszadja a számok **átlagát** (float).
- **median**
	- Visszaadja a **mediánt** (float). Rendezett tömbböl a középső elem, ha az elemek száma páros akkor a két középső érték átlagát.
- **modus**
	- BÓNUSZ FELADAT: Visszaadja a **legtöbbször előforduló értéket** a tömbböl. (Ha több érték is ugyanannyiszor fordul elő, akkor elég a legelsőt visszaadni.)

Minden metódus publikus. Paraméterként mindegyik egy egész szám tömböt kap.

## Segédlet
```java
// Példa tömb paraméterre
public class ArrayParameterExample {
//                         VVVV
  public int highestNumber(int[] numbers) {
    int max = 0;

    for (int number : numbers) {
      if (number > max) {
        max = number;
      }
    }

    return max;
  }

}

// Tömb rendezése, ennek nincs visszatérési értéke, a megadott tömböt rendezi növekvő sorrendben.
Arrays.sort(tomb);
```

## Példa 1
Forrás
```java
MathHelper helper = new MathHelper();

int[] T1 = new int[] {3, 1, 5, 10, 6, 3, 1};
int[] T2 = new int[] {9, 10, 10, 5, 3, 2};

System.out.println("T1 teszt: ");
System.out.println("Min: "+helper.min(T1));
System.out.println("Max: "+helper.max(T1));
System.out.println("Avg: "+helper.avg(T1));
System.out.println("Median: "+helper.median(T1));
System.out.println("Modus: "+helper.modus(T1));

System.out.println();

System.out.println("T2 teszt: ");
System.out.println("Min: "+helper.min(T2));
System.out.println("Max: "+helper.max(T2));
System.out.println("Avg: "+helper.avg(T2));
System.out.println("Median: "+helper.median(T2));
System.out.println("Modus: "+helper.modus(T2));
```

Kimenet
```
T1 teszt: 
Min: 1
Max: 10
Avg: 4.142857
Median: 10.0
Modus: 3

T2 teszt: 
Min: 2
Max: 10
Avg: 6.5
Median: 4.0
Modus: 10
```