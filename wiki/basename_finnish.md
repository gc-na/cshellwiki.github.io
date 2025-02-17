# [Linux] Bash basename käyttö: Tiedostonimen erottaminen polusta

## Overview
`basename`-komento on Bash-komento, jota käytetään tiedostonimen erottamiseen sen polusta. Se palauttaa vain tiedostonimen ilman sen edeltäviä hakemistoja.

## Usage
Perussyntaksi `basename`-komennolle on seuraava:

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: Käsittelee useita tiedostoja ja palauttaa jokaisen tiedoston nimen.
- `-s`: Poistaa määritellyn päätteet tiedostonimestä.
- `--help`: Näyttää apu- ja käyttöohjeet.

## Common Examples
### Esimerkki 1: Yksinkertainen tiedostonimen erottaminen
```bash
basename /home/kayttaja/tiedosto.txt
```
Tuloste: 
```
tiedosto.txt
```

### Esimerkki 2: Tiedostonimen erottaminen ilman päätettä
```bash
basename /home/kayttaja/tiedosto.txt .txt
```
Tuloste: 
```
tiedosto
```

### Esimerkki 3: Useiden tiedostojen käsittely
```bash
basename -a /home/kayttaja/tiedosto1.txt /home/kayttaja/tiedosto2.txt
```
Tuloste: 
```
tiedosto1.txt
tiedosto2.txt
```

## Tips
- Käytä `basename`-komentoa skripteissä, kun haluat käsitellä tiedostopolkuja ja tarvitsen vain tiedostonimen.
- Muista käyttää `-s`-optiota, jos haluat poistaa tiedostopäätteitä automaattisesti.
- Voit yhdistää `basename`-komennon muihin komentoihin, kuten `find`, saadaksesi tehokkaampia tuloksia.