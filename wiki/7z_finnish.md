# [Linux] Bash 7z käyttö: Tiedostojen pakkaaminen ja purkaminen

## Yleiskatsaus
7z on tehokas komentorivipohjainen työkalu, joka mahdollistaa tiedostojen pakkaamisen ja purkamisen useissa eri formaateissa. Se tukee monia pakkausmenetelmiä ja tarjoaa erinomaisen pakkaussuhteen.

## Käyttö
Perussyntaksi 7z-komennolle on seuraava:

```
7z [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `a`: Lisää tiedostoja arkistoon.
- `x`: Purkaa tiedostoja arkistosta.
- `t`: Tarkistaa arkiston eheyttä.
- `l`: Listaa arkiston sisällön.
- `d`: Poistaa tiedostoja arkistosta.

## Yleiset esimerkit
### Tiedostojen pakkaaminen
Pakkaa tiedostot nimeltä `tiedosto1.txt` ja `tiedosto2.txt` arkistoon `arkisto.7z`:
```bash
7z a arkisto.7z tiedosto1.txt tiedosto2.txt
```

### Tiedostojen purkaminen
Purkaa arkisto `arkisto.7z` nykyiseen hakemistoon:
```bash
7z x arkisto.7z
```

### Arkiston sisällön listaaminen
Listaa arkiston `arkisto.7z` sisältö:
```bash
7z l arkisto.7z
```

### Arkiston eheystarkistus
Tarkistaa arkiston `arkisto.7z` eheys:
```bash
7z t arkisto.7z
```

### Tiedoston poistaminen arkistosta
Poistaa tiedoston `tiedosto1.txt` arkistosta `arkisto.7z`:
```bash
7z d arkisto.7z tiedosto1.txt
```

## Vinkit
- Käytä `-p` -vaihtoehtoa lisätäksesi salasanan arkistoon, mikä lisää tietoturvaa.
- Hyödynnä `-mx` -vaihtoehtoa säätääksesi pakkaustasoa (0-9), jossa 0 tarkoittaa ei-pakkaamista ja 9 maksimaalista pakkausta.
- Tarkista aina arkiston eheys ennen tiedostojen purkamista, erityisesti suurissa tai tärkeissä arkistoissa.