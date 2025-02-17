# [Linux] Bash umask használat: A fájlok alapértelmezett jogosultságainak beállítása

## Áttekintés
A `umask` parancs a fájlok és könyvtárak alapértelmezett jogosultságainak beállítására szolgál a Unix-alapú operációs rendszerekben. A parancs segítségével meghatározhatjuk, hogy új fájlok és könyvtárak milyen jogosultságokkal jöjjenek létre.

## Használat
A `umask` parancs alapvető szintaxisa a következő:

```bash
umask [opciók] [érvek]
```

## Gyakori opciók
- `-S`: A jogosultságok szimbolikus formában való megjelenítése.
- `-p`: A jelenlegi umask értékének megjelenítése.

## Gyakori példák
1. **Jelenlegi umask érték megjelenítése:**
   ```bash
   umask
   ```

2. **Umask érték beállítása:**
   Például, ha azt szeretnénk, hogy az új fájlok alapértelmezett jogosultsága 664 legyen:
   ```bash
   umask 002
   ```

3. **Szimbolikus umask megjelenítése:**
   ```bash
   umask -S
   ```

4. **Umask érték visszaállítása alapértelmezett értékre:**
   ```bash
   umask 022
   ```

## Tippek
- Mindig ellenőrizd a `umask` értékét, mielőtt új fájlokat hozol létre, hogy biztos lehess benne, hogy a kívánt jogosultságokkal rendelkeznek.
- A `umask` beállításokat a shell indító fájlokban (pl. `.bashrc`, `.bash_profile`) is megadhatod, hogy a beállítások minden új shell indításakor érvényesüljenek.
- Használj szimbolikus formát a jogosultságok megértéséhez, mivel ez könnyebben érthető lehet, mint a numerikus értékek.