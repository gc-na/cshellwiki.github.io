# [Linux] Bash exit käyttö: Poistuu shellistä tai skriptistä

## Overview
`exit`-komento Bashissa käytetään poistumaan shellistä tai skriptistä. Se voi myös palauttaa arvon, joka voi olla hyödyllinen, kun halutaan ilmoittaa ohjelman suorituskyvystä tai virheistä.

## Usage
Perussyntaksi `exit`-komennolle on seuraava:

```bash
exit [options] [arguments]
```

## Common Options
- `n` : Määrittää poistumiskoodin, joka on kokonaisluku (0-255). Oletusarvo on 0, mikä tarkoittaa onnistunutta suoritusta.
- `-` : Käytetään, kun halutaan palauttaa virhekoodi, mutta tämä on harvinaisempaa.

## Common Examples

### Esimerkki 1: Poistuminen ilman koodia
```bash
exit
```
Tämä komento sulkee nykyisen shell-istunnon ja palauttaa oletusarvon 0.

### Esimerkki 2: Poistuminen tietyllä koodilla
```bash
exit 1
```
Tämä komento sulkee shellin ja palauttaa arvon 1, mikä voi viitata virhetilanteeseen.

### Esimerkki 3: Poistuminen skriptistä
```bash
#!/bin/bash
echo "Skripti käynnistyy."
exit 0
```
Tässä skriptissä tulostuu viesti ja sitten poistutaan onnistuneesti.

### Esimerkki 4: Poistuminen virhetilanteessa
```bash
#!/bin/bash
if [ ! -f "tiedosto.txt" ]; then
    echo "Virhe: tiedostoa ei löydy!"
    exit 2
fi
```
Tässä skriptissä tarkistetaan, onko tiedostoa olemassa. Jos ei, tulostuu virheilmoitus ja poistumiskoodi 2 palautetaan.

## Tips
- Käytä `exit`-komentoa skriptin lopussa ilmoittaaksesi suorituksen onnistumisesta tai epäonnistumisesta.
- Muista, että palautettavat koodit voivat olla hyödyllisiä, kun käytät skriptejä toisten ohjelmien kanssa.
- Vältä `exit`-komennon käyttöä interaktiivisessa shellissä, ellei se ole tarkoituksellista, sillä se sulkee koko istunnon.