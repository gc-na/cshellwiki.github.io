# [Linux] Bash test käyttö: testaa ehtoja ja tiedostoja

## Yleiskatsaus
`test`-komento on Bashin sisäinen komento, jota käytetään ehtojen arvioimiseen. Se voi tarkistaa, onko tiedosto olemassa, onko se luettavissa tai kirjoitettavissa, ja se voi myös arvioida erilaisia loogisia ja vertailuehtoja.

## Käyttö
Perussyntaksi `test`-komennolle on seuraava:

```bash
test [options] [arguments]
```

## Yleiset vaihtoehdot
- `-e`: Tarkistaa, onko tiedosto olemassa.
- `-f`: Tarkistaa, onko tiedosto tavallinen tiedosto.
- `-d`: Tarkistaa, onko tiedosto hakemisto.
- `-r`: Tarkistaa, onko tiedosto luettavissa.
- `-w`: Tarkistaa, onko tiedosto kirjoitettavissa.
- `-x`: Tarkistaa, onko tiedosto suoritettavissa.
- `=`: Vertaa kahta merkkijonoa.
- `-eq`: Tarkistaa, ovatko kaksi kokonaislukua yhtä suuret.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `test`-komennon käytöstä:

1. Tarkista, onko tiedosto olemassa:
   ```bash
   test -e /polku/tiedostoon.txt && echo "Tiedosto on olemassa."
   ```

2. Tarkista, onko tiedosto hakemisto:
   ```bash
   test -d /polku/hakemistoon && echo "Se on hakemisto."
   ```

3. Vertaa kahta merkkijonoa:
   ```bash
   test "abc" = "abc" && echo "Merkkijonot ovat samat."
   ```

4. Tarkista, onko tiedosto kirjoitettavissa:
   ```bash
   test -w /polku/tiedostoon.txt && echo "Tiedosto on kirjoitettavissa."
   ```

5. Tarkista, ovatko kaksi kokonaislukua yhtä suuret:
   ```bash
   a=5
   b=5
   test $a -eq $b && echo "Luvut ovat yhtä suuret."
   ```

## Vinkit
- Käytä `[`-merkkiä `test`-komennon sijasta, jolloin voit kirjoittaa ehtoja hieman luettavammassa muodossa, esimerkiksi: 
  ```bash
  [ -e /polku/tiedostoon.txt ] && echo "Tiedosto on olemassa."
  ```
  
- Muista, että ehtojen arvioinnissa on tärkeää käyttää oikeita välilyöntejä, jotta komento toimii oikein.

- Voit yhdistää useita ehtoja käyttämällä `&&` (JA) tai `||` (TAI) operaattoreita, mikä tekee skripteistäsi tehokkaampia.