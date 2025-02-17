# [Linux] Bash exit használat: A shell kilépési parancsa

## Áttekintés
Az `exit` parancs a Bash shell-ben a parancssor vagy a szkript végén használatos, hogy kilépjen a shell-ből vagy a szkriptből. A parancs visszaad egy kilépési kódot, amely jelzi a végrehajtás sikerességét vagy hibáját.

## Használat
A `exit` parancs alapvető szintaxisa a következő:

```bash
exit [opciók] [érvek]
```

## Gyakori Opciók
- **`n`**: A kilépési kód, amelyet a shell vagy a szkript visszaad. Alapértelmezett érték 0, ami a sikeres végrehajtást jelzi.

## Gyakori Példák

1. **Kilépés alapértelmezett kóddal:**
   ```bash
   exit
   ```

2. **Kilépés egy adott kóddal:**
   ```bash
   exit 1
   ```

3. **Kilépés egy szkriptből:**
   ```bash
   #!/bin/bash
   echo "A szkript futása befejeződött."
   exit 0
   ```

4. **Kilépés hiba esetén:**
   ```bash
   if [ ! -f "file.txt" ]; then
       echo "A fájl nem található!"
       exit 1
   fi
   ```

## Tippek
- Mindig használj egyértelmű kilépési kódokat, hogy mások (vagy te magad a jövőben) könnyen megértsék a szkript állapotát.
- A 0-ás kód a sikeres végrehajtást jelzi, míg a 1 vagy nagyobb számok általában hibát jeleznek.
- Használj `exit` parancsot a szkriptek végén, hogy biztosítsd a megfelelő kilépést és a kódok visszaadását.