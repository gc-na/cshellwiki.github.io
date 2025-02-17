# [Linux] Bash nice käyttö: Prosessien priorisointi

## Overview
`nice`-komento Bashissa mahdollistaa prosessien priorisoinnin, mikä tarkoittaa, että voit säätää, kuinka paljon CPU-aikaa prosessi saa verrattuna muihin prosesseihin. Tämä on erityisen hyödyllistä, kun haluat varmistaa, että tärkeämmät prosessit saavat enemmän resursseja.

## Usage
Perussyntaksi `nice`-komennolle on seuraava:

```bash
nice [options] [arguments]
```

## Common Options
- `-n, --adjustment=N`: Asettaa prioriteettitason. Voit käyttää positiivisia tai negatiivisia arvoja.
- `-h, --help`: Näyttää apuviestin ja käytön.
- `-V, --version`: Näyttää versionumeron.

## Common Examples
### 1. Suorita komento normaalilla prioriteetilla
```bash
nice echo "Tämä on normaali prioriteetti."
```

### 2. Suorita komento matalalla prioriteetilla
```bash
nice -n 10 sleep 60
```
Tässä komennossa `sleep`-prosessi saa matalamman prioriteetin, jolloin se ei häiritse muita prosesseja.

### 3. Suorita komento korkealla prioriteetilla
```bash
nice -n -5 ./tärkeä_prosessi
```
Tässä `tärkeä_prosessi` saa korkeamman prioriteetin, mikä voi olla hyödyllistä kriittisissä tilanteissa.

### 4. Tarkista prosessin prioriteetti
```bash
ps -o pid,ni,cmd -p <prosessi_id>
```
Tämä komento näyttää prosessin ID:n, prioriteetin ja komennon.

## Tips
- Käytä `nice`-komentoa yhdessä `nohup`-komennon kanssa, jos haluat, että prosessi jatkaa toimintaansa myös kirjautuessasi ulos.
- Varo asettamasta liian korkeaa prioriteettia muille prosesseille, sillä se voi vaikuttaa järjestelmän vakauteen.
- Voit tarkistaa prosessien prioriteetteja `top`-komennolla, joka näyttää reaaliaikaisia tietoja järjestelmän prosesseista.