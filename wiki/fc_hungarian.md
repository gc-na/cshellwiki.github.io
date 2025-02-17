# [Linux] Bash fc használata: Parancsok szerkesztése és végrehajtása

## Áttekintés
A `fc` parancs a Bash környezetben használt eszköz, amely lehetővé teszi a felhasználók számára, hogy megtekintsék, szerkesszék és újra végrehajtsák a korábbi parancsokat. Ez különösen hasznos lehet, ha egy korábbi parancsot szeretnénk módosítani, vagy ha gyakran használunk bizonyos parancsokat.

## Használat
A `fc` parancs alapvető szintaxisa a következő:

```bash
fc [opciók] [argumentumok]
```

## Gyakori Opciók
- `-l`: Listázza a korábbi parancsokat.
- `-s`: Az utolsó parancsot végrehajtja, anélkül, hogy megnyitná a szerkesztőben.
- `-n`: A parancsok listázásakor ne jelenítse meg a sorszámokat.

## Gyakori Példák
1. **Korábbi parancsok listázása**:
   A legutóbbi 16 parancs megjelenítése:
   ```bash
   fc -l
   ```

2. **Egy adott parancs szerkesztése**:
   Az utolsó parancs megnyitása a szerkesztőben:
   ```bash
   fc
   ```

3. **Egy konkrét parancs végrehajtása**:
   Az utolsó parancs végrehajtása anélkül, hogy megnyitnánk a szerkesztőben:
   ```bash
   fc -s
   ```

4. **Korábbi parancsok listázása sorszámok nélkül**:
   Az utolsó 10 parancs megjelenítése sorszámok nélkül:
   ```bash
   fc -ln -10
   ```

## Tippek
- Használj `fc`-t, ha gyakran futtatsz hasonló parancsokat, így könnyen módosíthatod őket.
- A `fc` parancs használata előtt érdemes megismerni a használt szövegszerkesztőt, mert a parancs ezt fogja használni a parancsok szerkesztéséhez.
- Kísérletezz a `-l` és `-n` opciókkal, hogy gyorsan áttekintsd a parancsaidat anélkül, hogy zavaró sorszámokat látnál.