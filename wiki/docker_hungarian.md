# [Linux] Bash docker használata: Konténerizálás és alkalmazáskezelés

## Áttekintés
A `docker` parancs egy nyílt forráskódú platform, amely lehetővé teszi az alkalmazások konténerekbe történő csomagolását, terjesztését és futtatását. A Docker segítségével könnyen kezelhetjük az alkalmazásokat és azok függőségeit, függetlenül a környezettől.

## Használat
A `docker` parancs alapvető szintaxisa a következő:

```bash
docker [opciók] [argumentumok]
```

## Gyakori opciók
- `run`: Új konténer indítása.
- `ps`: A futó konténerek listázása.
- `images`: A helyi képek listázása.
- `pull`: Kép letöltése a Docker Hub-ról.
- `push`: Kép feltöltése a Docker Hub-ra.
- `rm`: Konténer törlése.

## Gyakori példák
1. **Új konténer indítása**:
   ```bash
   docker run hello-world
   ```
   Ez a parancs elindít egy új konténert a `hello-world` képből, amely egy egyszerű üzenetet jelenít meg.

2. **Futó konténerek listázása**:
   ```bash
   docker ps
   ```
   Ezzel a paranccsal megtekinthetjük az aktuálisan futó konténereket.

3. **Helyi képek listázása**:
   ```bash
   docker images
   ```
   Ez a parancs megmutatja az összes helyben tárolt Docker képet.

4. **Kép letöltése**:
   ```bash
   docker pull ubuntu
   ```
   Ezzel a paranccsal letöltjük az Ubuntu legfrissebb Docker képét.

5. **Konténer törlése**:
   ```bash
   docker rm my_container
   ```
   Ez a parancs törli a `my_container` nevű konténert.

## Tippek
- Mindig használj címkéket a képeidhez, hogy könnyebben nyomon követhesd a verziókat.
- Használj Docker Compose-t, ha több konténert szeretnél egyszerre kezelni.
- Rendszeresen frissítsd a Docker képeidet a legújabb biztonsági javítások érdekében.