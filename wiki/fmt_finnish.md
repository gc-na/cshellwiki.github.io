# [Linux] Bash fmt käyttö: Tekstin muotoilu

## Overview
`fmt` on komentorivikäsky, joka muotoilee tekstiä siten, että se on helpommin luettavissa. Se säätää rivien pituuden ja poistaa ylimääräiset rivinvaihdot, mikä tekee siitä hyödyllisen työkalun tekstidokumenttien käsittelyssä.

## Usage
Perussyntaksi `fmt`-komennolle on seuraava:

```bash
fmt [options] [arguments]
```

## Common Options
- `-w, --width <leveys>`: Määrittää rivin maksimi leveyden. Oletusarvo on 75 merkkiä.
- `-s, --split-only`: Jakaa vain pitkät rivit, mutta ei muotoile lyhyita rivejä.
- `-p, --paragraphs`: Muotoilee vain eristetyt kappaleet.
- `-u, --uniform`: Muotoilee tekstiä siten, että rivit ovat tasaisesti jakautuneet.

## Common Examples
### Esimerkki 1: Perusmuotoilu
Muotoile tekstitiedosto `esimerkki.txt` ja tallenna tulos `muotoiltu.txt`-tiedostoon.

```bash
fmt esimerkki.txt > muotoiltu.txt
```

### Esimerkki 2: Määritä rivin leveys
Muotoile teksti 50 merkin levyisiksi riveiksi.

```bash
fmt -w 50 esimerkki.txt
```

### Esimerkki 3: Jakaa vain pitkät rivit
Käytä `-s`-optiota jakamaan vain yli 80 merkin pituiset rivit.

```bash
fmt -s esimerkki.txt
```

### Esimerkki 4: Muotoile vain kappaleet
Muotoile vain eristetyt kappaleet tiedostosta.

```bash
fmt -p esimerkki.txt
```

## Tips
- Käytä `-w`-optiota säätääksesi rivin pituuden tarpeidesi mukaan.
- Yhdistä `fmt` muihin komentoihin, kuten `cat`, käsitelläksesi useita tiedostoja kerralla.
- Muista tarkistaa tulosteen muotoilu ennen kuin tallennat sen uuteen tiedostoon, jotta voit varmistaa, että se vastaa odotuksiasi.