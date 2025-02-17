# [Linux] Bash sftp használata: Fájlok biztonságos átvitele

## Áttekintés
Az `sftp` (SSH File Transfer Protocol) egy biztonságos fájlátviteli protokoll, amely lehetővé teszi fájlok átvitelét egy távoli szerverre vagy onnan. Az `sftp` parancs az SSH protokollt használja a biztonságos kapcsolat létrehozásához, így ideális választás érzékeny adatok kezelésére.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
sftp [opciók] [felhasználónév@]szerver
```

## Gyakori opciók
- `-P`: A port megadása, amelyen a szerver elérhető.
- `-i`: Az SSH kulcsfájl megadása a hitelesítéshez.
- `-o`: További SSH opciók megadása.

## Gyakori példák
1. **Kapcsolódás egy távoli szerverhez:**
   ```bash
   sftp user@hostname
   ```

2. **Fájl feltöltése a távoli szerverre:**
   ```bash
   sftp user@hostname
   put helyi_fájl.txt
   ```

3. **Fájl letöltése a távoli szerverről:**
   ```bash
   sftp user@hostname
   get távoli_fájl.txt
   ```

4. **Mappa listázása a távoli szerveren:**
   ```bash
   sftp user@hostname
   ls
   ```

5. **Fájl törlése a távoli szerveren:**
   ```bash
   sftp user@hostname
   rm távoli_fájl.txt
   ```

## Tippek
- Mindig használj SSH kulcsokat a jelszavak helyett a biztonság növelése érdekében.
- Ellenőrizd a fájlok integritását a `md5sum` vagy `sha256sum` parancsokkal a fájlok átvitele előtt és után.
- Használj `-P` opciót, ha a távoli szerver nem az alapértelmezett 22-es portot használja.