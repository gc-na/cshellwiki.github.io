# [Linux] Bash else käyttö: Ehdollinen suoritus

## Yleiskatsaus
`else`-komento Bashissa on osa ehtolauseita, joita käytetään ohjaamaan ohjelman suorituspolkua. Se mahdollistaa vaihtoehtoisten toimintojen määrittämisen, jos edellinen ehto ei täyty.

## Käyttö
Perussyntaksi `else`-komennolle on seuraava:
```bash
if [ ehto ]; then
    # Suorita tämä, jos ehto on tosi
else
    # Suorita tämä, jos ehto on epätosi
fi
```

## Yleiset vaihtoehdot
`else`-komennolla ei ole erityisiä vaihtoehtoja, mutta se käytetään yhdessä `if`-komennon kanssa. Tärkeimmät osat ovat:
- `if`: Määrittää ehdon, jota tarkastellaan.
- `then`: Ilmaisee, mitä tapahtuu, jos ehto on tosi.
- `fi`: Päättää ehtolauseen.

## Yleiset esimerkit

### Esimerkki 1: Yksinkertainen ehto
```bash
if [ -f "tiedosto.txt" ]; then
    echo "Tiedosto löytyy."
else
    echo "Tiedostoa ei löydy."
fi
```

### Esimerkki 2: Ehtojen yhdistäminen
```bash
if [ "$ikä" -ge 18 ]; then
    echo "Olet aikuinen."
else
    echo "Olet alaikäinen."
fi
```

### Esimerkki 3: Useita ehtoja
```bash
if [ "$sää" = "aurinkoinen" ]; then
    echo "Mennään ulos!"
else
    echo "Pysytään sisällä."
fi
```

## Vinkit
- Käytä selkeitä ja kuvaavia ehtoja, jotta koodisi on helposti ymmärrettävää.
- Muista sulkea ehtolause `fi`:llä, jotta Bash ymmärtää, missä ehtolause päättyy.
- Voit yhdistää `else`-komennon `elif`-komennon kanssa monimutkaisempien ehtojen käsittelemiseksi.