# [Linux] Bash zip käyttö: Tiedostojen pakkaaminen

## Yleiskatsaus
`zip`-komento on työkalu, jota käytetään tiedostojen ja kansioiden pakkaamiseen ZIP-muotoon. Se vähentää tiedostojen kokoa ja helpottaa niiden siirtämistä tai tallentamista.

## Käyttö
Perussyntaksi `zip`-komennolle on seuraava:

```bash
zip [vaihtoehdot] [tiedostonimi.zip] [tiedostot...]
```

## Yleiset vaihtoehdot
- `-r`: Pakkaa koko hakemiston rekursiivisesti.
- `-e`: Luo salattu ZIP-tiedosto.
- `-9`: Käytä maksimaalista pakkausastetta.
- `-d`: Poistaa tiedostoja ZIP-arkistosta.

## Yleiset esimerkit
Pakkaa yksi tiedosto:

```bash
zip tiedosto.zip tiedosto.txt
```

Pakkaa useita tiedostoja:

```bash
zip arkisto.zip tiedosto1.txt tiedosto2.txt tiedosto3.txt
```

Pakkaa koko hakemisto:

```bash
zip -r hakemisto.zip hakemisto/
```

Luo salattu ZIP-tiedosto:

```bash
zip -e salattu.zip tiedosto.txt
```

Poista tiedosto ZIP-arkistosta:

```bash
zip -d arkisto.zip tiedosto.txt
```

## Vinkit
- Käytä `-9`-vaihtoehtoa, jos haluat maksimoida pakkausasteen, mutta muista, että tämä voi hidastaa prosessia.
- Salauksen lisääminen `-e`-vaihtoehdolla on hyvä tapa suojata arkistosi arkaluontoisilta tiedoilta.
- Tarkista ZIP-arkiston sisältö komennolla `unzip -l tiedosto.zip` ennen sen purkamista varmistaaksesi, että se sisältää oikeat tiedostot.