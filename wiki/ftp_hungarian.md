# [Linux] Bash ftp használata: Fájlok átvitele FTP-n keresztül

## Áttekintés
Az `ftp` (File Transfer Protocol) parancs lehetővé teszi fájlok átvitelét a számítógép és egy távoli FTP szerver között. Az FTP egy elterjedt protokoll, amelyet fájlok feltöltésére és letöltésére használnak.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
ftp [opciók] [argumentumok]
```

## Gyakori Opciók
- `-i`: Kikapcsolja az interaktív módot, lehetővé téve a fájlok automatikus átvitelét.
- `-v`: Verbose (részletes) mód, amely megjeleníti az FTP parancsok kimenetét.
- `-n`: Megakadályozza az automatikus bejelentkezést a szerverre.
- `-p`: Passzív mód, amely segíthet a tűzfalakkal kapcsolatos problémák megoldásában.

## Gyakori Példák
1. **Kapcsolódás egy FTP szerverhez:**

```bash
ftp ftp.example.com
```

2. **Fájl letöltése a szerverről:**

```bash
get filename.txt
```

3. **Fájl feltöltése a szerverre:**

```bash
put filename.txt
```

4. **Fájlok listázása a szerveren:**

```bash
ls
```

5. **Kilépés az FTP-ből:**

```bash
bye
```

## Tippek
- Mindig ellenőrizd, hogy a megfelelő FTP szerverhez csatlakozol, és használd a megfelelő hitelesítési adatokat.
- Használj `-v` opciót a hibaelhárításhoz, ha problémák merülnek fel a fájlátvitel során.
- Ha lehetséges, használj biztonságosabb alternatívákat, mint például az SFTP, mivel az FTP nem titkosítja az adatokat.