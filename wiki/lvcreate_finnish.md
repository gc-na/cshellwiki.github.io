# [Linux] Bash lvcreate käyttö: Loida loogisia levyjä

## Overview
`lvcreate` on komento, jota käytetään loogisten levyjen (Logical Volumes) luomiseen Linux-järjestelmissä, jotka käyttävät LVM:ää (Logical Volume Manager). Tämä komento mahdollistaa joustavan levytilan hallinnan ja dynaamisen levyjen luomisen.

## Usage
Perussyntaksi komennolle on seuraava:
```bash
lvcreate [options] [arguments]
```

## Common Options
- `-n, --name <name>`: Määrittää loogisen levyn nimen.
- `-L, --size <size>`: Määrittää loogisen levyn koon.
- `-l, --extents <number>`: Määrittää loogisen levyn koon extenteissä.
- `-C, --mirrors <number>`: Määrittää peilattujen loogisten levyjen määrän.
- `-Z, --zeroing <y|n>`: Määrittää, nollataanko looginen levy luomisen yhteydessä.

## Common Examples
### Esimerkki 1: Loogisen levyn luominen
Luo looginen levy nimeltä `data` koossa 10G:
```bash
lvcreate -n data -L 10G vg_name
```

### Esimerkki 2: Loogisen levyn luominen extenteissä
Luo looginen levy nimeltä `backup`, joka on 20 extenttiä:
```bash
lvcreate -n backup -l 20 vg_name
```

### Esimerkki 3: Peilattu looginen levy
Luo peilattu looginen levy nimeltä `mirror_data`:
```bash
lvcreate -n mirror_data -m 1 -L 15G vg_name
```

### Esimerkki 4: Loogisen levyn nollaaminen
Luo looginen levy nimeltä `secure_data` ja nollaa se:
```bash
lvcreate -n secure_data -L 5G -Z y vg_name
```

## Tips
- Varmista, että LVM on asennettu ja konfiguroitu oikein ennen `lvcreate`-komennon käyttöä.
- Käytä `lvdisplay`-komentoa tarkistaaksesi luotujen loogisten levyjen tiedot.
- Suunnittele loogisten levyjen koko ja määrä etukäteen, jotta levytilan käyttö on tehokasta.