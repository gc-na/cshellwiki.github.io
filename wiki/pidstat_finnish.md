# [Linux] Bash pidstat käyttö: Prosessien tilan seuranta

## Yleiskatsaus
`pidstat` on komento, joka kuuluu `sysstat`-pakettiin ja sitä käytetään prosessien suorituskyvyn seurannassa. Se näyttää tietoja prosessien käyttöasteesta, kuten CPU:n ja muistin käytöstä, mikä auttaa järjestelmänvalvojia ja kehittäjiä optimoimaan sovellusten suorituskykyä.

## Käyttö
Perussyntaksi `pidstat`-komennolle on seuraava:

```bash
pidstat [options] [arguments]
```

## Yleiset vaihtoehdot
- `-h`: Näyttää ohjeen ja käytön.
- `-r`: Näyttää muistinkäytön tiedot.
- `-u`: Näyttää CPU:n käyttöasteen tiedot.
- `-p <pid>`: Seuraa tiettyä prosessia, jonka prosessitunnus (PID) on määritelty.
- `-t`: Näyttää tiedot kaikista säikeistä.

## Yleiset esimerkit
1. **Perustietojen näyttäminen kaikista prosesseista:**
   ```bash
   pidstat
   ```

2. **Seuraa tietyn prosessin CPU:n käyttöä (esim. PID 1234):**
   ```bash
   pidstat -p 1234
   ```

3. **Näytä muistinkäyttö kaikista prosesseista:**
   ```bash
   pidstat -r
   ```

4. **Seuraa prosessien käyttöä tietyllä aikavälillä (esim. 5 sekunnin välein):**
   ```bash
   pidstat 5
   ```

5. **Näytä tiedot kaikista säikeistä:**
   ```bash
   pidstat -t
   ```

## Vinkit
- Käytä `pidstat`-komentoa yhdessä muiden järjestelmänvalvontatyökalujen kanssa, kuten `top` tai `htop`, saadaksesi kattavamman kuvan järjestelmän suorituskyvystä.
- Voit ohjata `pidstat`-komennon tulosteet tiedostoon analysointia varten lisäämällä `> output.txt` komennon loppuun.
- Säännöllinen seuranta voi auttaa havaitsemaan suorituskykyongelmia ennen kuin ne vaikuttavat käyttäjiin.