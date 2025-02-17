# [Linux] Bash curl käyttö: Verkkopyynnöt ja tiedostojen lataaminen

## Yleiskatsaus
`curl` on komento, jota käytetään verkkopyyntöjen tekemiseen ja tiedostojen lataamiseen tai lähettämiseen eri protokollien, kuten HTTP, HTTPS ja FTP, kautta. Se on erittäin hyödyllinen työkalu verkkosovellusten testaamiseen ja tiedostojen siirtämiseen.

## Käyttö
Perussyntaksi `curl`-komennolle on seuraava:
```bash
curl [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-O`: Lataa tiedosto ja nimeä se samalla kuin palvelimella.
- `-o [tiedostonimi]`: Lataa tiedosto ja nimeä se haluamaksesi.
- `-I`: Hakee vain HTTP-otsikot.
- `-X [metodi]`: Määrittää HTTP-menetelmän (esim. GET, POST).
- `-d [data]`: Lähettää tietoja POST-pyynnössä.
- `-H [otsikko]`: Lisää mukautetun HTTP-otsikon pyyntöön.

## Yleiset esimerkit
### Tiedoston lataaminen
Lataa tiedosto palvelimelta ja nimeä se samalla kuin palvelimella:
```bash
curl -O http://esimerkki.com/tiedosto.txt
```

### HTTP-otsikoiden hakeminen
Hae vain HTTP-otsikot tietystä URL-osoitteesta:
```bash
curl -I http://esimerkki.com
```

### POST-pyynnön tekeminen
Lähetä tietoja POST-pyynnössä:
```bash
curl -X POST -d "nimi=esimerkki&ikä=25" http://esimerkki.com/api
```

### Mukautetun otsikon lisääminen
Lisää mukautettu HTTP-otsikko pyyntöön:
```bash
curl -H "Authorization: Bearer token" http://esimerkki.com/suojattu
```

## Vinkit
- Käytä `-v`-vaihtoehtoa saadaksesi yksityiskohtaisempaa tietoa pyynnöistä ja vastauksista, mikä on hyödyllistä virheiden etsinnässä.
- Muista, että `curl` voi myös käsitellä useita tiedostotyyppejä ja protokollia, joten kokeile eri vaihtoehtoja tarpeidesi mukaan.
- Varmista, että käytät HTTPS-protokollaa, kun siirrät arkaluontoisia tietoja, jotta tiedot pysyvät turvassa.