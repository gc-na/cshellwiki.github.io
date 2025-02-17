# [Linux] Bash tr käyttö: Merkkien muuntaminen ja poistaminen

## Yleiskatsaus
`tr`-komento on Bashissa käytettävä työkalu, joka muuntaa tai poistaa merkkejä syötteestä. Se on erityisen hyödyllinen tekstinkäsittelyssä, kun halutaan muuttaa tai suodattaa tiettyjä merkkejä.

## Käyttö
Perussyntaksi `tr`-komennolle on seuraava:

```bash
tr [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d`: Poistaa määritellyt merkit syötteestä.
- `-s`: Tiivistää peräkkäiset merkit yhdeksi.
- `-c`: Käyttää täydentäviä merkkejä, eli muuntaa kaikki muut merkit kuin määritellyt.
- `-t`: Rajoittaa muunnoksen vain ensimmäiseen esiintymään.

## Yleiset esimerkit

### Merkkien muuntaminen
Muuta pieniä kirjaimia isoiksi:

```bash
echo "tervetuloa" | tr 'a-z' 'A-Z'
```

### Merkkien poistaminen
Poista kaikki vokaalit tekstistä:

```bash
echo "tervetuloa" | tr -d 'aeiou'
```

### Peräkkäisten merkkien tiivistäminen
Tiivistä peräkkäiset välilyönnit yhdeksi:

```bash
echo "Tämä   on   esimerkki" | tr -s ' '
```

### Merkkien täydentäminen
Muuta kaikki merkit, jotka eivät ole numeroita, tyhjiksi:

```bash
echo "Hinta on 100 euroa" | tr -c '0-9' ' '
```

## Vinkit
- Käytä `echo`-komentoa yhdessä `tr`:n kanssa testataksesi nopeasti erilaisia muunnoksia.
- Muista, että `tr` ei voi käsitellä tiedostoja suoraan. Käytä putkia tai ohjaa syöte tiedostosta.
- Varmista, että käytät oikeita merkkejä, erityisesti kun käytät vaihtoehtoja, kuten `-c` tai `-d`, jotta et poista tai muuta vahingossa tärkeitä merkkejä.