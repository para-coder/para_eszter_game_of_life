# Conway-féle Életjáték Pythonban

A projektünk a Conway-féle Életjáték (Game of Life) nevű sejtautomata működését mutatja be. Az Életjátékot John Conway matematikus alkotta meg 1970-ben. A program egy kétdimenziós rácson szimulálja a sejtek fejlődését, ahol minden cella kétféle állapotban lehet: élő vagy halott.

A sejtek állapota generációról generációra változik a szomszédos sejtek száma alapján. Bár a szabályok egyszerűek, a rendszer rendkívül érdekes és összetett mintázatok kialakulására képes.

A projekt Python nyelven készült el, :contentReference[oaicite:0]{index=0} környezetben. A számításokat :contentReference[oaicite:1]{index=1} segítségével végezzük, a vizualizációhoz a :contentReference[oaicite:2]{index=2} `heatmap()` függvényét használjuk, az animációt pedig a :contentReference[oaicite:3]{index=3} `FuncAnimation()` osztálya valósítja meg.

## Az Életjáték szabályai

Minden cellának legfeljebb 8 szomszédja van. Az új generáció az alábbi szabályok szerint jön létre:

1. Egy élő sejt kevesebb mint 2 élő szomszéd esetén elpusztul.
2. Egy élő sejt 2 vagy 3 élő szomszéd esetén életben marad.
3. Egy élő sejt több mint 3 élő szomszéd esetén elpusztul.
4. Egy halott sejt pontosan 3 élő szomszéd esetén életre kel.

## A feltöltött `game_of_life.ipynb` fájl

A `game_of_life.ipynb` notebook tartalmazza a program teljes megvalósítását. A notebook futtatása során:

- létrejön egy véletlen kezdeti rács,
- a program minden generációban kiszámolja az új állapotot,
- a rács animált formában jelenik meg,
- a generációk folyamatosan frissülnek.

A program elején három paraméter módosítható:

```python
SIZE = 30
P_ALIVE = 0.5
INTERVAL = 400
