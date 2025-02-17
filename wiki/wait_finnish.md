# [Linux] Bash wait käyttö: Odottaa prosessien valmistumista

## Overview
`wait`-komento on Bashin sisäinen komento, joka odottaa, että yksi tai useampi taustaprosessi valmistuu. Se palauttaa prosessin lopullisen tilan, mikä on hyödyllistä skripteissä, joissa halutaan varmistaa, että tietyt prosessit ovat valmiita ennen seuraavien komentojen suorittamista.

## Usage
Perussyntaksi `wait`-komennolle on seuraava:

```bash
wait [options] [arguments]
```

## Common Options
- `-n`: Odottaa ensimmäisen valmistuvan prosessin.
- `-p`: Odottaa tiettyä prosessia, jonka tunnus (PID) on annettu argumenttina.

## Common Examples

### Esimerkki 1: Odota kaikkia taustaprosesseja
```bash
#!/bin/bash
sleep 5 &
sleep 3 &
wait
echo "Kaikki prosessit ovat valmiita."
```

### Esimerkki 2: Odota tiettyä prosessia
```bash
#!/bin/bash
sleep 5 &
PID=$!
echo "Odotetaan prosessia PID: $PID"
wait $PID
echo "Prosessi $PID on valmis."
```

### Esimerkki 3: Odota ensimmäistä valmistuvaa prosessia
```bash
#!/bin/bash
sleep 5 &
sleep 3 &
wait -n
echo "Ensimmäinen prosessi on valmis."
```

## Tips
- Käytä `wait`-komentoa skripteissä, joissa on useita taustaprosesseja, varmistaaksesi, että kaikki tarvittavat prosessit ovat valmiita ennen jatkamista.
- Hyödynnä PID:tä, jos haluat odottaa vain tiettyä prosessia, mikä voi parantaa skriptin tehokkuutta.
- Muista, että `wait` palauttaa prosessin tilan, joten voit tarkistaa, onnistuiko prosessi vai ei, ja reagoida sen mukaan.