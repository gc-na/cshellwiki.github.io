# [Linux] Bash date käyttö: Näyttää ja muokkaa päivämäärää ja aikaa

## Yleiskatsaus
`date`-komento Bashissa näyttää nykyisen päivämäärän ja ajan tai muokkaa niitä tiettyjen parametrien avulla. Tämä komento on hyödyllinen, kun halutaan tarkistaa järjestelmän aikaleima tai muuttaa aikavyöhykkeitä.

## Käyttö
Perussyntaksi `date`-komennolle on seuraava:

```
date [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `+FORMAT`: Määrittää tulostettavan päivämäärän ja ajan muodon.
- `-u`: Näyttää UTC-aikavyöhykkeen mukaisen päivämäärän ja ajan.
- `-d STRING`: Näyttää päivämäärän ja ajan, joka vastaa annettua merkkijonoa.
- `-s STRING`: Asettaa järjestelmän päivämäärän ja ajan annetun merkkijonon mukaan.

## Yleiset esimerkit
1. **Nykyisen päivämäärän ja ajan näyttäminen:**
   ```bash
   date
   ```

2. **Päivämäärän näyttäminen tietyssä muodossa:**
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

3. **UTC-aikavyöhykkeen näyttäminen:**
   ```bash
   date -u
   ```

4. **Tulevan päivämäärän näyttäminen:**
   ```bash
   date -d "next Friday"
   ```

5. **Järjestelmän päivämäärän ja ajan asettaminen:**
   ```bash
   sudo date -s "2023-10-01 12:00:00"
   ```

## Vinkit
- Käytä `man date` saadaksesi lisätietoja ja täydellisen käyttöohjeen.
- Muista, että järjestelmän päivämäärän ja ajan asettaminen vaatii yleensä pääkäyttäjän oikeudet.
- Voit tallentaa usein käytetyt päivämäärämuodot skripteihin helpottaaksesi työskentelyä.