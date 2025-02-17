# [Linux] Bash comm käyttö: vertaa kahta tiedostoa

## Yleiskatsaus
`comm`-komento on työkalu, joka vertaa kahta lajiteltua tiedostoa ja näyttää niiden yhteiset ja eroavat rivit. Tämä komento on erityisen hyödyllinen, kun halutaan analysoida kahta erilaista tietolähdettä ja nähdä, mitkä rivit ovat samoja tai eroavat toisistaan.

## Käyttö
Perussyntaksi `comm`-komennolle on seuraava:

```bash
comm [vaihtoehdot] [tiedosto1] [tiedosto2]
```

## Yleiset vaihtoehdot
- `-1`: Poistaa ensimmäisen sarakkeen (tiedosto1:n rivit).
- `-2`: Poistaa toisen sarakkeen (tiedosto2:n rivit).
- `-3`: Poistaa kolmannen sarakkeen (yhteiset rivit).
- `-i`: Huomioi isot ja pienet kirjaimet samana.
- `-d`: Näyttää vain rivit, jotka ovat molemmissa tiedostoissa.

## Yleiset esimerkit

### Esimerkki 1: Perusvertailu
Vertaa kahta tiedostoa ja näytä kaikki rivit.
```bash
comm tiedosto1.txt tiedosto2.txt
```

### Esimerkki 2: Poista ensimmäinen sarake
Näytä vain rivit, jotka löytyvät tiedostosta 2.
```bash
comm -13 tiedosto1.txt tiedosto2.txt
```

### Esimerkki 3: Huomioi isot ja pienet kirjaimet
Vertaa kahta tiedostoa siten, että isot ja pienet kirjaimet eivät vaikuta vertailuun.
```bash
comm -i tiedosto1.txt tiedosto2.txt
```

### Esimerkki 4: Näytä vain yhteiset rivit
Näytä vain rivit, jotka ovat molemmissa tiedostoissa.
```bash
comm -12 tiedosto1.txt tiedosto2.txt
```

## Vinkit
- Varmista, että tiedostot ovat lajiteltuja ennen `comm`-komennon käyttöä, sillä komento toimii vain lajitelluilla tiedostoilla.
- Käytä `sort`-komentoa tiedostojen lajitteluun ennen vertailua, jos et ole varma niiden järjestyksestä.
- Hyödynnä vaihtoehtoja yhdistämällä niitä tarpeidesi mukaan saadaksesi tarkempia tuloksia.