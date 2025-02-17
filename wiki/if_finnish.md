# [Linux] Bash if käyttö: Ehtojen tarkistaminen

## Yleiskatsaus
`if`-komento Bashissa on käytössä ehtojen tarkistamiseen. Se mahdollistaa erilaisten toimintojen suorittamisen sen mukaan, onko tietty ehto tosi vai epätosi. Tämä on hyödyllistä skriptien kirjoittamisessa, jossa halutaan suorittaa komentoja vain tietyissä olosuhteissa.

## Käyttö
Perussyntaksi `if`-komennolle on seuraava:

```bash
if [ehto]; then
    komento
fi
```

## Yleiset vaihtoehdot
- `-e`: Tarkistaa, onko tiedosto olemassa.
- `-d`: Tarkistaa, onko tiedosto hakemisto.
- `-f`: Tarkistaa, onko tiedosto tavallinen tiedosto.
- `-z`: Tarkistaa, onko merkkijono tyhjö.
- `-n`: Tarkistaa, onko merkkijono ei-tyhjö.

## Yleiset esimerkit

### Esimerkki 1: Tiedoston olemassaolon tarkistus
```bash
if [ -e "tiedosto.txt" ]; then
    echo "Tiedosto löytyy."
else
    echo "Tiedostoa ei löydy."
fi
```

### Esimerkki 2: Hakemiston tarkistus
```bash
if [ -d "hakemisto" ]; then
    echo "Hakemisto on olemassa."
else
    echo "Hakemistoa ei löydy."
fi
```

### Esimerkki 3: Merkkijonon tarkistus
```bash
merkkijono="Hello"
if [ -n "$merkkijono" ]; then
    echo "Merkkijono ei ole tyhjö."
else
    echo "Merkkijono on tyhjö."
fi
```

## Vinkit
- Muista käyttää välilyöntejä ehtojen ympärillä, kuten `if [ ehto ]`.
- Voit yhdistää useita ehtoja käyttämällä `&&` (JA) tai `||` (TAI) operaattoreita.
- Käytä `elif`-lausetta lisäehtojen tarkistamiseen ilman, että sinun tarvitsee kirjoittaa useita `if`-lausuntoja.