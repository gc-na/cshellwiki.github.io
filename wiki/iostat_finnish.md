# [Linux] Bash iostat käyttö: Näyttää järjestelmän I/O-tilastot

## Yleiskatsaus
`iostat`-komento on työkalu, joka näyttää tietokoneen I/O-tilastot, mukaan lukien levyn ja prosessorin käyttöasteet. Se auttaa järjestelmänvalvojia ja käyttäjiä arvioimaan järjestelmän suorituskykyä ja tunnistamaan mahdollisia pullonkauloja.

## Käyttö
Perussyntaksi iostat-komennolle on seuraava:

```
iostat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Näyttää vain prosessorin käyttötilastot.
- `-d`: Näyttää vain levyn käyttötilastot.
- `-x`: Näyttää laajennetut levyn käyttötilastot.
- `-m`: Näyttää tilastot megatavuina.
- `-t`: Näyttää aikaleiman jokaiselle tulostetulle riville.

## Yleiset esimerkit
### Esimerkki 1: Perustilastot
Näyttää perus I/O-tilastot:
```bash
iostat
```

### Esimerkki 2: Prosessorin käyttötilastot
Näyttää vain prosessorin käyttötilastot:
```bash
iostat -c
```

### Esimerkki 3: Laajennetut levyn käyttötilastot
Näyttää laajennetut levyn käyttötilastot:
```bash
iostat -x
```

### Esimerkki 4: Tilastot megatavuina
Näyttää tilastot megatavuina:
```bash
iostat -m
```

### Esimerkki 5: Aikaleimalla
Näyttää tilastot aikaleiman kanssa:
```bash
iostat -t
```

## Vinkit
- Käytä `iostat`-komentoa yhdessä muiden järjestelmänvalvontatyökalujen, kuten `top` tai `vmstat`, kanssa saadaksesi kattavamman kuvan järjestelmän suorituskyvystä.
- Aseta komento ajastetuksi, esimerkiksi `iostat 5`, jolloin se näyttää tilastot viiden sekunnin välein.
- Tarkista säännöllisesti I/O-tilastoja, erityisesti suurten kuormitusten aikana, jotta voit tunnistaa mahdolliset ongelmat ajoissa.