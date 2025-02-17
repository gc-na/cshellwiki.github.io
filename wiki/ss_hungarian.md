# [Linux] Bash ss használat: Hálózati kapcsolatok megjelenítése

## Áttekintés
Az `ss` parancs a Linux operációs rendszerben a hálózati kapcsolatok, socketek és portok állapotának megjelenítésére szolgál. Gyorsabb és részletesebb alternatívája a régebbi `netstat` parancsnak.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
ss [opciók] [argumentumok]
```

## Gyakori opciók
- `-t`: Csak TCP kapcsolatok megjelenítése.
- `-u`: Csak UDP kapcsolatok megjelenítése.
- `-l`: Csak a hallgató socketek listázása.
- `-p`: A folyamatok azonosítójának (PID) és nevüknek megjelenítése.
- `-n`: A címek és portok numerikus formátumban való megjelenítése.

## Gyakori példák
1. **Összes aktív kapcsolat megjelenítése:**

   ```bash
   ss
   ```

2. **Csak TCP kapcsolatok megjelenítése:**

   ```bash
   ss -t
   ```

3. **Csak UDP kapcsolatok megjelenítése:**

   ```bash
   ss -u
   ```

4. **Hallgató socketek listázása:**

   ```bash
   ss -l
   ```

5. **Folyamatok megjelenítése a kapcsolatokkal együtt:**

   ```bash
   ss -p
   ```

6. **Numerikus címek és portok megjelenítése:**

   ```bash
   ss -n
   ```

## Tippek
- Használja a `-s` opciót a statisztikák gyors megjelenítéséhez, amely összegzi a különböző típusú socketek számát.
- A `ss` parancs kombinálható más parancsokkal, például a `grep`-pel, hogy szűkítse a megjelenített információkat.
- Érdemes a `man ss` parancsot futtatni a részletes dokumentáció megtekintéséhez és a további opciók felfedezéséhez.