# [Linux] Bash whoami használat: Az aktuális felhasználó nevének megjelenítése

## Áttekintés
A `whoami` parancs megjeleníti az aktuális felhasználó nevét, aki a parancsot futtatja. Ez hasznos lehet, ha több felhasználóval dolgozunk egy rendszeren, és szeretnénk tudni, hogy éppen ki van bejelentkezve.

## Használat
A `whoami` parancs alapvető szintaxisa a következő:

```bash
whoami [opciók] [argumentumok]
```

## Gyakori opciók
A `whoami` parancsnak nincsenek különösebb opciói, mivel a funkciója rendkívül egyszerű. Azonban a következő opciókat használhatjuk:

- `--help`: Megjeleníti a parancs használatával kapcsolatos súgót.

## Gyakori példák
Íme néhány gyakori példa a `whoami` parancs használatára:

1. Az aktuális felhasználó nevének megjelenítése:
   ```bash
   whoami
   ```

2. A parancs súgójának megjelenítése:
   ```bash
   whoami --help
   ```

## Tippek
- Használja a `whoami` parancsot script írásakor, hogy dinamikusan lekérdezze a futtató felhasználó nevét.
- A `whoami` parancsot kombinálhatja más parancsokkal, például a `echo` parancs használatával, hogy testreszabott üzeneteket jelenítsen meg:
  ```bash
  echo "Jelenlegi felhasználó: $(whoami)"
  ```
- A `whoami` parancsot különösen hasznos lehet, ha SSH-n keresztül csatlakozik egy távoli gépre, és szeretné megerősíteni a bejelentkezett felhasználót.