# [Linux] Bash continue käyttö: Jatkaa silmukkaa

## Yleiskatsaus
`continue`-komento Bashissa käytetään silmukoissa, kuten `for`, `while` ja `until`, ohittamaan nykyinen iteraatio ja siirtymään seuraavaan. Tämä on hyödyllistä, kun haluat ohittaa tiettyjä ehtoja silmukan sisällä.

## Käyttö
Perussyntaksi `continue`-komennolle on seuraava:

```bash
continue [n]
```

Missä `n` on valinnainen argumentti, joka määrittää, kuinka monta silmukan iteraatiota ohitetaan. Oletusarvo on 1.

## Yleiset vaihtoehdot
- `n`: Määrittää, kuinka monta iteraatiota ohitetaan. Esimerkiksi `continue 2` ohittaa kaksi seuraavaa iteraatiota.

## Yleiset esimerkit

### Esimerkki 1: Perussilmukka
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    continue
  fi
  echo $i
done
```
Tässä esimerkissä luku 3 ohitetaan, ja tulostus on 1, 2, 4, 5.

### Esimerkki 2: While-silmukka
```bash
count=1
while [ $count -le 5 ]; do
  if [ $count -eq 2 ]; then
    count=$((count + 1))
    continue
  fi
  echo $count
  count=$((count + 1))
done
```
Tässä esimerkissä luku 2 ohitetaan, ja tulostus on 1, 3, 4, 5.

### Esimerkki 3: Continue useamman iteraation ohittamiseen
```bash
for i in {1..10}; do
  if [ $((i % 2)) -eq 0 ]; then
    continue 2
  fi
  echo $i
done
```
Tässä esimerkissä kaikki parilliset luvut ohitetaan, ja tulostus on 1, 3, 5, 7, 9.

## Vinkit
- Käytä `continue`-komentoa harkiten, jotta silmukan logiikka pysyy selkeänä.
- Varmista, että silmukan ehtoja on helppo seurata, jotta vältät odottamattomat tulokset.
- Testaa silmukoita pienillä arvoilla ennen suurempien tietomäärien käsittelyä varmistaaksesi, että `continue` toimii odotetusti.