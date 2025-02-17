# [Linux] Bash yes használat: Folyamatos "igen" kimenet generálása

## Áttekintés
A `yes` parancs egy egyszerű eszköz, amely folyamatosan "igen" (vagy bármilyen megadott szöveget) kimenetet generál a standard kimenetre. Hasznos lehet olyan helyzetekben, amikor egy program folyamatos megerősítést vár.

## Használat
A `yes` parancs alapvető szintaxisa a következő:

```bash
yes [opciók] [argumentumok]
```

## Gyakori opciók
- `-n`: A megadott szöveg előtt nem ad hozzá új sort.
- `--help`: Megjeleníti a parancs súgóját.
- `--version`: Megjeleníti a verzióinformációt.

## Gyakori példák

1. **Alapértelmezett használat**: A `yes` parancs alapértelmezett működése az "igen" folyamatos kiírása.
   ```bash
   yes
   ```

2. **Más szöveg kiírása**: Megadhatunk bármilyen szöveget, amit folyamatosan szeretnénk kiíratni.
   ```bash
   yes "Hello, World!"
   ```

3. **Kombinálás más parancsokkal**: A `yes` parancsot más parancsokkal is kombinálhatjuk, például a `rm` parancs megerősítésekor.
   ```bash
   yes | rm -i *.tmp
   ```

4. **Kimenet korlátozása**: A kimenetet átirányíthatjuk egy fájlba.
   ```bash
   yes "Y" > responses.txt
   ```

## Tippek
- Használja a `yes` parancsot óvatosan, különösen destruktív parancsokkal, mint a `rm`, hogy elkerülje a véletlen adatvesztést.
- A `yes` parancs kimenete hatalmas lehet, ezért érdemes figyelni a kimenet irányítására, például fájlba írással.
- A `yes` parancs hasznos lehet automatizált tesztelés során, ahol folyamatos megerősítések szükségesek.