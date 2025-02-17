# [Linux] Bash docker-compose käyttö: Hallitse Docker-sovelluksia helposti

## Yleiskatsaus
`docker-compose` on työkalu, joka mahdollistaa useiden Docker-konttien hallinnan yhdellä komennolla. Sen avulla voit määrittää ja käynnistää monimutkaisempia sovelluksia, jotka koostuvat useista kontista, käyttämällä yksinkertaista YAML-muotoista konfiguraatiota.

## Käyttö
Perussyntaksi `docker-compose` -komennolle on seuraava:

```bash
docker-compose [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `up`: Käynnistää määritellyt kontit.
- `down`: Pysäyttää ja poistaa kontit.
- `build`: Rakentaa tai päivittää palvelut.
- `logs`: Näyttää konttien lokitiedot.
- `exec`: Suorittaa komento käynnissä olevassa kontissa.

## Yleiset esimerkit
### Konttien käynnistäminen
Käynnistä kaikki palvelut, jotka on määritelty `docker-compose.yml` -tiedostossa:

```bash
docker-compose up
```

### Konttien pysäyttäminen
Pysäytä ja poista kaikki käynnissä olevat kontit:

```bash
docker-compose down
```

### Lokitietojen tarkastelu
Näytä lokitiedot kaikista palveluista:

```bash
docker-compose logs
```

### Komennon suorittaminen kontissa
Suorita komento `web`-palvelussa:

```bash
docker-compose exec web bash
```

### Rakentaminen ja käynnistäminen yhdessä
Rakennetaan ja käynnistetään palvelut yhdellä komennolla:

```bash
docker-compose up --build
```

## Vinkit
- Käytä `-d` -vaihtoehtoa `up`-komennossa, jos haluat käynnistää kontit taustalla (detached mode).
- Varmista, että `docker-compose.yml` -tiedosto on oikein määritelty, jotta kaikki palvelut toimivat odotetusti.
- Hyödynnä ympäristömuuttujia `docker-compose.yml` -tiedostossa konfiguraation hallintaan eri ympäristöissä.