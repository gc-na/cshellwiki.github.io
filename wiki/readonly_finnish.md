# [Linux] Bash readonly käyttö: Muuttumattomien muuttujien määrittäminen

## Yleiskatsaus
`readonly`-komento Bashissa määrittää muuttujan, jota ei voi muuttaa tai poistaa sen määrittämisen jälkeen. Tämä on hyödyllistä, kun halutaan estää vahingossa tapahtuva muuttujan muokkaaminen tai poistaminen skriptin aikana.

## Käyttö
Perussyntaksi `readonly`-komennolle on seuraava:

```bash
readonly [options] [arguments]
```

## Yleiset vaihtoehdot
- `-p`: Tulostaa kaikki tällä hetkellä määritellyt readonly-muuttujat.

## Yleiset esimerkit

### Esimerkki 1: Muuttujan määrittäminen readonly-tilaan
```bash
myvar="Tämä on muuttuja"
readonly myvar
```
Tässä esimerkissä `myvar`-muuttuja määritellään readonly-tilaan, joten sen arvoa ei voi muuttaa myöhemmin.

### Esimerkki 2: Yritetään muuttaa readonly-muuttujaa
```bash
myvar="Tämä on muuttuja"
readonly myvar
myvar="Uusi arvo"  # Tämä aiheuttaa virheen
```
Yllä oleva komento aiheuttaa virheen, koska yritämme muuttaa readonly-muuttujaa.

### Esimerkki 3: Kaikkien readonly-muuttujien näyttäminen
```bash
readonly -p
```
Tämä komento tulostaa kaikki tällä hetkellä määritellyt readonly-muuttujat ja niiden arvot.

## Vinkit
- Käytä `readonly`-komentoa tärkeiden muuttujien suojaamiseen skripteissä, jotta vältät vahingossa tapahtuvat muutokset.
- Muista, että `readonly`-muuttujat ovat vain nykyisessä Bash-istunnossa voimassa. Jos avaat uuden istunnon, muuttujat on määritettävä uudelleen.
- Hyvä käytäntö on määrittää kaikki tärkeät muuttujat readonly-tilaan heti niiden määrittämisen jälkeen, jotta niiden arvojen muuttaminen estetään.