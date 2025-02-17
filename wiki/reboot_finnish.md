# [Linux] Bash reboot käyttö: Käynnistää järjestelmän uudelleen

## Yleiskatsaus
`reboot`-komento on Linux-järjestelmissä käytettävä työkalu, joka käynnistää järjestelmän uudelleen. Tämä komento on hyödyllinen, kun halutaan päivittää järjestelmä tai kun järjestelmä tarvitsee uudelleenkäynnistyksen ongelmien ratkaisemiseksi.

## Käyttö
Perussyntaksi `reboot`-komennolle on seuraava:

```bash
reboot [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-f`: Pakottaa järjestelmän uudelleenkäynnistyksen ilman, että suljetaan avoimia sovelluksia.
- `-p`: Samalla kun järjestelmä käynnistetään uudelleen, se myös sammuttaa sen.
- `now`: Käynnistää järjestelmän uudelleen heti.
- `+m`: Aikatauluttaa uudelleenkäynnistyksen m minuutin kuluttua.

## Yleiset esimerkit
### Esimerkki 1: Järjestelmän uudelleenkäynnistys heti
```bash
reboot
```

### Esimerkki 2: Järjestelmän uudelleenkäynnistys pakolla
```bash
reboot -f
```

### Esimerkki 3: Järjestelmän uudelleenkäynnistys tietyn ajan kuluttua
```bash
reboot +5
```

### Esimerkki 4: Järjestelmän sammutus ja uudelleenkäynnistys
```bash
reboot -p
```

## Vinkit
- Varmista, että tallennat kaikki työt ennen `reboot`-komennon suorittamista, erityisesti jos käytät `-f`-vaihtoehtoa.
- Käytä `shutdown`-komentoa, jos haluat antaa käyttäjille varoituksen ennen uudelleenkäynnistystä.
- Tarkista järjestelmän lokit, jos kohtaat ongelmia uudelleenkäynnistyksen jälkeen, jotta voit diagnosoida mahdolliset virheet.