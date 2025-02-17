# [Linux] Bash tee käyttö: Tietojen ohjaaminen useisiin kohteisiin

## Overview
`tee`-komento on Bashin työkalu, joka lukee standardisyötteen ja kirjoittaa sen sekä standardilähtöön että tiedostoon tai useisiin tiedostoihin. Tämä mahdollistaa tietojen samanaikaisen tarkastelun ja tallentamisen.

## Usage
Perussyntaksi `tee`-komennolle on seuraava:

```bash
tee [options] [arguments]
```

## Common Options
- `-a`, `--append`: Lisää tiedot tiedoston loppuun sen sijaan, että ylikirjoittaisi sen.
- `-i`, `--ignore-interrupts`: Ohita keskeytyssignaalit.
- `--help`: Näyttää aputiedot komennosta.
- `--version`: Näyttää ohjelman version.

## Common Examples
### Esimerkki 1: Tietojen tallentaminen tiedostoon
Voit ohjata komennon tulosteen tiedostoon `output.txt` seuraavasti:

```bash
echo "Hello, World!" | tee output.txt
```

### Esimerkki 2: Tietojen lisääminen olemassa olevaan tiedostoon
Jos haluat lisätä tietoja tiedoston loppuun, käytä `-a`-optiota:

```bash
echo "New line" | tee -a output.txt
```

### Esimerkki 3: Tietojen ohjaaminen useisiin tiedostoihin
Voit myös ohjata tulosteen useisiin tiedostoihin kerralla:

```bash
echo "Data for both files" | tee file1.txt file2.txt
```

### Esimerkki 4: Tietojen näyttäminen ja tallentaminen
Jos haluat nähdä tulosteen terminaalissa ja tallentaa sen tiedostoon:

```bash
cat somefile.txt | tee output.txt
```

## Tips
- Käytä `-a`-optiota, kun haluat lisätä tietoja olemassa olevaan tiedostoon, jotta et vahingossa ylikirjoita tärkeitä tietoja.
- Voit yhdistää `tee`-komennon muihin komentoihin putkissa, jolloin voit käsitellä tietoja ennen niiden tallentamista.
- Muista tarkistaa tiedostojen oikeudet, jotta sinulla on tarvittavat oikeudet kirjoittaa tiedostoihin.