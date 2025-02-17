# [Linux] Bash mountpoint käyttö: Tarkistaa, onko hakemisto liitetty

## Overview
`mountpoint`-komento tarkistaa, onko tietty hakemisto liitetty tiedostojärjestelmään. Tämä on hyödyllistä, kun halutaan varmistaa, että tiedostot tai kansiot ovat käytettävissä oikeassa paikassa.

## Usage
Perussyntaksi `mountpoint`-komennolle on seuraava:

```bash
mountpoint [options] [arguments]
```

## Common Options
- `-q`, `--quiet`: Ei tulosta mitään, vain palauta tila.
- `-d`, `--directory`: Tarkistaa, onko annettu hakemisto liitetty.
- `-h`, `--help`: Näyttää ohjeet ja käytön.

## Common Examples

### Esimerkki 1: Tarkista, onko hakemisto liitetty
```bash
mountpoint /mnt/data
```
Tämä komento tarkistaa, onko `/mnt/data`-hakemisto liitetty.

### Esimerkki 2: Käytä hiljaista tilaa
```bash
mountpoint -q /mnt/data
```
Tämä komento tarkistaa, onko `/mnt/data`-hakemisto liitetty, mutta ei tulosta mitään.

### Esimerkki 3: Tarkista useita hakemistoja
```bash
mountpoint /mnt/data /mnt/backup
```
Tässä komennossa tarkistetaan, ovatko molemmat hakemistot liitettyjä.

## Tips
- Käytä `-q`-vaihtoehtoa skripteissä, joissa et halua tulostaa mitään, vaan haluat vain tarkistaa tilan.
- Varmista, että käytät oikeita polkuja, jotta saat tarkkoja tuloksia.
- `mountpoint`-komento on erityisen hyödyllinen järjestelmänvalvojille, jotka hallitsevat useita tiedostojärjestelmiä.