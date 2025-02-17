# [Linux] Bash dirs käyttö: Näyttää nykyiset hakemistot

## Overview
`dirs`-komento Bashissa näyttää nykyiset hakemistot, jotka on tallennettu hakemistopinoon. Tämä komento on erityisen hyödyllinen, kun työskentelet useissa hakemistoissa ja haluat nopeasti tarkistaa, mitkä hakemistot ovat käytettävissä.

## Usage
Perussyntaksi `dirs`-komennolle on seuraava:

```bash
dirs [options] [arguments]
```

## Common Options
- `-l` : Näyttää hakemistot pitkänä muotona.
- `-p` : Näyttää hakemistot ilman lyhennystä.
- `-c` : Tyhjentää hakemistopin.

## Common Examples

### Esimerkki 1: Näytä nykyiset hakemistot
Voit käyttää `dirs`-komentoa yksinkertaisesti näyttämään nykyiset hakemistot:

```bash
dirs
```

### Esimerkki 2: Näytä hakemistot pitkänä muotona
Jos haluat nähdä hakemistot yksityiskohtaisemmin, käytä `-l`-valintaa:

```bash
dirs -l
```

### Esimerkki 3: Tyhjennä hakemistopin
Jos haluat tyhjentää hakemistopin, voit käyttää `-c`-valintaa:

```bash
dirs -c
```

### Esimerkki 4: Näytä hakemistot ilman lyhennystä
Voit myös näyttää hakemistot ilman lyhennystä käyttämällä `-p`-valintaa:

```bash
dirs -p
```

## Tips
- Käytä `pushd` ja `popd` komentoja yhdessä `dirs`-komennon kanssa hallitaksesi hakemistopinoa tehokkaasti.
- Muista, että `dirs` näyttää vain hakemistot, jotka on tallennettu hakemistopinoon, joten varmista, että olet käyttänyt `pushd`-komentoa ennen `dirs`-komentoa.
- Voit yhdistää `dirs`-komennon muihin komentoihin, kuten `echo`, tulostaaksesi hakemistot selkeämmin:

```bash
echo "Nykyiset hakemistot: $(dirs)"
```