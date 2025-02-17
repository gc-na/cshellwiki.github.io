# [Linux] Bash mkfifo käyttö: Luodaan nimettyjä putkia

## Overview
`mkfifo` on Bash-komento, jota käytetään nimettyjen putkien (FIFO) luomiseen. Nimetyt putket mahdollistavat prosessien välisen viestinnän, jolloin yksi prosessi voi kirjoittaa tietoa putkeen ja toinen prosessi voi lukea sitä.

## Usage
Perussyntaksi komennolle on seuraava:

```bash
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE`: Määrittää putken käyttöoikeudet. Esimerkiksi `-m 644` asettaa käyttöoikeudet.
- `--help`: Näyttää aputiedot komennosta.
- `--version`: Näyttää versionumeron.

## Common Examples
### Esimerkki 1: Perusputken luominen
Luodaan nimetty putki nimeltä `mypipe`:

```bash
mkfifo mypipe
```

### Esimerkki 2: Putken käyttö oikeuksien määrittämiseen
Luodaan nimetty putki, jossa on tietyt käyttöoikeudet:

```bash
mkfifo -m 666 mypipe
```

### Esimerkki 3: Putken lukeminen ja kirjoittaminen
Voit käyttää putkea prosessien välillä. Esimerkiksi:

1. Avaa yksi terminaali ja kirjoita:

    ```bash
    echo "Hello, World!" > mypipe
    ```

2. Avaa toinen terminaali ja kirjoita:

    ```bash
    cat mypipe
    ```

Tämä tulostaa "Hello, World!" ensimmäisestä terminaalista toiseen.

## Tips
- Varmista, että putki on luotu ennen kuin yrität kirjoittaa tai lukea siitä.
- Käytä `-m`-vaihtoehtoa, jos haluat hallita putken käyttöoikeuksia tarkemmin.
- Muista, että nimetty putki estää kirjoittamisen, jos ei ole lukijaa, joten varmista, että lukija on käynnissä ennen kirjoittamista.