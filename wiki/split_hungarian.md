# [Linux] Bash split használata: Fájlok darabolása

## Áttekintés
A `split` parancs lehetővé teszi fájlok darabolását kisebb részekre. Ezt általában nagy fájlok kezelésekor használják, hogy könnyebben kezelhető méretű darabokra bontsák őket.

## Használat
A `split` parancs alapvető szintaxisa a következő:

```bash
split [opciók] [argumentumok]
```

## Gyakori opciók
- `-l [szám]`: A fájlt sorok szerint darabolja, a megadott számú soronként.
- `-b [méret]`: A fájlt bájtok szerint darabolja, a megadott méretű részekre.
- `-d`: Számozott kiterjesztéseket használ a kimeneti fájlokhoz.
- `--additional-suffix=[kiterjesztés]`: Kiterjesztést ad a kimeneti fájlokhoz.

## Gyakori példák
1. Fájl darabolása 100 soronként:
   ```bash
   split -l 100 nagyfajl.txt
   ```

2. Fájl darabolása 1 MB-os részekre:
   ```bash
   split -b 1M nagyfajl.txt
   ```

3. Számozott kiterjesztésekkel való darabolás:
   ```bash
   split -d -l 50 nagyfajl.txt darab_
   ```

4. Kiterjesztés hozzáadása a kimeneti fájlokhoz:
   ```bash
   split --additional-suffix=.txt -l 10 nagyfajl.txt darab_
   ```

## Tippek
- Mindig ellenőrizd a kimeneti fájlok nevét, hogy elkerüld a felülírást.
- Használj megfelelő méretet a daraboláshoz, hogy a fájlok kezelhetőek maradjanak.
- A `split` parancsot gyakran használják más parancsokkal együtt, például a `cat`-tel a fájlok visszaállításához.