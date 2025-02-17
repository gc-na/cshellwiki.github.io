# [Linux] Bash tar käyttö: Tiedostojen pakkaaminen ja purkaminen

## Yleiskatsaus
`tar`-komento on työkalu, jota käytetään tiedostojen pakkaamiseen ja purkamiseen Unix-tyyppisissä käyttöjärjestelmissä. Se voi yhdistää useita tiedostoja yhdeksi arkistoksi ja purkaa arkistoja, mikä helpottaa tiedostojen hallintaa ja siirtämistä.

## Käyttö
Perussyntaksi `tar`-komennolle on seuraava:

```bash
tar [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Luo uusi arkisto.
- `-x`: Purkaa arkiston.
- `-f`: Määrittelee arkiston nimen.
- `-v`: Näyttää prosessin aikana käsiteltävät tiedostot (verbose).
- `-z`: Pakkaa tai purkaa gzip-muodossa.
- `-j`: Pakkaa tai purkaa bzip2-muodossa.

## Yleiset esimerkit
### Arkiston luominen
Luodaan uusi arkisto nimeltä `tiedostot.tar`:

```bash
tar -cvf tiedostot.tar tiedosto1.txt tiedosto2.txt
```

### Arkiston purkaminen
Puretaan arkisto `tiedostot.tar`:

```bash
tar -xvf tiedostot.tar
```

### Gzip-pakatun arkiston luominen
Luodaan gzip-pakattu arkisto nimeltä `tiedostot.tar.gz`:

```bash
tar -czvf tiedostot.tar.gz tiedosto1.txt tiedosto2.txt
```

### Bzip2-pakatun arkiston purkaminen
Puretaan bzip2-pakattu arkisto `tiedostot.tar.bz2`:

```bash
tar -xjvf tiedostot.tar.bz2
```

## Vinkit
- Käytä `-v`-vaihtoehtoa, jos haluat nähdä, mitkä tiedostot käsitellään, mikä voi olla hyödyllistä suurissa arkistoissa.
- Varmista, että käytät oikeaa vaihtoehtoa pakkaamiseen tai purkamiseen, jotta tiedostot eivät vahingoitu.
- Voit yhdistää useita tiedostoja tai hakemistoja arkistoon käyttämällä niiden nimiä peräkkäin komennossa.