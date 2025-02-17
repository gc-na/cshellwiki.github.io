# [Linux] Bash rm használat: Fájlok törlése

## Áttekintés
A `rm` parancs a Bash környezetben fájlok és könyvtárak törlésére szolgál. Használatával eltávolíthatjuk a nem kívánt fájlokat a rendszerünkből.

## Használat
A `rm` parancs alapvető szintaxisa a következő:

```bash
rm [opciók] [argumentumok]
```

## Gyakori Opciók
- `-f`: Kényszerített törlés, amely figyelmen kívül hagyja a nem létező fájlokat és nem kér megerősítést.
- `-i`: Interaktív mód, amely megerősítést kér minden egyes fájl törlése előtt.
- `-r`: Rekurzív törlés, amely lehetővé teszi könyvtárak és azok tartalmának törlését.
- `-v`: Verbózus mód, amely megjeleníti a törölt fájlok nevét.

## Gyakori Példák
1. **Egy fájl törlése:**
   ```bash
   rm pelda.txt
   ```

2. **Több fájl törlése:**
   ```bash
   rm pelda1.txt pelda2.txt
   ```

3. **Könyvtár és annak tartalmának törlése:**
   ```bash
   rm -r pelda_konyvtar
   ```

4. **Megerősítést kérve fájl törlése:**
   ```bash
   rm -i pelda.txt
   ```

5. **Kényszerített törlés:**
   ```bash
   rm -f pelda.txt
   ```

## Tippek
- Mindig ellenőrizd, hogy a törölni kívánt fájlok valóban nem szükségesek-e, mivel a törlés véglegesen eltávolítja őket.
- Használj `-i` opciót, ha nem vagy biztos a törlésben, hogy elkerüld a véletlen adatvesztést.
- Legyél óvatos a `-r` opcióval, különösen, ha rendszermappákat törölsz, mert ez súlyos problémákat okozhat a rendszer működésében.