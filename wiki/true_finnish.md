# [Linux] Bash true käyttö: palauttaa aina onnistuneen tilan

## Overview
`true` on Bash-komento, joka palauttaa aina onnistuneen tilan (0). Sitä käytetään usein skripteissä ja komentoissa, joissa tarvitaan komento, joka ei tee mitään, mutta joka voi toimia onnistuneena tilana.

## Usage
Perussyntaksi komennolle on seuraava:
```bash
true [options] [arguments]
```

## Common Options
`true`-komennolla ei ole erityisiä vaihtoehtoja, koska se ei vaadi argumentteja eikä sillä ole lisäasetuksia. Se toimii yksinkertaisesti palauttamalla onnistuneen tilan.

## Common Examples
Tässä on muutamia käytännön esimerkkejä `true`-komennon käytöstä:

1. **Yksinkertainen käyttö:**
   ```bash
   true
   ```
   Tämä komento palauttaa onnistuneen tilan.

2. **Käytetään osana ehtolauseketta:**
   ```bash
   if true; then
       echo "Tämä tulostuu aina."
   fi
   ```
   Tässä `if`-lause palauttaa aina totta, joten tulostus tapahtuu aina.

3. **Silmukka, joka ei koskaan lopu:**
   ```bash
   while true; do
       echo "Tämä toistuu ikuisesti."
       sleep 1
   done
   ```
   Tämä komento toistaa viestin ikuisesti, kunnes se keskeytetään.

4. **Käytetään skriptissä:**
   ```bash
   #!/bin/bash
   while true; do
       echo "Skripti toimii."
       sleep 2
   done
   ```
   Tämä skripti tulostaa viestin joka toinen sekunti.

## Tips
- `true` on hyödyllinen, kun haluat testata ehtoja tai silmukoita ilman, että sinun tarvitsee käyttää muita komentoja.
- Voit yhdistää `true`-komennon muihin komentoihin, kuten `&&`-operaattoriin, varmistaaksesi, että seuraava komento suoritetaan aina.
- Käytä `true`-komentoa skripteissä, joissa haluat varmistaa, että jokin osa koodista suoritetaan riippumatta edellisistä komentoista.