# [Linux] Bash free käyttö: Muistin käytön tarkastelu

## Yleiskatsaus
`free`-komento on työkalu, jota käytetään järjestelmän muistin käytön tarkasteluun. Se näyttää käytettävissä olevan muistin, käytetyn muistin ja välimuistin määrät, mikä auttaa käyttäjiä ymmärtämään järjestelmän muistiresursseja.

## Käyttö
Perussyntaksi `free`-komennolle on seuraava:

```bash
free [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h`: Näyttää muistimäärät ihmisen luettavassa muodossa (esim. KB, MB, GB).
- `-m`: Näyttää muistimäärät megatavuina.
- `-g`: Näyttää muistimäärät gigatavuina.
- `-s [sekunnit]`: Päivittää näyttöä tietyin aikavälein (esim. 5 sekunnin välein).
- `-t`: Näyttää yhteenvetotiedot käytetystä ja käytettävissä olevasta muistista.

## Yleiset esimerkit
1. **Perusmuistin tarkastelu:**
   ```bash
   free
   ```

2. **Muistin tarkastelu ihmisen luettavassa muodossa:**
   ```bash
   free -h
   ```

3. **Muistin tarkastelu megatavuina:**
   ```bash
   free -m
   ```

4. **Muistin tarkastelu gigatavuina:**
   ```bash
   free -g
   ```

5. **Muistin päivitys 5 sekunnin välein:**
   ```bash
   free -s 5
   ```

6. **Yhteenvetotietojen näyttäminen:**
   ```bash
   free -t
   ```

## Vinkit
- Käytä `-h`-vaihtoehtoa saadaksesi helposti luettavat muistimäärät, erityisesti suurilla järjestelmillä.
- Jos haluat seurata muistinkäyttöä reaaliaikaisesti, yhdistä `free`-komento `watch`-komentoon:
  ```bash
  watch free -h
  ```
- Muista, että `free`-komento näyttää vain RAM-muistin tilan, ei esimerkiksi swap-muistin tilaa, ellei sitä erikseen pyydetä.