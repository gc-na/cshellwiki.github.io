# [Linux] Bash find käyttö: Tiedostojen etsiminen

## Yleiskatsaus
`find`-komento on tehokas työkalu, jota käytetään tiedostojen ja hakemistojen etsimiseen tiedostojärjestelmässä. Se mahdollistaa hakemisen monilla eri kriteereillä, kuten nimen, koon, muokkausajan ja muiden ominaisuuksien perusteella.

## Käyttö
Perussyntaksi `find`-komennolle on seuraava:

```bash
find [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-name`: Etsii tiedostoja, joiden nimi vastaa annettua mallia.
- `-type`: Rajaa haun tietyn tyyppisiin tiedostoihin, kuten `f` (tiedosto) tai `d` (hakemisto).
- `-size`: Etsii tiedostoja, joiden koko vastaa annettua arvoa.
- `-mtime`: Etsii tiedostoja, jotka on muutettu tietyn ajan sisällä.
- `-exec`: Suorittaa annetun komennon jokaiselle löydetylle tiedostolle.

## Yleiset esimerkit
Eri käyttötapojen havainnollistamiseksi tässä on muutama esimerkki:

### Etsi tiedosto nimeltä "esimerkki.txt"
```bash
find /polku/hakemistoon -name "esimerkki.txt"
```

### Etsi kaikki hakemistot
```bash
find /polku/hakemistoon -type d
```

### Etsi tiedostot, joiden koko on yli 1MB
```bash
find /polku/hakemistoon -size +1M
```

### Etsi tiedostot, jotka on muutettu viimeisen 7 päivän aikana
```bash
find /polku/hakemistoon -mtime -7
```

### Suorita komento jokaiselle löydetylle tiedostolle
```bash
find /polku/hakemistoon -name "*.log" -exec rm {} \;
```

## Vinkit
- Käytä `-iname` vaihtoehtoa, jos haluat tehdä hausta kirjainherkkää.
- Voit yhdistää useita ehtoja käyttämällä `-and` ja `-or` operaattoreita.
- Testaa ensin komento ilman `-exec`-vaihtoehtoa varmistaaksesi, että löydät oikeat tiedostot ennen kuin suoritat vaarallisia komentoja, kuten `rm`.