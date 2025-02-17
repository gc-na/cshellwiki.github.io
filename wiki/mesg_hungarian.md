# [Linux] Bash mesg használat: Üzenetek fogadása vagy elutasítása

## Áttekintés
A `mesg` parancs a felhasználói üzenetek fogadásának vagy elutasításának beállítására szolgál a terminálban. Ezzel a parancssal lehetőséged van arra, hogy szabályozd, ki küldhet üzeneteket neked, amikor a terminál aktív.

## Használat
A `mesg` parancs alapvető szintaxisa a következő:

```bash
mesg [opciók] [érvek]
```

## Gyakori opciók
- `y` - Engedélyezi az üzenetek fogadását.
- `n` - Megakadályozza az üzenetek fogadását.
- `--help` - Megjeleníti a parancs használati útmutatóját.

## Gyakori példák
1. Üzenetek fogadásának engedélyezése:

```bash
mesg y
```

2. Üzenetek fogadásának letiltása:

```bash
mesg n
```

3. A parancs súgójának megjelenítése:

```bash
mesg --help
```

## Tippek
- Használj `mesg n` parancsot, ha nem szeretnél zavaró üzeneteket kapni, különösen, ha nyilvános terminálon dolgozol.
- Ellenőrizd a beállításaidat a `mesg` parancs egyszerű futtatásával, amely megmutatja az aktuális állapotot.
- Ne feledd, hogy a `mesg` parancs hatása csak a jelenlegi terminálra vonatkozik, így ha új terminált nyitsz, szükség lehet a beállítások megismétlésére.