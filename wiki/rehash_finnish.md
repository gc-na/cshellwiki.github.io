# [Linux] Bash rehash käyttö: Komentojen välimuistin päivittäminen

## Yleiskatsaus
`rehash`-komento päivittää Bashin komentojen välimuistin. Tämä on erityisen hyödyllistä, kun olet lisännyt uusia suoritettavia tiedostoja tai muuttanut olemassa olevia, ja haluat varmistaa, että Bash tunnistaa nämä muutokset ilman, että sinun tarvitsee sulkea ja avata komentoriviä uudelleen.

## Käyttö
Perussyntaksi `rehash`-komennolle on seuraava:

```bash
rehash [options] [arguments]
```

## Yleiset vaihtoehdot
- **-p**: Päivittää vain polkuun liittyvän välimuistin.
- **-a**: Lisää kaikki suoritettavat tiedostot välimuistiin.

## Yleiset esimerkit
### Esimerkki 1: Välimuistin päivittäminen
Kun olet lisännyt uuden suoritettavan tiedoston hakemistoon, voit päivittää välimuistin seuraavasti:

```bash
rehash
```

### Esimerkki 2: Polkuvälimuistin päivittäminen
Jos haluat päivittää vain polkuun liittyvän välimuistin, käytä seuraavaa komentoa:

```bash
rehash -p
```

### Esimerkki 3: Kaikkien suoritettavien tiedostojen lisääminen
Jos olet lisännyt useita uusia suoritettavia tiedostoja ja haluat lisätä ne kaikki välimuistiin, käytä:

```bash
rehash -a
```

## Vinkit
- **Käytä säännöllisesti**: Muista käyttää `rehash`-komentoa aina, kun lisäät uusia komentoja tai muokkaat olemassa olevia.
- **Yhdistä muihin komentoihin**: Voit käyttää `rehash`-komentoa yhdessä muiden komentojen kanssa, kuten `cd`, varmistaaksesi, että uusi polku on käytettävissä.
- **Vältä tarpeetonta käyttöä**: Jos et ole tehnyt muutoksia suoritettaviin tiedostoihin, `rehash`-komennon käyttäminen ei ole tarpeen, ja se voi hidastaa komentorivin toimintaa.