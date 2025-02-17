# [Linux] Bash shift käyttö: Siirtää argumentteja vasemmalle

## Yleiskatsaus
`shift`-komento Bashissa siirtää argumentteja vasemmalle, mikä tarkoittaa, että se poistaa ensimmäisen argumentin ja siirtää kaikki jäljellä olevat argumentit yhden paikan vasemmalle. Tämä on hyödyllistä, kun käsitellään skriptejä, joissa argumentteja käsitellään yksi kerrallaan.

## Käyttö
Perussyntaksi `shift`-komennolle on seuraava:

```bash
shift [n]
```

Missä `n` on valinnainen argumentti, joka määrittää, kuinka monta paikkaa argumentteja siirretään. Oletusarvoisesti `n` on 1.

## Yleiset vaihtoehdot
- `n`: Määrittää, kuinka monta argumenttia siirretään. Esimerkiksi `shift 2` siirtää argumentteja kaksi paikkaa vasemmalle.

## Yleiset esimerkit

### Esimerkki 1: Perus siirto
```bash
#!/bin/bash
echo "Alkuperäiset argumentit: $@"
shift
echo "Siirron jälkeen: $@"
```
Tässä skriptissä ensimmäinen argumentti poistuu ja jäljelle jääneet argumentit tulostuvat.

### Esimerkki 2: Siirto useammalla paikalla
```bash
#!/bin/bash
echo "Alkuperäiset argumentit: $@"
shift 2
echo "Siirron jälkeen: $@"
```
Tässä esimerkissä ensimmäiset kaksi argumenttia poistuvat, ja tulostuvat vain jäljelle jääneet.

### Esimerkki 3: Argumenttien käsittely silmukassa
```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "Käsitellään argumenttia: $1"
    shift
done
```
Tässä skriptissä kaikki argumentit käsitellään yksi kerrallaan, kunnes niitä ei enää ole.

## Vinkit
- Käytä `shift`-komentoa yhdessä silmukoiden kanssa, jotta voit käsitellä useita argumentteja tehokkaasti.
- Varmista, että tarkistat argumenttien määrän ennen `shift`-komennon käyttöä, jotta vältät virheitä.
- Hyödynnä `shift`-komentoa skripteissä, joissa argumenttien järjestys on tärkeä, kuten komentosarjoissa, jotka käsittelevät useita syötteitä.