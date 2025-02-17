# [Linux] Bash at: Ajasta komentoja

## Yleiskatsaus
`at`-komento on työkalu, jonka avulla voit ajoittaa komentoja tai skriptejä suoritettavaksi tiettynä ajankohtana tulevaisuudessa. Tämä on erityisen hyödyllistä, kun haluat suorittaa tehtäviä automaattisesti ilman, että sinun tarvitsee olla kirjautuneena sisään.

## Käyttö
Perussyntaksi `at`-komennolle on seuraava:

```bash
at [options] [arguments]
```

## Yleiset vaihtoehdot
- `-f` : Määrittää tiedoston, joka sisältää suoritettavat komennot.
- `-l` : Listaa kaikki ajoitetut tehtävät.
- `-d` : Poistaa ajoitetun tehtävän.
- `-q` : Määrittää jonon, johon tehtävä lisätään (esim. a, b, c).

## Yleiset esimerkit
1. Ajoita komento suoritettavaksi tänään klo 15:00:

   ```bash
   echo "Hello, World!" | at 15:00
   ```

2. Ajoita skripti suoritettavaksi huomenna klo 10:00:

   ```bash
   at 10:00 tomorrow -f /path/to/script.sh
   ```

3. Listaa kaikki ajoitetut tehtävät:

   ```bash
   at -l
   ```

4. Poista tietty ajoitettu tehtävä (esimerkiksi ID 5):

   ```bash
   at -d 5
   ```

## Vinkit
- Varmista, että käytät oikeaa aikamuotoa (esim. "now", "tomorrow", "HH:MM").
- Tarkista ajoitetut tehtävät säännöllisesti, jotta et unohda niitä.
- Käytä `atq`-komentoa, jos haluat nähdä vain omat ajoitetut tehtäväsi.