# [Linux] Bash history käyttö: Komentohistorian näyttäminen

## Yleiskatsaus
`history`-komento Bashissa näyttää käyttäjän komentohistorian. Se auttaa käyttäjiä tarkastelemaan aiemmin syötettyjä komentoja, mikä voi olla hyödyllistä toistuvien tehtävien suorittamisessa tai virheiden korjaamisessa.

## Käyttö
Perussyntaksi `history`-komennolle on seuraava:

```bash
history [options] [arguments]
```

## Yleiset vaihtoehdot
- `-c`: Tyhjentää komentohistorian.
- `-d offset`: Poistaa historian rivin, jonka numero on `offset`.
- `n`: Näyttää vain viimeiset `n` komentoa historiasta.

## Yleiset esimerkit
1. **Näytä koko komentohistoria**:
   ```bash
   history
   ```

2. **Näytä viimeiset 10 komentoa**:
   ```bash
   history 10
   ```

3. **Poista tietty komento historiasta** (esim. rivin 5 poistaminen):
   ```bash
   history -d 5
   ```

4. **Tyhjennä koko komentohistoria**:
   ```bash
   history -c
   ```

## Vinkit
- Voit käyttää nuolinäppäimiä ylös ja alas selataksesi komentohistoriaasi nopeasti.
- Voit suorittaa aiemmin käytetyn komennon uudelleen kirjoittamalla sen numeron, esimerkiksi `!42` suorittaa historian rivin 42.
- Hyödynnä `grep`-komentoa etsiäksesi tiettyjä komentoja historiasta, esimerkiksi `history | grep "git"` löytää kaikki git-komennot.