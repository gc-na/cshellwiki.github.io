# [Linux] Bash wget käyttö: Tiedostojen lataaminen verkosta

## Yleiskatsaus
`wget` on tehokas komentoriviohjelma, jota käytetään tiedostojen lataamiseen verkosta. Se tukee useita protokollia, kuten HTTP, HTTPS ja FTP, ja se on suunniteltu toimimaan vakaasti myös heikommissa verkkoyhteyksissä.

## Käyttö
Perussyntaksi `wget`-komennolle on seuraava:

```bash
wget [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-O [tiedostonimi]`: Määrittää ladattavan tiedoston nimen.
- `-q`: Käynnistää hiljaisen tilan, jolloin ohjelma ei tulosta mitään.
- `-c`: Jatkaa keskeytettyä latausta.
- `--limit-rate=[nopeus]`: Rajoittaa latausnopeuden.
- `-r`: Lataa verkkosivuston rekursiivisesti.

## Yleiset esimerkit
### Yksinkertainen tiedoston lataus
Lataa tiedosto suoraan URL-osoitteesta:

```bash
wget https://esimerkki.com/tiedosto.zip
```

### Tiedoston lataaminen tiettyyn nimeen
Lataa tiedosto ja nimeä se uudelleen:

```bash
wget -O uusi_tiedosto.zip https://esimerkki.com/tiedosto.zip
```

### Hiljainen lataus
Lataa tiedosto ilman tulostusta:

```bash
wget -q https://esimerkki.com/tiedosto.zip
```

### Latauksen jatkaminen
Jos lataus keskeytyy, voit jatkaa sitä seuraavalla komennolla:

```bash
wget -c https://esimerkki.com/tiedosto.zip
```

### Verkkosivuston lataaminen rekursiivisesti
Lataa koko verkkosivusto:

```bash
wget -r https://esimerkki.com
```

## Vinkit
- Käytä `-q`-vaihtoehtoa, kun haluat vähentää tulostusta, erityisesti skripteissä.
- Hyödynnä `--limit-rate`-vaihtoehtoa, jos haluat säästää kaistanleveyttä.
- Muista tarkistaa ladattavien tiedostojen oikeudet ja käyttöehdot ennen lataamista.