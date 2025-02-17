# [Linux] Bash unzip käyttö: Tiedostojen purkaminen ZIP-arkistoista

## Yleiskatsaus
`unzip`-komento on työkalu, jota käytetään ZIP-arkistojen purkamiseen. Se mahdollistaa pakattujen tiedostojen ja kansioiden palauttamisen alkuperäiseen muotoonsa, jolloin voit käyttää niitä normaalisti.

## Käyttö
Perussyntaksi `unzip`-komennolle on seuraava:

```bash
unzip [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Listaa ZIP-arkiston sisällön ilman purkamista.
- `-d`: Määrittää kohdekansion, johon tiedostot puretaan.
- `-o`: Ylikirjoittaa olemassa olevat tiedostot ilman varmistusta.
- `-q`: Suorittaa purkamisen hiljaisessa tilassa, jolloin ei näytetä purkamisen aikana tietoja.

## Yleiset esimerkit
### 1. ZIP-arkiston purkaminen nykyiseen kansioon
```bash
unzip tiedosto.zip
```

### 2. ZIP-arkiston purkaminen tiettyyn kansioon
```bash
unzip tiedosto.zip -d /polku/kohdekansioon
```

### 3. ZIP-arkiston sisällön listaaminen
```bash
unzip -l tiedosto.zip
```

### 4. Ylikirjoittaminen ilman varmistusta
```bash
unzip -o tiedosto.zip
```

### 5. Hiljainen purkaminen
```bash
unzip -q tiedosto.zip
```

## Vinkit
- Tarkista aina ZIP-arkiston sisältö ennen purkamista käyttämällä `-l`-vaihtoehtoa.
- Käytä `-d`-vaihtoehtoa, jos haluat pitää purkamasi tiedostot järjestyksessä tietyssä kansiossa.
- Ole varovainen `-o`-vaihtoehdon kanssa, sillä se voi ylikirjoittaa tärkeitä tiedostoja ilman varoitusta.