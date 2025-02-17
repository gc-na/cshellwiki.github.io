# [Linux] Bash netcat käyttö: Verkkoyhteyksien luominen ja testaaminen

## Yleiskatsaus
Netcat, usein lyhennettynä "nc", on monipuolinen työkalu, jota käytetään verkkoyhteyksien luomiseen ja testaamiseen. Se voi toimia sekä palvelimena että asiakkaana, ja sen avulla voi lähettää ja vastaanottaa tietoja TCP- tai UDP-protokollien kautta.

## Käyttö
Perussyntaksi netcat-komennolle on seuraava:

```bash
netcat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Kuuntelee saapuvia yhteyksiä (palvelin).
- `-p [portti]`: Määrittää portin, jota käytetään.
- `-u`: Käyttää UDP-protokollaa TCP:n sijaan.
- `-v`: Näyttää lisätietoja yhteyksistä (verbose).
- `-z`: Testaa vain yhteyden ilman tietojen lähettämistä.

## Yleiset esimerkit

### Yhteyden kuuntelu
Kuuntele porttia 1234 ja odota saapuvia yhteyksiä:
```bash
netcat -l -p 1234
```

### Yhteyden muodostaminen
Yhdistä palvelimeen IP-osoitteella 192.168.1.10 portissa 1234:
```bash
netcat 192.168.1.10 1234
```

### Tiedostojen siirtäminen
Lähetä tiedosto nimeltä `tiedosto.txt` toiseen koneeseen:
```bash
netcat -l -p 1234 > vastaanota.txt
```
Toisella koneella:
```bash
netcat 192.168.1.10 1234 < tiedosto.txt
```

### Porttiskannaus
Skannaa portit 1-1000 kohdekoneessa:
```bash
netcat -z -v 192.168.1.10 1-1000
```

## Vinkit
- Käytä `-v`-vaihtoehtoa saadaksesi lisätietoja yhteyksistä ja virheistä.
- Varmista, että palomuuriasetukset sallivat tarvittavat portit.
- Netcat voi olla hyödyllinen työkalu myös skriptauksessa, joten harkitse sen käyttöä automaatiossa.