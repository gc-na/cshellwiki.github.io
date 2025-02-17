# [Linux] Bash screen használata: A terminál többfeladatos kezelése

## Áttekintés
A `screen` parancs lehetővé teszi a felhasználók számára, hogy több virtuális terminál ablakot hozzanak létre és kezeljenek egyetlen fizikai terminálon. Ez különösen hasznos távoli munkavégzés során, mivel a `screen` lehetővé teszi a munkamenetek lebegtetését és későbbi folytatását.

## Használat
A `screen` parancs alapvető szintaxisa a következő:

```bash
screen [opciók] [argumentumok]
```

## Gyakori opciók
- `-S <név>`: Nevezze el a screen munkamenetet.
- `-d -r <név>`: Csatlakozzon egy leválasztott munkamenethez.
- `-list`: Listázza az elérhető screen munkameneteket.
- `-L`: Engedélyezze a naplózást a munkamenet során.

## Gyakori példák
1. **Új screen munkamenet indítása:**
   ```bash
   screen
   ```

2. **Munkamenet névvel való indítása:**
   ```bash
   screen -S mysession
   ```

3. **Leválasztott munkamenethez való csatlakozás:**
   ```bash
   screen -d -r mysession
   ```

4. **Munkamenetek listázása:**
   ```bash
   screen -list
   ```

5. **Munkamenet naplózása:**
   ```bash
   screen -L
   ```

## Tippek
- Használja a `Ctrl + A`, majd `D` billentyűkombinációt a munkamenet leválasztásához anélkül, hogy megszakítaná a folyamatokat.
- Nevezze el a munkameneteket, hogy könnyebben azonosíthassa őket, különösen, ha több munkamenetet futtat.
- Rendszeresen ellenőrizze a naplófájlokat, ha problémák merülnek fel, vagy ha vissza szeretné nézni a korábbi munkameneteket.