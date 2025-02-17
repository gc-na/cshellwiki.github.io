# [Linux] Bash apt käyttö: Pakettien hallinta

## Yleiskatsaus
`apt` on komento, jota käytetään Debian-pohjaisissa Linux-järjestelmissä ohjelmistopakettien hallintaan. Se mahdollistaa ohjelmistojen asentamisen, päivittämisen ja poistamisen helposti komentoriviltä.

## Käyttö
Perussyntaksi `apt`-komennolle on seuraava:

```bash
apt [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `install`: Asentaa yhden tai useamman ohjelmistopaketin.
- `remove`: Poistaa yhden tai useamman ohjelmistopaketin.
- `update`: Päivittää pakettivarastojen tiedot.
- `upgrade`: Päivittää asennetut paketit uusimpiin versioihin.
- `search`: Etsii paketteja nimellä tai kuvauksella.

## Yleiset esimerkit
Asennetaan ohjelmisto:

```bash
sudo apt install ohjelman_nimi
```

Poistetaan ohjelmisto:

```bash
sudo apt remove ohjelman_nimi
```

Päivitetään pakettivarastot:

```bash
sudo apt update
```

Päivitetään kaikki asennetut paketit:

```bash
sudo apt upgrade
```

Etsitään ohjelmistoa:

```bash
apt search ohjelman_nimi
```

## Vinkit
- Käytä `sudo`-komentoa, jotta saat tarvittavat oikeudet pakettien asentamiseen tai poistamiseen.
- Suosittelemme suorittamaan `apt update` ennen `apt upgrade` -komentoa varmistaaksesi, että käytät uusimpia pakettitietoja.
- Voit käyttää `apt list --upgradable` nähdäksesi, mitkä paketit ovat päivitettävissä.