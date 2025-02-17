# [Linux] Bash docker-compose használata: Konténerek kezelése egyszerűen

## Áttekintés
A `docker-compose` parancs lehetővé teszi több Docker konténer együttes kezelését egy egyszerű konfigurációs fájl segítségével. Ezzel a parancssal könnyen definiálhatók és futtathatók a konténerek, így egyszerűsítve a komplex alkalmazások telepítését és kezelését.

## Használat
A `docker-compose` parancs alapvető szintaxisa a következő:

```bash
docker-compose [opciók] [argumentumok]
```

## Gyakori opciók
- `up`: Futtatja a konténereket a `docker-compose.yml` fájlban definiáltak szerint.
- `down`: Leállítja és eltávolítja a konténereket, hálózatokat és köteteket.
- `build`: Létrehozza a szolgáltatásokhoz szükséges képeket.
- `logs`: Megjeleníti a konténerek naplóit.
- `ps`: Listázza a futó konténereket.

## Gyakori példák
1. **Konténerek indítása**:
   ```bash
   docker-compose up
   ```

2. **Konténerek háttérben történő indítása**:
   ```bash
   docker-compose up -d
   ```

3. **Konténerek leállítása és eltávolítása**:
   ```bash
   docker-compose down
   ```

4. **Szolgáltatások újraépítése**:
   ```bash
   docker-compose build
   ```

5. **Naplók megtekintése**:
   ```bash
   docker-compose logs
   ```

## Tippek
- Mindig használj `docker-compose.yml` fájlt a konténerek konfigurálásához, hogy könnyen kezelhesd a szolgáltatásokat.
- Használj `-d` opciót, ha nem szeretnéd, hogy a konténerek a terminálban fussanak.
- Ellenőrizd a konténerek állapotát a `docker-compose ps` paranccsal, hogy biztos legyél benne, hogy minden megfelelően fut.
- A `docker-compose` parancsot gyakran használják fejlesztési környezetekben, így érdemes ismerni a legfontosabb parancsokat és opciókat.