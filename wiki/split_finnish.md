# [Linux] Bash split käyttö: Tiedostojen jakaminen pienempiin osiin

## Yleiskatsaus
`split`-komento Bashissa jakaa suuria tiedostoja pienempiin osiin. Tämä on erityisen hyödyllistä, kun haluat käsitellä suuria tiedostoja tai siirtää niitä helpommin.

## Käyttö
Perussyntaksi `split`-komennolle on seuraava:

```bash
split [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l N`: Jakaa tiedoston N rivin mukaan.
- `-b N`: Jakaa tiedoston N tavun mukaan.
- `-d`: Käyttää numeroita tiedostojen nimissä.
- `--additional-suffix=S`: Lisää määritellyn päätteetiedoston nimeen.

## Yleiset esimerkit
Jakaminen rivien mukaan:

```bash
split -l 100 suuri_tiedosto.txt
```

Jakaminen tavujen mukaan:

```bash
split -b 1M suuri_tiedosto.bin
```

Jakaminen ja numeroiden käyttö tiedostojen nimissä:

```bash
split -d -l 50 suuri_tiedosto.txt osa_
```

Lisäämällä päätteetiedoston nimeen:

```bash
split --additional-suffix=.txt -l 10 suuri_tiedosto.txt osa_
```

## Vinkit
- Käytä `-d`-vaihtoehtoa, jos haluat helpommin järjestettävät tiedostot numeroilla.
- Tarkista jakamisen jälkeen tiedostojen koko varmistaaksesi, että ne ovat oikean kokoisia.
- Voit käyttää `cat`-komentoa yhdistääksesi jakamasi tiedostot takaisin alkuperäiseen muotoon.