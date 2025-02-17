# [Linux] Bash head käyttö: Näyttää tiedoston alun

## Overview
`head`-komento on Bash-komento, jota käytetään näyttämään tiedoston alkuosa. Oletusarvoisesti se näyttää ensimmäiset 10 riviä tiedostosta, mutta käyttäjä voi määrittää haluamansa rivimäärän.

## Usage
Perussyntaksi `head`-komennolle on seuraava:

```bash
head [options] [arguments]
```

## Common Options
- `-n [number]`: Määrittää näytettävien rivien määrän. Esimerkiksi `-n 5` näyttää ensimmäiset 5 riviä.
- `-c [number]`: Määrittää näytettävien merkkien määrän. Esimerkiksi `-c 100` näyttää ensimmäiset 100 merkkiä.
- `-q`: Ei tulosta tiedoston nimeä, kun useita tiedostoja käsitellään.
- `-v`: Tulostaa tiedoston nimen ennen sen sisältöä.

## Common Examples
Tässä on muutamia käytännön esimerkkejä `head`-komennon käytöstä:

1. Näytä ensimmäiset 10 riviä tiedostosta:
    ```bash
    head tiedosto.txt
    ```

2. Näytä ensimmäiset 5 riviä tiedostosta:
    ```bash
    head -n 5 tiedosto.txt
    ```

3. Näytä ensimmäiset 100 merkkiä tiedostosta:
    ```bash
    head -c 100 tiedosto.txt
    ```

4. Näytä ensimmäiset 10 riviä useasta tiedostosta:
    ```bash
    head tiedosto1.txt tiedosto2.txt
    ```

5. Näytä ensimmäiset 20 riviä tiedostosta ilman tiedoston nimeä:
    ```bash
    head -n 20 -q tiedosto1.txt tiedosto2.txt
    ```

## Tips
- Voit yhdistää `head`-komennon muihin komentoihin, kuten `grep` tai `sort`, putkittamalla tuloksia.
- Käytä `-v`-vaihtoehtoa, kun haluat selkeästi nähdä, mistä tiedostosta rivit tulevat, erityisesti useiden tiedostojen kanssa.
- Muista, että `head`-komento ei muokkaa alkuperäistä tiedostoa, vaan näyttää vain sen osan.