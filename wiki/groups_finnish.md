# [Linux] Bash groups käyttö: Käyttäjäryhmien näyttäminen

## Overview
`groups`-komento näyttää käyttäjäryhmät, joihin käyttäjä kuuluu. Tämä komento on hyödyllinen, kun halutaan tarkistaa käyttäjän ryhmäjäsenyys tai selvittää, mihin ryhmiin muut käyttäjät kuuluvat.

## Usage
Perussyntaksi `groups`-komennolle on seuraava:

```bash
groups [options] [arguments]
```

## Common Options
- `-h`, `--help`: Näyttää aputiedot komennosta.
- `-v`, `--version`: Näyttää versionumeron.

## Common Examples
### Esimerkki 1: Omat ryhmät
Voit tarkistaa omat ryhmäsi suorittamalla komennon ilman argumentteja:

```bash
groups
```

### Esimerkki 2: Tietyn käyttäjän ryhmät
Jos haluat tarkistaa toisen käyttäjän ryhmät, voit lisätä käyttäjänimen komennon perään:

```bash
groups käyttäjänimi
```

### Esimerkki 3: Useiden käyttäjien ryhmät
Voit myös tarkistaa useiden käyttäjien ryhmät kerralla:

```bash
groups käyttäjä1 käyttäjä2
```

## Tips
- Käytä `groups`-komentoa yhdessä muiden käyttäjähallintakomentojen, kuten `id`, kanssa saadaksesi kattavampaa tietoa käyttäjän oikeuksista.
- Muista, että `groups`-komento näyttää vain käyttäjän ryhmät, ei ryhmien jäseniä. Käytä `getent group`-komentoa, jos haluat nähdä ryhmien jäsenet.