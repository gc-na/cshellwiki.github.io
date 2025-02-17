# [Linux] Bash pkg käyttö: Pakettien hallinta

## Overview
`pkg` on komentorivikäsky, jota käytetään pakettien hallintaan Unix-pohjaisissa järjestelmissä. Se mahdollistaa ohjelmistopakettien asentamisen, päivittämisen ja poistamisen, mikä tekee siitä tärkeän työkalun järjestelmän ylläpidossa.

## Usage
Perussyntaksi `pkg`-komennolle on seuraava:

```bash
pkg [options] [arguments]
```

## Common Options
- `install`: Asentaa uuden paketin.
- `remove`: Poistaa olemassa olevan paketin.
- `update`: Päivittää kaikki asennetut paketit.
- `search`: Etsii paketteja nimellä tai kuvauksella.
- `info`: Näyttää tietoja tietystä paketista.

## Common Examples
### Paketin asentaminen
Asentaaksesi uuden paketin, käytä seuraavaa komentoa:

```bash
pkg install <paketin_nimi>
```

### Paketin poistaminen
Poistaaksesi paketin, käytä komentoa:

```bash
pkg remove <paketin_nimi>
```

### Pakettien päivittäminen
Päivittääksesi kaikki asennetut paketit, käytä komentoa:

```bash
pkg update
```

### Pakettien etsiminen
Etsi paketteja käyttämällä seuraavaa komentoa:

```bash
pkg search <hakusana>
```

### Pakettitietojen näyttäminen
Näyttääksesi tietoja tietystä paketista, käytä komentoa:

```bash
pkg info <paketin_nimi>
```

## Tips
- Varmista, että käytät `sudo`-oikeuksia, kun asennat tai poistat paketteja, jotta sinulla on tarvittavat käyttöoikeudet.
- Tarkista säännöllisesti käytettävissä olevat päivitykset `pkg update` -komennolla, jotta järjestelmäsi pysyy ajan tasalla.
- Käytä `pkg search` -komentoa ennen asennusta varmistaaksesi, että paketti on saatavilla ja että sen nimi on oikein.