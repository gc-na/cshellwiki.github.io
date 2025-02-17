# [Linux] Bash export käyttö: Ympäristömuuttujien määrittäminen

## Overview
`export`-komento Bashissa käytetään ympäristömuuttujien määrittämiseen ja niiden tekemiseen saataville alikomennoille. Kun muuttuja on viety, se on käytettävissä kaikissa sen jälkeen käynnistetyissä prosesseissa.

## Usage
Perussyntaksi `export`-komennolle on seuraava:

```bash
export [options] [arguments]
```

## Common Options
- `-n`: Poistaa muuttujan vienti.
- `-p`: Näyttää kaikki viedyt muuttujat.

## Common Examples

### Muuttujan vienti
Voit määrittää ja viedä ympäristömuuttujan seuraavasti:

```bash
MY_VAR="Hello, World!"
export MY_VAR
```

### Muuttujan tarkistaminen
Voit tarkistaa, että muuttuja on viety oikein käyttämällä `echo`-komentoa:

```bash
echo $MY_VAR
```

### Useiden muuttujien vienti
Voit myös viedä useita muuttujia yhdellä komennolla:

```bash
export VAR1="Value1" VAR2="Value2"
```

### Muuttujan vienti ilman arvoa
Voit viedä muuttujan ilman arvoa, jolloin se saa tyhjät arvot:

```bash
export MY_EMPTY_VAR
```

### Näytä kaikki viedyt muuttujat
Voit näyttää kaikki tällä hetkellä viedyt muuttujat seuraavasti:

```bash
export -p
```

## Tips
- Muista, että `export`-komento vaikuttaa vain nykyiseen istuntoon ja sen alikomentoihin. Jos haluat, että ympäristömuuttuja on käytettävissä myös seuraavissa istunnoissa, voit lisätä sen esimerkiksi `.bashrc`- tai `.bash_profile`-tiedostoon.
- Käytä selkeitä ja kuvaavia nimiä muuttujille, jotta niiden tarkoitus on helppo ymmärtää.
- Vältä muuttujien nimeämistä yleisillä nimillä, kuten `PATH` tai `HOME`, jotta et aiheuta konflikteja järjestelmän muuttujien kanssa.