# [Linux] Bash docker käyttö: Konttien hallinta ja sovellusten eristys

## Yleiskatsaus
Docker on työkalu, joka mahdollistaa sovellusten ja niiden riippuvuuksien pakkaamisen, jakamisen ja ajamisen konttien sisällä. Kontit ovat kevyitä, eristettyjä ympäristöjä, jotka toimivat samalla tavalla eri käyttöjärjestelmissä.

## Käyttö
Dockerin perussyntaksi on seuraava:

```bash
docker [options] [arguments]
```

## Yleiset vaihtoehdot
- `run`: Luo ja käynnistää uuden kontin.
- `ps`: Näyttää aktiiviset kontit.
- `stop`: Pysäyttää toimivan kontin.
- `rm`: Poistaa kontin.
- `images`: Listaa ladatut Docker-kuvat.

## Yleiset esimerkit
### Kontin käynnistäminen
Käynnistä uusi Docker-kontti Nginx-palvelimella:

```bash
docker run -d -p 80:80 nginx
```

### Aktiivisten konttien listaaminen
Näytä kaikki aktiiviset kontit:

```bash
docker ps
```

### Kontin pysäyttäminen
Pysäytä tietty kontti, jonka ID on `abc123`:

```bash
docker stop abc123
```

### Kontin poistaminen
Poista pysäytetty kontti:

```bash
docker rm abc123
```

### Kuvien listaaminen
Listaa kaikki ladatut Docker-kuvat:

```bash
docker images
```

## Vinkit
- Käytä `docker-compose`-työkalua monimutkaisempien sovellusten hallintaan, jotka koostuvat useista konteista.
- Varmista, että kontit ovat eristettyjä, jotta ne eivät vaikuta toisiinsa.
- Hyödynnä Dockerfile-tiedostoja automatisoidaksesi kontin rakentamisen ja konfiguroinnin.