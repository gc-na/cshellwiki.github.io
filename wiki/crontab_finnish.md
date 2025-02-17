# [Linux] Bash crontab käyttö: Aikatauluta komentoja

## Yleiskatsaus
Crontab on työkalu, jota käytetään aikatauluttamaan komentoja tai skriptejä suoritettavaksi tietyin aikavälein Linux- ja Unix-järjestelmissä. Se mahdollistaa automaattisten tehtävien suorittamisen ilman käyttäjän jatkuvaa valvontaa.

## Käyttö
Perussyntaksi crontab-komennolle on seuraava:

```bash
crontab [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-e`: Muokkaa nykyistä crontab-tiedostoa.
- `-l`: Listaa käyttäjän nykyiset crontab-tehtävät.
- `-r`: Poistaa nykyisen crontab-tiedoston.
- `-i`: Vahvista poisto ennen kuin poistat crontab-tiedoston.

## Yleiset esimerkit
### 1. Aikatauluta komento joka päivä klo 2:00
```bash
0 2 * * * /polku/komento
```

### 2. Aikatauluta skripti joka maanantai klo 5:30
```bash
30 5 * * 1 /polku/skripti.sh
```

### 3. Aikatauluta komento joka 15. minuutti
```bash
*/15 * * * * /polku/komento
```

### 4. Aikatauluta komento joka kuukauden ensimmäinen päivä klo 12:00
```bash
0 12 1 * * /polku/komento
```

## Vinkit
- Varmista, että komennot tai skriptit, joita aikataulutat, ovat suoritettavissa ja niillä on tarvittavat käyttöoikeudet.
- Käytä `>> /polku/loki.txt 2>&1` komennon lopussa ohjataksesi tulosteet lokitiedostoon, jotta voit seurata suorituksia.
- Testaa komentoasi manuaalisesti ennen aikatauluttamista varmistaaksesi, että se toimii odotetusti.