# [Linux] Bash while käyttö: Toistaa komentoja ehtojen mukaan

## Overview
`while`-komento Bashissa on silmukka, joka toistaa tiettyjä komentoja niin kauan kuin annettu ehto on tosi. Tämä on hyödyllistä, kun halutaan suorittaa toimenpiteitä toistuvasti, kunnes tietty olosuhde muuttuu.

## Usage
Perussyntaksi `while`-komennolle on seuraava:

```bash
while [ehto]; do
    komennot
done
```

## Common Options
`while`-komennolla ei ole erityisiä vaihtoehtoja, mutta ehtojen määrittelyyn voi käyttää erilaisia vertailu- ja loogisia operaattoreita, kuten:
- `-eq`: on yhtä suuri kuin
- `-ne`: ei ole yhtä suuri kuin
- `-lt`: on pienempi kuin
- `-gt`: on suurempi kuin
- `-le`: on pienempi tai yhtä suuri kuin
- `-ge`: on suurempi tai yhtä suuri kuin

## Common Examples

### Esimerkki 1: Laskuri
Tässä esimerkissä käytämme `while`-silmukkaa laskemaan lukuja yhdestä kymmeneen.

```bash
count=1
while [ $count -le 10 ]; do
    echo "Luku: $count"
    ((count++))
done
```

### Esimerkki 2: Käyttäjän syötteen käsittely
Tässä esimerkissä kysytään käyttäjältä syötettä, kunnes hän syöttää "lopeta".

```bash
input=""
while [ "$input" != "lopeta" ]; do
    read -p "Syötä jotain (lopeta lopettaa): " input
    echo "Syötit: $input"
done
```

### Esimerkki 3: Tiedoston rivien lukeminen
Tässä esimerkissä luetaan tiedoston rivejä yksi kerrallaan.

```bash
file="esimerkki.txt"
while IFS= read -r line; do
    echo "Rivi: $line"
done < "$file"
```

## Tips
- Varmista, että ehtosi muuttuu jossain vaiheessa, jotta silmukka ei jää ikuisesti päälle.
- Käytä `break`-komentoa, jos haluat keskeyttää silmukan tietyissä olosuhteissa.
- Hyödynnä `sleep`-komentoa silmukoissa, joissa on odotusaikoja, jotta prosessorin kuormitus pysyy alhaisena.