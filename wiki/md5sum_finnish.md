# [Linux] Bash md5sum käyttö: Tiedostojen MD5-tarkistussumman laskeminen

## Yleiskatsaus
`md5sum`-komento on työkalu, joka laskee ja tarkistaa tiedostojen MD5-tarkistussummat. MD5-tarkistussumma on 128-bittinen luku, jota käytetään usein tiedostojen eheys- ja identiteettitarkistukseen.

## Käyttö
Perussyntaksi `md5sum`-komennolle on seuraava:

```bash
md5sum [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-b`: Käsittele binääritiedostoja.
- `-c`: Tarkista MD5-tarkistussummat tiedostosta.
- `-t`: Laske tarkistussumma vain standardisyötteestä.
- `--help`: Näytä apu ja vaihtoehdot.

## Yleiset esimerkit
### 1. MD5-tarkistussumman laskeminen tiedostolle
```bash
md5sum tiedosto.txt
```

### 2. MD5-tarkistussumman tallentaminen tiedostoon
```bash
md5sum tiedosto.txt > tarkistus.txt
```

### 3. Tarkistussumman tarkistaminen tiedostosta
```bash
md5sum -c tarkistus.txt
```

### 4. MD5-tarkistussumman laskeminen useille tiedostoille
```bash
md5sum tiedosto1.txt tiedosto2.txt
```

## Vinkit
- Käytä `-c`-vaihtoehtoa varmistaaksesi, että tiedostot eivät ole muuttuneet, erityisesti siirron jälkeen.
- Voit yhdistää `md5sum`-komennon putkistoon muiden komentojen kanssa, kuten `find`, tiedostojen automaattiseen tarkistamiseen.
- Muista, että MD5 ei ole täysin turvallinen kryptografinen algoritmi, joten käytä sitä vain tiedostojen eheystarkistukseen, ei salassapitoon.