# [Linux] Bash history használata: A parancs előzményeinek megjelenítése

## Overview
A `history` parancs megjeleníti a Bash shellben végrehajtott parancsok listáját. Ez lehetővé teszi a felhasználók számára, hogy könnyen visszakeressék és újra felhasználják a korábban használt parancsokat.

## Usage
A `history` parancs alapvető szintaxisa a következő:

```bash
history [options] [arguments]
```

## Common Options
- `-c`: Törli a parancsok előzményeit.
- `-d offset`: Törli a megadott offsetű parancsot a történelemből.
- `n`: Megjeleníti az utolsó `n` parancsot.

## Common Examples
1. **Az összes parancs megjelenítése:**
   ```bash
   history
   ```

2. **Az utolsó 10 parancs megjelenítése:**
   ```bash
   history 10
   ```

3. **Egy adott parancs újra végrehajtása:**
   Ha például a 25-ös parancsot szeretnéd újra futtatni:
   ```bash
   !25
   ```

4. **A parancsok törlése:**
   Az összes parancs törléséhez:
   ```bash
   history -c
   ```

## Tips
- Használj `!n` szintaxist a parancsok gyors újrafuttatásához, ahol `n` a parancs sorszáma.
- Rendszeresen töröld a történetet, ha érzékeny információkat tartalmaz.
- Használj aliasokat a gyakran használt parancsok gyorsabb eléréséhez, így kevesebb parancsot kell megjegyezned.