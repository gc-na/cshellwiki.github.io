# [Linux] Bash bg használat: Háttérben futó folyamatok

## Áttekintés
A `bg` parancs lehetővé teszi a felhasználók számára, hogy a háttérben futtassanak folyamatokat a Bash környezetben. Ez hasznos, amikor egy folyamatot el szeretnénk indítani, de nem akarjuk, hogy a terminálunkat blokkolja.

## Használat
A `bg` parancs alapvető szintaxisa a következő:

```bash
bg [opciók] [argumentumok]
```

## Gyakori opciók
- **%job_id**: A háttérbe helyezni kívánt folyamat azonosítója, amelyet a `jobs` parancs segítségével találhatunk meg.
- **-l**: A folyamatok listázása hosszú formátumban.

## Gyakori példák

1. **Folyamat háttérbe helyezése**
   Ha egy folyamatot elindítunk, például egy hosszú futású szkriptet, és a Ctrl + Z billentyűkombinációval leállítjuk, a következő paranccsal helyezhetjük a háttérbe:
   ```bash
   bg %1
   ```

2. **Összes háttérben futó folyamat listázása**
   A `jobs` parancs segítségével megtekinthetjük az összes háttérben futó folyamatot:
   ```bash
   jobs
   ```

3. **Folyamat újraindítása háttérben**
   Ha egy folyamatot leállítottunk, és szeretnénk újraindítani a háttérben:
   ```bash
   bg
   ```

## Tippek
- Használja a `jobs` parancsot a háttérben futó folyamatok nyomon követésére.
- A `fg` parancs segítségével visszahozhatja a háttérben futó folyamatot a terminálba, ha szüksége van rá.
- Ügyeljen arra, hogy a háttérben futó folyamatok kimenete ne zavarja a munkáját; érdemes lehet átirányítani a kimenetet fájlokba.