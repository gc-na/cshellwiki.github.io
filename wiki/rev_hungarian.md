# [Linux] Bash rev: A szöveg visszafordítása

## Áttekintés
A `rev` parancs a szöveg visszafordítására szolgál, karakterenként. Ez azt jelenti, hogy a bemeneti szöveg minden egyes sorát megfordítja, így az utolsó karakter az első helyre kerül.

## Használat
A `rev` parancs alapvető szintaxisa a következő:

```bash
rev [opciók] [argumentumok]
```

## Gyakori Opciók
- `-f`: A bemeneti fájlok megadása, ha nem a standard bemenetre szeretnénk olvasni.
- `-o`: Kimeneti fájl megadása, ha nem a standard kimenetre szeretnénk írni.

## Gyakori Példák
1. **Egyszerű szöveg visszafordítása a standard bemenetről:**
   ```bash
   echo "Hello World" | rev
   ```
   **Kimenet:**
   ```
   dlroW olleH
   ```

2. **Fájl tartalmának visszafordítása:**
   ```bash
   rev myfile.txt
   ```
   Ez a parancs megfordítja a `myfile.txt` fájl minden sorát.

3. **Fájl visszafordított tartalmának mentése egy új fájlba:**
   ```bash
   rev myfile.txt > reversed.txt
   ```
   Ez a parancs a `myfile.txt` fájl tartalmát megfordítja, és a kimenetet a `reversed.txt` fájlba menti.

4. **Több fájl visszafordítása:**
   ```bash
   rev file1.txt file2.txt
   ```
   Ez a parancs mindkét fájl tartalmát megfordítja, és a kimenetet a standard kimenetre írja.

## Tippek
- Használja a `rev` parancsot szkriptekben, ha szüksége van a szöveg visszafordítására, például jelszavak vagy titkosított üzenetek esetén.
- A `rev` parancs jól működik együtt más parancsokkal, például a `grep`-pel, ha először szűrni szeretné a bemenetet.
- Ellenőrizze a fájlok kódolását, hogy biztosítsa a megfelelő működést, különösen nem ASCII karakterek esetén.