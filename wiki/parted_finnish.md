# [Linux] Bash parted käyttö: Levyjen hallinta ja osiointi

## Overview
`parted` on komentorivityökalu, jota käytetään levyjen ja osioiden hallintaan Linux-järjestelmissä. Sen avulla voit luoda, muokata ja poistaa osioita sekä tarkastella levyjen tietoja.

## Usage
Perussyntaksi `parted`-komennolle on seuraava:

```bash
parted [options] [arguments]
```

## Common Options
- `-l`, `--list`: Näyttää kaikki käytettävissä olevat levyt ja niiden osiot.
- `-s`, `--script`: Käyttää skriptitilaa, jolloin kysymyksiä ei esitetä käyttäjälle.
- `mklabel`: Luo uuden osiointitaulukon levylle.
- `mkpart`: Luo uuden osion.
- `rm`: Poistaa olemassa olevan osion.

## Common Examples
### Levyjen listaus
Näyttää kaikki käytettävissä olevat levyt ja niiden osiot:
```bash
parted -l
```

### Uuden osiointitaulukon luominen
Luo uuden osiointitaulukon levylle (esim. `/dev/sda`):
```bash
parted /dev/sda mklabel gpt
```

### Uuden osion luominen
Luo uusi osio levylle (esim. `/dev/sda`), joka alkaa 1GB:sta ja päättyy 5GB:iin:
```bash
parted /dev/sda mkpart primary ext4 1GB 5GB
```

### Olemassa olevan osion poistaminen
Poistaa osion, jonka numero on 1 levyllä `/dev/sda`:
```bash
parted /dev/sda rm 1
```

## Tips
- Varmista, että varmuuskopioit tärkeät tiedot ennen osioiden muokkaamista.
- Käytä `-s`-optiota skriptitilassa, jos suoritat komentoja automaattisesti.
- Tarkista osioiden koko ja tyyppi ennen muutoksia varmistaaksesi, että ne vastaavat tarpeitasi.