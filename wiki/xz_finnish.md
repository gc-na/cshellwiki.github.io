# [Linux] Bash xz käyttö: Tiedostojen pakkaaminen ja purkaminen

## Yleiskatsaus
`xz` on tehokas komento, jota käytetään tiedostojen pakkaamiseen ja purkamiseen. Se käyttää XZ-pakkausalgoritmia, joka tarjoaa erinomaisen pakkaussuhteen verrattuna moniin muihin pakkausmenetelmiin.

## Käyttö
Perussyntaksi `xz`-komennolle on seuraava:

```bash
xz [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d`, `--decompress`: Purkaa pakatun tiedoston.
- `-k`, `--keep`: Säilyttää alkuperäisen tiedoston pakkaamisen jälkeen.
- `-f`, `--force`: Pakkaa tai purkaa tiedoston, vaikka se olisi jo olemassa.
- `-z`, `--compress`: Pakkaa tiedoston (oletusvaihtoehto).
- `-9`: Käyttää maksimaalista pakkausta (1-9, missä 9 on paras pakkaussuhde).

## Yleiset esimerkit
### Tiedoston pakkaaminen
Pakkaa tiedosto nimeltä `esimerkki.txt`:
```bash
xz esimerkki.txt
```

### Tiedoston purkaminen
Purkaa pakattu tiedosto `esimerkki.txt.xz`:
```bash
xz -d esimerkki.txt.xz
```

### Alkuperäisen tiedoston säilyttäminen
Pakkaa tiedosto ja säilytä alkuperäinen:
```bash
xz -k esimerkki.txt
```

### Maksimaalinen pakkaus
Pakkaa tiedosto maksimaalisella pakkaussuhteella:
```bash
xz -9 esimerkki.txt
```

## Vinkit
- Käytä `-k`-vaihtoehtoa, jos haluat säilyttää alkuperäiset tiedostot pakkaamisen aikana.
- Varmista, että sinulla on tarpeeksi levytilaa, koska pakkaaminen voi vaatia enemmän tilaa kuin alkuperäiset tiedostot.
- Hyödynnä `-f`-vaihtoehtoa, jos haluat pakata tiedostoja, vaikka ne olisivat jo olemassa, mutta ole varovainen, sillä tämä voi korvata tiedostoja.