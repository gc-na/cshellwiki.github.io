# [Linux] Bash gzip käyttö: Tiedostojen pakkaaminen

## Yleiskatsaus
`gzip` on komento, jota käytetään tiedostojen pakkaamiseen Unix- ja Linux-järjestelmissä. Se vähentää tiedostojen kokoa, mikä helpottaa niiden tallentamista ja siirtämistä. Gzip käyttää tehokasta pakkausalgoritmia, joka voi merkittävästi pienentää tiedostojen tilaa.

## Käyttö
Perussyntaksi gzip-komennolle on seuraava:
```
gzip [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d`, `--decompress`: Purkaa pakatut tiedostot.
- `-k`, `--keep`: Säilyttää alkuperäisen tiedoston pakkaamisen jälkeen.
- `-v`, `--verbose`: Näyttää yksityiskohtaisia tietoja pakkausprosessista.
- `-r`, `--recursive`: Pakkaa kaikki tiedostot ja alikansiot rekursiivisesti.

## Yleiset esimerkit
Pakkaa tiedosto nimeltä `esimerkki.txt`:
```bash
gzip esimerkki.txt
```

Purkaa pakattu tiedosto nimeltä `esimerkki.txt.gz`:
```bash
gzip -d esimerkki.txt.gz
```

Pakkaa tiedosto ja säilytä alkuperäinen tiedosto:
```bash
gzip -k esimerkki.txt
```

Pakkaa kaikki `.txt`-tiedostot nykyisessä hakemistossa:
```bash
gzip *.txt
```

Pakkaa tiedostot rekursiivisesti hakemistosta `data`:
```bash
gzip -r data/
```

## Vinkit
- Käytä `-v`-vaihtoehtoa, jos haluat nähdä pakkausprosessin yksityiskohdat ja tiedostojen koon muutokset.
- Muista, että gzip muuttaa tiedoston nimeä pakkaamisen jälkeen, joten alkuperäinen tiedosto poistuu, ellei käytä `-k`-vaihtoehtoa.
- Gzip on erityisen hyödyllinen suurten tekstimuotoisten tiedostojen pakkaamiseen, kuten lokitiedostojen tai CSV-tiedostojen.