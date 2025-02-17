# [Linux] Bash iconv használata: Karakterkódok konvertálása

## Áttekintés
Az `iconv` parancs a karakterkódok közötti konvertálásra szolgál. Lehetővé teszi, hogy fájlokat vagy szövegeket különböző karakterkódolások között alakítsunk át, például UTF-8, ISO-8859-1, vagy Windows-1252.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
iconv [opciók] [argumentumok]
```

## Gyakori opciók
- `-f`: Megadja a forrás karakterkódolást.
- `-t`: Megadja a cél karakterkódolást.
- `-o`: Megadja a kimeneti fájl nevét.
- `-c`: Figyelmen kívül hagyja a nem konvertálható karaktereket.

## Gyakori példák

1. **Fájl konvertálása UTF-8-ról ISO-8859-1-re:**

```bash
iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
```

2. **Szöveg konvertálása közvetlenül a parancssorból:**

```bash
echo "Hello, világ!" | iconv -f UTF-8 -t ISO-8859-1
```

3. **Fájl konvertálása és a nem konvertálható karakterek figyelmen kívül hagyása:**

```bash
iconv -f UTF-8 -t ASCII//TRANSLIT -c input.txt -o output.txt
```

4. **Kimenet a standard kimenetre:**

```bash
iconv -f UTF-8 -t UTF-16 input.txt
```

## Tippek
- Mindig ellenőrizd a forrás és a cél karakterkódolást, hogy elkerüld a hibákat.
- Használj `-o` opciót a kimeneti fájl nevének megadásához, hogy ne írj felül véletlenül egy meglévő fájlt.
- A `-c` opció hasznos lehet, ha nem szeretnéd, hogy a nem konvertálható karakterek megjelenjenek a kimenetben.