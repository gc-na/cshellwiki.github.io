# [Linux] Bash tune2fs käyttö: Tiedostojärjestelmän säätö

## Yleiskatsaus
`tune2fs` on komento, jota käytetään ext2, ext3 ja ext4 tiedostojärjestelmien säätämiseen ja konfiguroimiseen. Sen avulla voit muuttaa tiedostojärjestelmän asetuksia, kuten varmuuskopiointiaikoja, käyttöoikeuksia ja muita parametreja, jotka vaikuttavat tiedostojärjestelmän toimintaan.

## Käyttö
Perussyntaksi komennolle on seuraava:

```bash
tune2fs [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c <n>`: Määrittää, kuinka monta kertaa tiedostojärjestelmä voidaan käyttää ennen kuin se vaatii tarkistuksen.
- `-i <aika>`: Asettaa aikarajan, jonka jälkeen tiedostojärjestelmä tarkistetaan.
- `-m <prosentti>`: Määrittää varatulle tilalle prosenttiosuuden, joka on varattava järjestelmän käyttäjille.
- `-L <nimi>`: Muuttaa tiedostojärjestelmän nimeä.
- `-O <ominaisuus>`: Lisää tai poistaa tiedostojärjestelmän ominaisuuksia.

## Yleiset esimerkit
### 1. Tiedostojärjestelmän tarkistuksen aikarajan asettaminen
```bash
tune2fs -i 7d /dev/sda1
```
Tämä asettaa tiedostojärjestelmän tarkistuksen aikarajaksi seitsemän päivää.

### 2. Varatulle tilalle prosenttiosuuden määrittäminen
```bash
tune2fs -m 5 /dev/sda1
```
Tämä varaa 5% tilasta järjestelmän käyttäjille.

### 3. Tiedostojärjestelmän nimen muuttaminen
```bash
tune2fs -L UusiNimi /dev/sda1
```
Tämä muuttaa tiedostojärjestelmän nimen "UusiNimi":ksi.

### 4. Tarkistusten määrän asettaminen
```bash
tune2fs -c 20 /dev/sda1
```
Tämä asettaa, että tiedostojärjestelmää voidaan käyttää 20 kertaa ennen tarkistusta.

## Vinkit
- Varmista, että tiedostojärjestelmä ei ole käytössä, kun käytät `tune2fs`-komentoa, jotta vältät mahdolliset tietojen menetykset.
- Käytä `-l`-vaihtoehtoa nähdäksesi tiedostojärjestelmän nykyiset asetukset ennen muutosten tekemistä.
- Suorita säännöllisiä varmuuskopioita ennen suuria muutoksia tiedostojärjestelmässä.