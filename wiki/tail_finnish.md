# [Linux] Bash tail käyttö: Näyttää tiedoston loppuosan

## Yleiskatsaus
`tail`-komento on Bash-komento, jota käytetään tiedostojen loppuosan näyttämiseen. Se on erityisen hyödyllinen suurten lokitiedostojen tarkastelussa, jolloin käyttäjä voi nähdä vain viimeiset rivit ilman, että koko tiedostoa tarvitsee avata.

## Käyttö
Perussyntaksi `tail`-komennolle on seuraava:

```bash
tail [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-n [numero]`: Määrittää näytettävien rivien määrän. Oletusarvoisesti näytetään 10 viimeistä riviä.
- `-f`: Seuraa tiedostoa reaaliaikaisesti, jolloin uudet rivit näkyvät heti, kun niitä lisätään tiedostoon.
- `-c [tavua]`: Näyttää tiedoston loppuosan tietyllä tavumäärällä.

## Yleiset esimerkit
1. Näytä 10 viimeistä riviä tiedostosta:
   ```bash
   tail tiedosto.txt
   ```

2. Näytä 20 viimeistä riviä tiedostosta:
   ```bash
   tail -n 20 tiedosto.txt
   ```

3. Seuraa lokitiedostoa reaaliaikaisesti:
   ```bash
   tail -f loki.log
   ```

4. Näytä tiedoston loppu 100 tavua:
   ```bash
   tail -c 100 tiedosto.txt
   ```

## Vinkit
- Käytä `-f`-vaihtoehtoa lokitiedostojen tarkastelussa, jotta pysyt ajan tasalla uusista tapahtumista.
- Voit yhdistää `tail`-komennon muihin komentoihin, kuten `grep`, suodattaaksesi vain tietyt rivit.
- Muista, että `tail`-komento ei muokkaa tiedostoa, vaan vain näyttää sen sisältöä.