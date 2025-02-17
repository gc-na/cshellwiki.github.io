# [Linux] Bash uname használat: Rendszerinformációk megjelenítése

## Áttekintés
A `uname` parancs a rendszer információinak megjelenítésére szolgál, mint például a kernel neve, verziója és architektúrája. Hasznos eszköz a rendszer jellemzőinek gyors ellenőrzésére.

## Használat
A `uname` parancs alapvető szintaxisa a következő:

```bash
uname [opciók] [argumentumok]
```

## Gyakori opciók
- `-a`: Minden elérhető információt megjelenít a rendszerről.
- `-s`: A kernel nevét mutatja.
- `-n`: A hálózati gépnevet adja vissza.
- `-r`: A kernel verzióját jeleníti meg.
- `-v`: A kernel kiadásának részleteit mutatja.
- `-m`: A gép architektúráját adja vissza.

## Gyakori példák
1. A kernel neve:
   ```bash
   uname -s
   ```

2. A kernel verziója:
   ```bash
   uname -r
   ```

3. Minden elérhető információ megjelenítése:
   ```bash
   uname -a
   ```

4. A gép architektúrájának megjelenítése:
   ```bash
   uname -m
   ```

5. A hálózati gépnév lekérdezése:
   ```bash
   uname -n
   ```

## Tippek
- Használja az `-a` opciót, ha gyorsan szeretne átfogó információt kapni a rendszerről.
- A `uname` parancsot script-ekben is használhatja, hogy dinamikusan ellenőrizze a rendszer jellemzőit.
- Kombinálja más parancsokkal, mint például a `grep`, hogy szűkítse az információkat.