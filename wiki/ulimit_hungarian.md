# [Linux] Bash ulimit használat: A rendszer erőforrásainak korlátozása

## Áttekintés
A `ulimit` parancs a Bash shellben lehetővé teszi a felhasználók számára, hogy korlátozzák a folyamatok által felhasználható rendszererőforrásokat. Ez segít megelőzni, hogy egyetlen folyamat túl sok erőforrást használjon, ami a rendszer instabilitásához vezethet.

## Használat
A `ulimit` parancs alapvető szintaxisa a következő:

```bash
ulimit [opciók] [argumentumok]
```

## Gyakori opciók
- `-a`: Megjeleníti az összes erőforrás-korlátozást.
- `-c`: Beállítja a core fájlok maximális méretét.
- `-d`: Beállítja a folyamat adatterületének maximális méretét.
- `-f`: Beállítja a fájlok maximális méretét.
- `-l`: Beállítja a maximális blokkolt memória méretét.
- `-m`: Beállítja a maximális fizikai memória méretét.
- `-n`: Beállítja a maximálisan nyitható fájlok számát.
- `-s`: Beállítja a stack méretét.
- `-t`: Beállítja a maximális futási időt másodpercben.
- `-u`: Beállítja a maximális folyamatok számát felhasználónként.

## Gyakori példák
1. Az összes erőforrás-korlátozás megjelenítése:
   ```bash
   ulimit -a
   ```

2. A maximálisan nyitható fájlok számának beállítása 2048-ra:
   ```bash
   ulimit -n 2048
   ```

3. A maximális memória méretének beállítása 1 GB-ra:
   ```bash
   ulimit -m 1000000
   ```

4. A core fájlok maximális méretének korlátozása 0-ra (core dump letiltása):
   ```bash
   ulimit -c 0
   ```

5. A maximális futási idő beállítása 60 másodpercre:
   ```bash
   ulimit -t 60
   ```

## Tippek
- Mindig ellenőrizd az aktuális korlátozásokat az `ulimit -a` paranccsal, mielőtt módosítanád őket.
- Használj magasabb korlátokat a fejlesztési környezetekben, de légy óvatos a termelési környezetekben, hogy elkerüld a rendszer túlterhelését.
- A `ulimit` beállításai a shell session-re vonatkoznak, így ha új shellt nyitsz, az alapértelmezett értékek érvényesek.