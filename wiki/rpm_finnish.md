# [Linux] Bash rpm käyttö: Pakettien hallinta

## Overview
`rpm` (Red Hat Package Manager) on työkalu, jota käytetään ohjelmistopakettien asentamiseen, poistamiseen ja hallintaan Linux-järjestelmissä, erityisesti Red Hat -pohjaisissa jakeluissa. Se mahdollistaa pakettien tarkistamisen, asennuksen ja päivityksen sekä riippuvuuksien hallinnan.

## Usage
Perussyntaksi `rpm`-komennolle on seuraava:

```bash
rpm [options] [arguments]
```

## Common Options
- `-i`: Asentaa uuden paketin.
- `-e`: Poistaa asennetun paketin.
- `-U`: Päivittää paketin uuteen versioon.
- `-q`: Kysyy paketin tietoja.
- `-l`: Listaa paketin tiedostot.
- `--checksig`: Tarkistaa paketin allekirjoituksen.

## Common Examples
Asennetaan uusi paketti:
```bash
rpm -i paketti.rpm
```

Poistetaan asennettu paketti:
```bash
rpm -e paketti-nimi
```

Päivitetään paketti:
```bash
rpm -U uusi-paketti.rpm
```

Kysytään paketin tietoja:
```bash
rpm -q paketti-nimi
```

Listataan paketin tiedostot:
```bash
rpm -l paketti-nimi
```

Tarkistetaan paketin allekirjoitus:
```bash
rpm --checksig paketti.rpm
```

## Tips
- Varmista aina, että käytät oikeaa pakettiversiota, erityisesti päivityksissä.
- Käytä `-v` (verbose) -optiota saadaksesi lisätietoja komennon suorittamisesta.
- Tarkista riippuvuudet ennen paketin asentamista, jotta vältät ongelmat asennuksen aikana.