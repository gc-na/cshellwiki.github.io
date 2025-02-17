# [Linux] Bash iconv käyttö: Merkkikoodien muuntaminen

## Yleiskatsaus
`iconv`-komento on työkalu, jota käytetään merkkikoodien muuntamiseen eri formaattien välillä. Se mahdollistaa tekstin muuntamisen yhdestä merkistöstä toiseen, mikä on erityisen hyödyllistä, kun työskennellään eri kielten ja järjestelmien kanssa.

## Käyttö
Perussyntaksi `iconv`-komennolle on seuraava:

```bash
iconv [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-f, --from-code=KODI`: Määrittää alkuperäisen merkkikoodauksen.
- `-t, --to-code=KODI`: Määrittää kohdemerkkikoodauksen.
- `-o, --output=TIEDOSTO`: Määrittää tulostiedoston nimen.
- `-l, --list`: Listaa kaikki tuetut merkkikoodaukset.

## Yleiset esimerkit
### Esimerkki 1: Tekstin muuntaminen UTF-8:sta ISO-8859-1:een
```bash
iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
```

### Esimerkki 2: Merkkikoodauksen tarkistaminen
```bash
iconv -l
```

### Esimerkki 3: Muuntaminen ilman tulostustiedostoa
```bash
iconv -f UTF-8 -t UTF-16 input.txt
```

### Esimerkki 4: Virheiden ohittaminen
```bash
iconv -f UTF-8 -t ISO-8859-1//IGNORE input.txt -o output.txt
```

## Vinkit
- Varmista, että tiedät alkuperäisen ja kohdemerkkikoodauksen ennen muuntamista.
- Käytä `-o`-vaihtoehtoa, jos et halua ylikirjoittaa alkuperäistä tiedostoa.
- Testaa muunnos ensin pienellä tiedostolla varmistaaksesi, että se toimii odotetusti.