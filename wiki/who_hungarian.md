# [Linux] Bash who használata: Aktív felhasználók listázása

## Áttekintés
A `who` parancs megjeleníti a rendszerben bejelentkezett felhasználók listáját. Hasznos információkat nyújt a felhasználók nevéről, a bejelentkezésük időpontjáról és a használt terminálokról.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
who [opciók] [argumentumok]
```

## Gyakori Opciók
- `-a`: Minden elérhető információt megjelenít a felhasználókról.
- `-b`: Megjeleníti a legutóbbi rendszerindítás időpontját.
- `-q`: Csak a bejelentkezett felhasználók számát és nevét mutatja.
- `--help`: Segítséget nyújt a parancs használatához.

## Gyakori Példák
1. **Alapvető felhasználói lista megjelenítése:**
   ```bash
   who
   ```

2. **Részletes információk megjelenítése:**
   ```bash
   who -a
   ```

3. **A legutóbbi rendszerindítás időpontjának megjelenítése:**
   ```bash
   who -b
   ```

4. **Csak a bejelentkezett felhasználók számának és nevüknek megjelenítése:**
   ```bash
   who -q
   ```

## Tippek
- Használja a `who` parancsot rendszeresen, hogy nyomon követhesse, ki van bejelentkezve a rendszerébe.
- Kombinálja a `who` parancsot más parancsokkal, például a `grep`-pel, hogy szűkítse a keresést egy adott felhasználóra.
- A `who` parancs kimenete hasznos lehet a rendszeradminisztráció során, különösen, ha több felhasználó dolgozik egyidejűleg.