# [Linux] Bash netstat használat: Hálózati kapcsolatok és statisztikák megjelenítése

## Áttekintés
A `netstat` parancs a hálózati kapcsolatok, a routing táblák, az interfészek statisztikái és a protokollok állapotának megjelenítésére szolgál. Segítségével könnyen nyomon követhetjük a rendszer hálózati aktivitását.

## Használat
A `netstat` parancs alapvető szintaxisa a következő:

```bash
netstat [opciók] [argumentumok]
```

## Gyakori opciók
- `-a`: Minden kapcsolat és hallgató port megjelenítése.
- `-t`: Csak a TCP kapcsolatok megjelenítése.
- `-u`: Csak az UDP kapcsolatok megjelenítése.
- `-n`: A címek és portok numerikus formátumban való megjelenítése.
- `-l`: Csak a hallgató portok megjelenítése.

## Gyakori példák
1. **Minden aktív kapcsolat megjelenítése:**
   ```bash
   netstat -a
   ```

2. **Csak a TCP kapcsolatok listázása:**
   ```bash
   netstat -t
   ```

3. **Hallgató portok megjelenítése:**
   ```bash
   netstat -l
   ```

4. **Numerikus címek és portok megjelenítése:**
   ```bash
   netstat -n
   ```

5. **TCP és UDP kapcsolatok együttes megjelenítése:**
   ```bash
   netstat -tu
   ```

## Tippek
- Használja a `-p` opciót, hogy lássa, melyik folyamat használja a kapcsolatokat.
- A `netstat` parancs kimenetei segíthetnek a hálózati problémák diagnosztizálásában.
- Érdemes a `grep` parancsot használni a kimenet szűrésére, például: 
  ```bash
  netstat -a | grep LISTEN
  ```