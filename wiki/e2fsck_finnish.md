# [Linux] Bash e2fsck käyttö: Tiedostojärjestelmän tarkistus ja korjaus

## Yleiskatsaus
e2fsck-komento on työkalu, jota käytetään Linux-järjestelmissä tiedostojärjestelmien tarkistamiseen ja korjaamiseen. Se tarkistaa ja korjaa Ext2-, Ext3- ja Ext4-tiedostojärjestelmiä, varmistaen, että tiedostojärjestelmä on eheä ja toimiva.

## Käyttö
Perussyntaksi e2fsck-komennolle on seuraava:

```bash
e2fsck [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-p`: Suorittaa automaattisen tarkistuksen ilman käyttäjän vuorovaikutusta.
- `-f`: Pakottaa tarkistuksen, vaikka tiedostojärjestelmä näyttäisi olevan kunnossa.
- `-y`: Vastaa automaattisesti "kyllä" kaikkiin kysymyksiin, jotka e2fsck esittää.
- `-c`: Tarkistaa tiedostojärjestelmän lohkot ja etsii huonoja lohkoja.
- `-n`: Suorittaa tarkistuksen ilman muutoksia tiedostojärjestelmään.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä e2fsck-komennosta:

1. **Perustarkistus**:
   Tarkista tiedostojärjestelmä, joka on liitetty `/dev/sda1`:
   ```bash
   e2fsck /dev/sda1
   ```

2. **Pakotettu tarkistus**:
   Pakota tarkistus, vaikka tiedostojärjestelmä olisi ehjä:
   ```bash
   e2fsck -f /dev/sda1
   ```

3. **Automaattinen korjaus**:
   Suorita tarkistus ja korjaa automaattisesti kaikki löydetyt ongelmat:
   ```bash
   e2fsck -y /dev/sda1
   ```

4. **Huonojen lohkojen tarkistus**:
   Tarkista tiedostojärjestelmän lohkot huonojen lohkojen varalta:
   ```bash
   e2fsck -c /dev/sda1
   ```

## Vinkit
- Suosittelemme, että suoritat e2fsck:n vain, kun tiedostojärjestelmä ei ole liitettynä, jotta vältät mahdolliset tietojen menetykset.
- Varmista, että sinulla on varmuuskopiot tärkeistä tiedoista ennen tarkistusta tai korjausta.
- Käytä `-n`-vaihtoehtoa ensin, jos haluat nähdä, mitä muutoksia e2fsck aikoo tehdä, ennen kuin suoritat varsinaisen korjauksen.