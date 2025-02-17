# [Linux] Bash expr käyttö: laskentatehtävien suorittaminen

## Yleiskatsaus
`expr` on Bash-komento, jota käytetään yksinkertaisten laskentatehtävien ja merkkijonojen käsittelyyn. Se voi suorittaa aritmeettisia laskelmia, vertailla arvoja ja käsitellä merkkijonoja.

## Käyttö
Perussyntaksi `expr`-komennolle on seuraava:

```bash
expr [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `+` : Yhdistelee kaksi lukua.
- `-` : Vähentää toisen luvun ensimmäisestä.
- `*` : Kertoo kaksi lukua (huomaa, että * on pakko paeta).
- `/` : Jakaa ensimmäisen luvun toisella.
- `%` : Laskee jakolaskun jäljelle jäävän osan.
- `=` : Vertaa kahta arvoa.
- `!=` : Tarkistaa, ovatko kaksi arvoa eri.

## Yleiset esimerkit
### Yhdisteleminen
```bash
expr 5 + 3
```
Tämä palauttaa arvon `8`.

### Vähentäminen
```bash
expr 10 - 4
```
Tämä palauttaa arvon `6`.

### Kertominen
```bash
expr 7 \* 6
```
Tämä palauttaa arvon `42`.

### Jakaminen
```bash
expr 20 / 4
```
Tämä palauttaa arvon `5`.

### Jäljelle jäävä osa
```bash
expr 10 % 3
```
Tämä palauttaa arvon `1`.

### Merkkijonojen vertailu
```bash
expr "hello" = "hello"
```
Tämä palauttaa arvon `1`, koska merkkijonot ovat samat.

## Vinkit
- Muista paeta kertolaskuoperaattoria `*` käyttämällä `\`-merkkiä.
- Käytä sulkuja monimutkaisemmissa laskelmissa varmistaaksesi oikean laskujärjestyksen.
- `expr` ei ole yhtä tehokas kuin muut laskentatyökalut, kuten `bc` tai `awk`, joten harkitse niiden käyttöä monimutkaisemmissa laskentatehtävissä.