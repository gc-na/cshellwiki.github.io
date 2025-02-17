# [Linux] Bash wc käyttö: Laskentatyökalu tiedostojen rivien, sanojen ja merkkien määrälle

## Yleiskatsaus
`wc` (word count) on Bash-komento, joka laskee tiedostojen rivien, sanojen ja merkkien määrän. Se on hyödyllinen työkalu tekstipohjaisten tietojen analysoimiseen ja tilastointiin.

## Käyttö
Perussyntaksi `wc`-komennolle on seuraava:

```bash
wc [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Laskee vain rivien määrän.
- `-w`: Laskee vain sanojen määrän.
- `-c`: Laskee vain merkkien määrän.
- `-m`: Laskee merkkien määrän (UTF-8).
- `-L`: Näyttää pisimmän rivin pituuden.

## Yleiset esimerkit
1. Rivien laskeminen tiedostossa:
   ```bash
   wc -l tiedosto.txt
   ```

2. Sanojen laskeminen tiedostossa:
   ```bash
   wc -w tiedosto.txt
   ```

3. Merkkien laskeminen tiedostossa:
   ```bash
   wc -c tiedosto.txt
   ```

4. Useiden tiedostojen rivien, sanojen ja merkkien laskeminen:
   ```bash
   wc tiedosto1.txt tiedosto2.txt
   ```

5. Pisimmän rivin pituuden näyttäminen:
   ```bash
   wc -L tiedosto.txt
   ```

## Vinkit
- Voit yhdistää `wc`-komennon muihin komentoihin, kuten `cat`, putkittamalla tuloksia. Esimerkiksi:
  ```bash
  cat tiedosto.txt | wc -l
  ```
- Käytä `-h`-vaihtoehtoa saadaksesi tulokset ihmislukuisessa muodossa, mikä tekee suurista tiedostoista helpommin luettavia.
- Muista, että `wc` voi käsitellä useita tiedostoja kerralla, mikä säästää aikaa, kun haluat analysoida useita tiedostoja samanaikaisesti.