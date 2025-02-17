# [Linux] Bash stty käyttö: Muokkaa terminaalin asetuksia

## Yleiskatsaus
`stty`-komento on työkalu, jota käytetään terminaalin asetusten muokkaamiseen. Sen avulla voit säätää erilaisia syöttö- ja tulostusasetuksia, kuten näppäinkomentoja ja merkkien käsittelyä.

## Käyttö
Perussyntaksi `stty`-komennolle on seuraava:

```bash
stty [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a`: Näyttää kaikki asetukset.
- `-g`: Tulostaa asetukset muodossa, jota voidaan käyttää myöhemmin.
- `erase`: Määrittää poistomerkin.
- `kill`: Määrittää tappomerkin.
- `intr`: Määrittää keskeytysmerkin.

## Yleiset esimerkit
1. **Näytä kaikki asetukset:**
   ```bash
   stty -a
   ```

2. **Määritä poistomerkiksi Backspace:**
   ```bash
   stty erase ^H
   ```

3. **Määritä keskeytysmerkiksi Ctrl+C:**
   ```bash
   stty intr ^C
   ```

4. **Tallenna nykyiset asetukset tiedostoon:**
   ```bash
   stty -g > asetukset.txt
   ```

5. **Palauta asetukset tiedostosta:**
   ```bash
   stty $(<asetukset.txt)
   ```

## Vinkit
- Käytä `stty -a` -komentoa tarkistaaksesi nykyiset asetukset ennen muutoksia.
- Muista, että muutokset ovat voimassa vain nykyisessä terminaalissa; ne eivät vaikuta muihin istuntoihin.
- Voit käyttää `stty`-komentoa yhdessä skriptien kanssa automatisoidaksesi terminaalimuutoksia.