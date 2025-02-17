# [Linux] Bash iotop käyttö: Seuraa levy I/O-aktiviteettia

## Yleiskatsaus
`iotop` on komento, joka näyttää reaaliaikaisesti prosessien levy I/O-aktiviteetin. Se auttaa käyttäjiä tunnistamaan, mitkä prosessit kuluttavat eniten levyresursseja, mikä on erityisen hyödyllistä järjestelmän suorituskyvyn optimoinnissa.

## Käyttö
Perussyntaksi `iotop`-komennolle on seuraava:

```bash
iotop [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-o`, `--only`: Näyttää vain prosessit, jotka ovat tällä hetkellä aktiivisia levy I/O:ssa.
- `-b`, `--batch`: Suorittaa iotopin erätilassa, jolloin tuloste voidaan ohjata tiedostoon.
- `-n NUM`, `--iter NUM`: Määrittää, kuinka monta kertaa iotop toistaa tulosteen ennen lopettamista.
- `-p PID`, `--pid=PID`: Näyttää vain tietyn prosessin I/O-aktiviteetin, kun annetaan prosessin tunnus (PID).

## Yleiset esimerkit
1. **Peruskäyttö**: Näyttää kaikki prosessit ja niiden I/O-aktiviteetin.
   ```bash
   iotop
   ```

2. **Näytä vain aktiiviset prosessit**:
   ```bash
   iotop -o
   ```

3. **Erätilassa tulostaminen**: Suorita iotop erätilassa ja tallenna tuloste tiedostoon.
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. **Seuraa tiettyä prosessia**: Näytä vain tietyn prosessin I/O-aktiviteetti.
   ```bash
   iotop -p 1234
   ```

## Vinkit
- Käytä `iotop`-komentoa yhdessä muiden järjestelmänvalvontatyökalujen, kuten `top` tai `htop`, kanssa saadaksesi kattavamman kuvan järjestelmän suorituskyvystä.
- Suosittelemme suorittamaan `iotop`-komennon pääkäyttäjänä (root), jotta saat täydet oikeudet kaikkien prosessien näyttämiseen.
- Muista, että `iotop` voi vaatia `python`-kirjaston asennusta, joten varmista, että se on asennettu järjestelmääsi.