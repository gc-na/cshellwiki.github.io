# [Linux] Bash endif käyttö: Ehtolauseiden päättäminen

## Yleiskatsaus
`endif`-komento on osa Bashin ohjelmointirakennetta, jota käytetään ehtolauseiden päättämiseen. Se on erityisen hyödyllinen, kun käytetään `if`-lausetta, joka mahdollistaa ehtojen tarkistamisen ja erilaisten toimintojen suorittamisen niiden perusteella.

## Käyttö
Perussyntaksi `endif`-komennolle on seuraava:

```bash
endif
```

## Yleiset vaihtoehdot
`endif`-komennolla ei ole erityisiä vaihtoehtoja, koska se toimii vain ehtolauseiden päättämisessä. Se tulee aina `if`-lausetta seuraavaksi.

## Yleiset esimerkit

### Esimerkki 1: Yksinkertainen ehtolause
```bash
if [ "$a" -lt 10 ]; then
    echo "A on pienempi kuin 10"
endif
```

### Esimerkki 2: Monimutkaisempi ehtolause
```bash
if [ "$b" -eq 5 ]; then
    echo "B on viisi"
else
    echo "B ei ole viisi"
endif
```

### Esimerkki 3: Useita ehtoja
```bash
if [ "$c" -gt 0 ]; then
    echo "C on positiivinen"
elif [ "$c" -lt 0 ]; then
    echo "C on negatiivinen"
else
    echo "C on nolla"
endif
```

## Vinkit
- Varmista, että `endif`-komento on aina `if`-lausetta seuraava, jotta skripti toimii oikein.
- Käytä sisennystä ja selkeitä kommentteja koodissasi, jotta ehtolauseet ovat helpommin luettavissa.
- Testaa ehtolauseet huolellisesti, jotta voit varmistaa, että kaikki mahdolliset polut on katettu.