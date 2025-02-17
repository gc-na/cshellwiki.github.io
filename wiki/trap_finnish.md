# [Linux] Bash trap käyttö: Ohjelman keskeyttämisen hallinta

## Overview
`trap`-komento Bashissa mahdollistaa ohjelman keskeyttämisen tai tiettyjen toimintojen suorittamisen, kun ohjelma saa tiettyjä signaaleja. Tämä on erityisen hyödyllistä, kun halutaan varmistaa, että tietyt puhdistustoimet suoritetaan ennen ohjelman lopettamista.

## Usage
Perussyntaksi `trap`-komennolle on seuraava:

```bash
trap [toiminto] [signaalit]
```

## Common Options
- `EXIT`: Suorittaa määritellyn toiminnon, kun skripti päättyy.
- `SIGINT`: Suorittaa toiminnon, kun käyttäjä keskeyttää ohjelman (esim. Ctrl+C).
- `SIGTERM`: Suorittaa toiminnon, kun ohjelma saa lopetussignaalin.

## Common Examples

### Esimerkki 1: Puhdistustoiminto ohjelman lopussa
```bash
trap 'echo "Ohjelma suljetaan"; rm -f /tmp/tiedosto' EXIT
```
Tässä esimerkissä ohjelma tulostaa viestin ja poistaa väliaikaisen tiedoston, kun se suljetaan.

### Esimerkki 2: Keskeytyksen käsittely
```bash
trap 'echo "Keskeytetty käyttäjän toimesta"; exit' SIGINT
```
Tässä komennossa ohjelma tulostaa viestin ja lopettaa suorituksen, kun käyttäjä keskeyttää sen.

### Esimerkki 3: Useiden signaalien käsittely
```bash
trap 'echo "Ohjelma keskeytetty"; exit' SIGINT SIGTERM
```
Tässä esimerkissä ohjelma reagoi sekä keskeytyssignaaliin että lopetussignaaliin samalla tavalla.

## Tips
- Käytä `trap`-komentoa aina, kun ohjelmasi voi keskeytyä tai lopettaa odottamattomasti, jotta voit varmistaa, että tarvittavat puhdistustoimet suoritetaan.
- Testaa `trap`-komentoa huolellisesti, jotta voit varmistaa, että se toimii odotetusti eri tilanteissa.
- Muista, että `trap`-komento voi myös estää ohjelman odottamattoman sulkeutumisen, mikä voi olla hyödyllistä pitkäkestoisissa prosesseissa.