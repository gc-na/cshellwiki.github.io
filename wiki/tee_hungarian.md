# [Linux] Bash tee használata: Kimenet másolása fájlokba

## Áttekintés
A `tee` parancs lehetővé teszi, hogy a parancsok kimenetét egyszerre több helyre irányítsuk, például a képernyőre és egy fájlba. Ez hasznos lehet, ha szeretnénk megtekinteni a kimenetet, miközben azt egy fájlba is mentjük.

## Használat
A `tee` parancs alapvető szintaxisa a következő:

```bash
tee [opciók] [fájlok]
```

## Gyakori opciók
- `-a`, `--append`: A kimenetet a fájl végéhez fűzi, ahelyett, hogy felülírná.
- `-i`, `--ignore-interrupts`: Figyelmen kívül hagyja a megszakításokat.
- `--help`: Megjeleníti a parancs használati útmutatóját.

## Gyakori példák
1. **Kimenet mentése egy fájlba:**
   ```bash
   echo "Hello, World!" | tee output.txt
   ```
   Ez a parancs a "Hello, World!" szöveget megjeleníti a képernyőn és elmenti az `output.txt` fájlba.

2. **Kimenet hozzáfűzése egy fájlhoz:**
   ```bash
   echo "Új sor" | tee -a output.txt
   ```
   Ez a parancs hozzáfűzi az "Új sor" szöveget az `output.txt` fájl végéhez.

3. **Több fájlba írás:**
   ```bash
   echo "Több fájlba" | tee file1.txt file2.txt
   ```
   Ez a parancs a "Több fájlba" szöveget megjeleníti a képernyőn, és elmenti mind a `file1.txt`, mind a `file2.txt` fájlokba.

## Tippek
- Használj `tee -a` opciót, ha nem szeretnéd felülírni a meglévő fájlokat.
- A `tee` parancsot gyakran használják csővezetékekben, hogy a parancsok kimenetét megőrizzék, miközben további feldolgozásra is átadják.
- Használj `--help` opciót, ha további információra van szükséged a `tee` parancs használatáról.