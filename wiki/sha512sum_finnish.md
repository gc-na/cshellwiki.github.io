# [Linux] Bash sha512sum käyttö: Lasketaan SHA-512 tiivisteitä

## Yleiskatsaus
`sha512sum` on komentorivikäsky, joka laskee ja tarkistaa tiedostojen SHA-512 tiivisteet. Tämä on hyödyllistä tiedostojen eheyden varmistamiseksi ja tietoturvan parantamiseksi.

## Käyttö
Perussyntaksi komennolle on seuraava:
```bash
sha512sum [options] [arguments]
```

## Yleiset vaihtoehdot
- `-b`, `--binary`: Käsittele tiedostoa binäärimuodossa.
- `-c`, `--check`: Tarkista tiivisteet tiedostosta.
- `-h`, `--help`: Näytä apu ja käytön ohjeet.
- `-o`, `--output`: Määritä tulostiedosto, johon tiivisteet tallennetaan.

## Yleiset esimerkit
### 1. SHA-512 tiivisteen laskeminen tiedostosta
```bash
sha512sum tiedosto.txt
```
Tämä komento laskee `tiedosto.txt`-tiedoston SHA-512 tiivisteen ja tulostaa sen konsoliin.

### 2. Tiivisteen tallentaminen tiedostoon
```bash
sha512sum tiedosto.txt > tiiviste.txt
```
Tässä komennossa lasketaan `tiedosto.txt`-tiedoston tiiviste ja tallennetaan se `tiiviste.txt`-tiedostoon.

### 3. Tiivisteen tarkistaminen
```bash
sha512sum -c tiiviste.txt
```
Tämä komento tarkistaa, vastaavatko `tiiviste.txt`-tiedostossa olevat tiivisteet vastaavia tiedostoja nykyisessä hakemistossa.

### 4. Binäärimuotoisen tiedoston tiiviste
```bash
sha512sum -b tiedosto.bin
```
Tässä komennossa lasketaan binäärimuotoisen `tiedosto.bin`-tiedoston SHA-512 tiiviste.

## Vinkit
- Varmista, että käytät `-c`-vaihtoehtoa, kun tarkistat tiivisteitä, jotta voit varmistaa tiedostojen eheyden.
- Tallenna tiivisteet erilliseen tiedostoon, jotta voit tarkistaa ne myöhemmin.
- Käytä `-h`-vaihtoehtoa, jos tarvitset apua komennon käytössä tai haluat nähdä kaikki saatavilla olevat vaihtoehdot.