# [Linux] Bash chage käyttö: Muuttaa käyttäjätilin salasanojen voimassaoloaikoja

## Overview
`chage`-komento on työkalu, jota käytetään käyttäjätilien salasanojen voimassaoloajan hallintaan Linux-järjestelmissä. Sen avulla voit määrittää, kuinka usein käyttäjän on vaihdettava salasana, sekä muita salasanoihin liittyviä asetuksia.

## Usage
Perussyntaksi `chage`-komennolle on seuraava:

```bash
chage [options] [arguments]
```

## Common Options
- `-l, --list`: Näyttää käyttäjän salasanan voimassaoloasetukset.
- `-m, --mindays DAYS`: Määrittää minimipäivien määrän, joka on kuluttava ennen kuin salasana voidaan vaihtaa.
- `-M, --maxdays DAYS`: Määrittää maksimi päivien määrän, jonka jälkeen salasana on vaihdettava.
- `-I, --inactive DAYS`: Määrittää päivien määrän, jonka jälkeen tili tulee inaktiiviseksi, jos salasanaa ei ole vaihdettu.
- `-E, --expiredate DATE`: Määrittää päivämäärän, jolloin tili vanhenee.

## Common Examples
### 1. Näytä käyttäjän salasanan voimassaoloasetukset
```bash
chage -l käyttäjänimi
```

### 2. Aseta minimipäivät salasanan vaihtamiselle
```bash
chage -m 7 käyttäjänimi
```

### 3. Aseta maksimi päivät salasanan voimassaololle
```bash
chage -M 90 käyttäjänimi
```

### 4. Aseta inaktiivisuusjakso
```bash
chage -I 30 käyttäjänimi
```

### 5. Aseta tilin vanhenemispäivämäärä
```bash
chage -E 2024-12-31 käyttäjänimi
```

## Tips
- Varmista, että käytät `chage`-komentoa järjestelmänvalvojan oikeuksilla, jotta voit muuttaa muiden käyttäjien asetuksia.
- Tarkista säännöllisesti käyttäjätilien salasanapolitiikka varmistaaksesi, että ne ovat ajan tasalla ja turvallisia.
- Käytä `chage -l` -komentoa säännöllisesti seurataksesi käyttäjien salasanan voimassaoloaikoja.