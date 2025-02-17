# [Linux] Bash ps käyttö: Prosessien tarkastelu

## Yleiskatsaus
`ps`-komento on työkalu, jota käytetään prosessien tarkasteluun Unix- ja Linux-järjestelmissä. Se näyttää tietoja käynnissä olevista prosesseista, kuten niiden tunnisteet, tila ja resurssien käyttö.

## Käyttö
Perussyntaksi `ps`-komennolle on seuraava:

```bash
ps [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-e` tai `-A`: Näyttää kaikki prosessit.
- `-f`: Näyttää prosessit täydellisessä muodossa, mukaan lukien vanhempien prosessien tunnisteet.
- `-u [käyttäjä]`: Näyttää vain tietyn käyttäjän prosessit.
- `-aux`: Näyttää kaikki prosessit ja niiden tiedot.
- `--sort`: Järjestää tulokset tietyn kentän mukaan, kuten `pid` tai `rss`.

## Yleiset esimerkit

1. **Kaikkien prosessien näyttäminen:**
   ```bash
   ps -e
   ```

2. **Tietyn käyttäjän prosessien näyttäminen:**
   ```bash
   ps -u username
   ```

3. **Prosessien näyttäminen täydellisessä muodossa:**
   ```bash
   ps -ef
   ```

4. **Kaikkien prosessien näyttäminen ja järjestäminen muistin käytön mukaan:**
   ```bash
   ps aux --sort=-%mem
   ```

5. **Tietyn prosessin etsiminen:**
   ```bash
   ps -e | grep process_name
   ```

## Vinkit
- Käytä `ps aux` saadaksesi kattavan näkymän kaikista prosesseista ja niiden tilasta.
- Yhdistä `ps`-komento muihin komentoihin, kuten `grep`, suodataksesi tuloksia tarkemmin.
- Muista, että `ps` näyttää vain hetkellisiä tietoja prosesseista; käytä `top`-komentoa reaaliaikaisen seurannan varten.