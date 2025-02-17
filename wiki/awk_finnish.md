# [Linux] Bash awk käyttö: Tekstinkäsittelyyn tarkoitettu työkalu

## Yleiskatsaus
`awk` on tehokas tekstinkäsittelytyökalu, jota käytetään erityisesti tiedostojen analysoimiseen ja muokkaamiseen. Se mahdollistaa tietojen suodattamisen, muuntamisen ja raportoinnin helposti.

## Käyttö
Perussyntaksi `awk`-komennolle on seuraava:

```bash
awk [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-F`: Määrittää kenttäerottimen (esim. `-F,` tarkoittaa, että kentät erotetaan pilkulla).
- `-v`: Määrittää muuttujan, jota voidaan käyttää awk-ohjelmassa.
- `-f`: Lataa awk-ohjelman tiedostosta.

## Yleiset esimerkit

### Esimerkki 1: Kenttien tulostaminen
Tulostaa ensimmäisen ja toisen kentän tiedostosta `data.txt`, jossa kentät on erotettu välilyönneillä.

```bash
awk '{print $1, $2}' data.txt
```

### Esimerkki 2: Suodatus
Tulostaa vain ne rivit, joissa kolmas kenttä on suurempi kuin 100.

```bash
awk '$3 > 100' data.txt
```

### Esimerkki 3: Kenttäerottimen määrittäminen
Tulostaa ensimmäisen kentän CSV-tiedostosta, jossa kentät on erotettu pilkulla.

```bash
awk -F, '{print $1}' data.csv
```

### Esimerkki 4: Muuttujan käyttö
Laskee ja tulostaa kaikkien rivien summan toisen kentän arvoista.

```bash
awk -v sum=0 '{sum += $2} END {print sum}' data.txt
```

## Vinkit
- Käytä `-F`-vaihtoehtoa, kun työskentelet tiedostojen kanssa, joissa kentät on erotettu muulla kuin välilyönneillä.
- Hyödynnä `BEGIN` ja `END` -lohkot, jos haluat suorittaa koodia ennen tai jälkeen tiedostojen käsittelyn.
- Testaa komentoja ensin pienillä tiedostoilla varmistaaksesi, että saat haluamasi tulokset.