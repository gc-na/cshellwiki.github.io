# [Linux] Bash ulimit käyttö: Rajoittaa resurssien käyttöä

## Yleiskatsaus
`ulimit`-komento on Bash-shellin työkalu, jota käytetään resurssirajoitusten asettamiseen käyttäjäprosessille. Se mahdollistaa erilaisten järjestelmäresurssien, kuten muistin ja prosessien määrän, rajoittamisen, mikä voi auttaa estämään yksittäisten prosessien liiallista käyttöä ja parantamaan järjestelmän vakautta.

## Käyttö
Perussyntaksi `ulimit`-komennolle on seuraava:

```bash
ulimit [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a`: Näyttää kaikki nykyiset rajoitukset.
- `-c`: Asettaa tai näyttää ydinmuistidumpin koon.
- `-d`: Asettaa tai näyttää prosessin datamuistin koon.
- `-f`: Asettaa tai näyttää tiedostojen maksimikoon.
- `-l`: Asettaa tai näyttää ladattavien tiedostojen maksimikoon.
- `-m`: Asettaa tai näyttää prosessin muistin koon.
- `-n`: Asettaa tai näyttää avattujen tiedostojen maksimimäärän.
- `-s`: Asettaa tai näyttää pinojen koon.
- `-t`: Asettaa tai näyttää prosessin maksimiajan sekunteina.
- `-u`: Asettaa tai näyttää prosessien maksimimäärän käyttäjälle.

## Yleiset esimerkit
### Näytä kaikki rajoitukset
```bash
ulimit -a
```

### Aseta maksimikoko tiedostolle
```bash
ulimit -f 1024
```
Tämä asettaa maksimikoon 1024 kilotavuksi.

### Aseta avattujen tiedostojen maksimimäärä
```bash
ulimit -n 2048
```
Tämä asettaa avattujen tiedostojen maksimimääräksi 2048.

### Aseta prosessin maksimiaika
```bash
ulimit -t 300
```
Tämä rajoittaa prosessin suoritusaikaa 300 sekuntiin.

## Vinkit
- Tarkista rajoitukset säännöllisesti, erityisesti ennen suurten prosessien käynnistämistä.
- Käytä `ulimit -a` -komentoa ymmärtääksesi nykyiset asetukset ennen muutoksia.
- Muista, että rajoitukset voivat vaikuttaa ohjelmien toimintaan, joten säädä niitä huolellisesti.
- Voit asettaa `ulimit`-komennon käyttäjäprofiiliin, jotta rajoitukset ovat voimassa aina, kun avaat uuden istunnon.