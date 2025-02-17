# [Linux] Bash end käyttö: Lopettaa prosessit

## Overview
`end`-komento on Bash-komento, jota käytetään prosessien lopettamiseen. Se mahdollistaa käyttäjän sulkea tai keskeyttää käynnissä olevia ohjelmia tai prosesseja järjestelmässä.

## Usage
Perussyntaksi `end`-komennolle on seuraava:

```bash
end [options] [arguments]
```

## Common Options
- `-h`, `--help`: Näyttää ohjeet ja käytön.
- `-v`, `--version`: Näyttää versionumeron.
- `-p`, `--pid`: Määrittää prosessin tunnuksen (PID), joka halutaan lopettaa.

## Common Examples
1. **Yksittäisen prosessin lopettaminen PID:n mukaan:**
   ```bash
   end -p 1234
   ```
   Tämä komento lopettaa prosessin, jonka PID on 1234.

2. **Useiden prosessien lopettaminen:**
   ```bash
   end 1234 5678 91011
   ```
   Tässä komennossa lopetetaan useita prosesseja kerralla.

3. **Ohjelman lopettaminen nimellä:**
   ```bash
   end firefox
   ```
   Tämä komento sulkee kaikki Firefox-selaimen instanssit.

## Tips
- Varmista, että tiedät, mitä prosessia olet lopettamassa, jotta et vahingossa sulje tärkeitä ohjelmia.
- Käytä `end -h` saadaksesi lisätietoja ja vaihtoehtoja komennosta.
- Voit tarkistaa käynnissä olevat prosessit komennolla `ps aux` ennen `end`-komennon käyttöä.