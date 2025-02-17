# [Linux] Bash csoportok használata: Felhasználói csoportok megjelenítése

## Áttekintés
A `groups` parancs megjeleníti a felhasználó csoportjait a Linux operációs rendszerben. Hasznos eszköz a felhasználói jogosultságok és csoporttagságok ellenőrzésére.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
groups [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`, `--help`: Megjeleníti a parancs használatával kapcsolatos súgót.
- `-n`, `--no-group`: Csak a felhasználó csoportjait jeleníti meg, a csoportnevek nélkül.

## Gyakori példák

1. **A jelenlegi felhasználó csoportjainak megjelenítése:**

```bash
groups
```

2. **Egy adott felhasználó csoportjainak megjelenítése:**

```bash
groups felhasználónév
```

3. **A csoportok megjelenítése csoportnevek nélkül:**

```bash
groups -n
```

4. **Súgó megjelenítése:**

```bash
groups --help
```

## Tippek
- Használja a `groups` parancsot a felhasználói jogosultságok gyors ellenőrzésére.
- Ha több felhasználó csoportjait szeretné megjeleníteni, egyszerre több felhasználónevet is megadhat.
- A `groups` parancs kimenete segíthet a rendszeradminisztrátoroknak a felhasználói csoportok kezelésében és a jogosultságok beállításában.