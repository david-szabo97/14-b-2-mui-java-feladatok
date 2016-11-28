# 5.1 / Fájl olvasásos - Sorok

## Feladat
Olvassunk be minden sort a `e5_t1_input.txt` fájlból és irassuk ki a képernyőre.

## Segédlet
```java
// Megoldás 1
// Miért jó ez? Hatékonyabb a Scanner-nél mert nagyobb a belső tárolója (buffer)
// Tehát ha hosszú sorokat akarsz olvasni ez a megoldás gyorsabb
BufferedReader br = new BufferedReader(new FileReader("file.txt"));

// Megoldás 2
// Miért jó ez? Lassabb mint a BufferedReader ha hosszú sorokat olvasol, de ha mást
// is olvasnod kell a sorokon kívül (pl szám), akkor a Scanner-rel ezt is megteheted
Scanner s = new Scanner(new File("file.txt"));
```

## Példa 1
Kimenet
```
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Morbi id dolor eget erat vehicula venenatis id volutpat mi.
Sed dictum tellus in tellus cursus rutrum.
Vestibulum a porta est.
Integer maximus, orci vel tristique volutpat, urna est egestas urna, non porta tortor orci vel mi.
Donec eu faucibus mi, sed consectetur augue.
Nulla neque lectus, hendrerit ac nibh eu, aliquet gravida dui.
Curabitur placerat non leo vel lacinia.
Praesent non ex malesuada magna bibendum laoreet et quis nisi.
Quisque mauris mi, elementum non lacus a, consectetur porta eros.
Curabitur sed risus velit.
```