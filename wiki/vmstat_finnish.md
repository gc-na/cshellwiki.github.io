# [Linux] Bash vmstat käyttö: Järjestelmän suorituskyvyn seuranta

## Yleiskatsaus
`vmstat` (virtuaalimuistin tila) on komento, joka näyttää tietoja järjestelmän suorituskyvystä, mukaan lukien muistin käyttö, prosessorin kuormitus ja I/O-toiminnot. Se auttaa käyttäjiä ymmärtämään järjestelmän tilaa ja tunnistamaan mahdollisia ongelmia.

## Käyttö
Perussyntaksi `vmstat`-komennolle on seuraava:

```bash
vmstat [options] [arguments]
```

## Yleiset vaihtoehdot
- `-a`: Näyttää kaikki muistin käytön tiedot, mukaan lukien vapaa ja käytössä oleva muisti.
- `-n`: Estää tulostamasta otsikkorivejä jokaisella tulostuskerralla.
- `-s`: Näyttää muistin käytön tilastot yksityiskohtaisessa muodossa.
- `-t`: Näyttää aikaleiman jokaisessa tulostuksessa.

## Yleiset esimerkit
1. Näytä järjestelmän suorituskyky 5 sekunnin välein:
   ```bash
   vmstat 5
   ```

2. Näytä muistin käyttö yksityiskohtaisesti:
   ```bash
   vmstat -a
   ```

3. Näytä tilastot ilman otsikoita:
   ```bash
   vmstat -n 5
   ```

4. Näytä muistin käytön tilastot:
   ```bash
   vmstat -s
   ```

5. Näytä aikaleima jokaisessa tulostuksessa:
   ```bash
   vmstat -t 5
   ```

## Vinkit
- Käytä `vmstat`-komentoa yhdessä muiden työkalujen, kuten `top` tai `htop`, kanssa saadaksesi kattavamman kuvan järjestelmän suorituskyvystä.
- Seuraa `vmstat`-tuloksia säännöllisesti, jotta voit tunnistaa suorituskykyongelmia ennen kuin ne vaikuttavat järjestelmän toimintaan.
- Muista, että `vmstat`-komento näyttää tilastot vain tietyn ajan, joten käytä sitä yhdessä aikarajojen kanssa saadaksesi jatkuvaa seurantaa.