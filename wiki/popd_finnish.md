# [Linux] Bash popd käyttö: Siirtyy takaisin edelliseen hakemistoon

## Yleiskatsaus
`popd`-komento on Bash-komento, joka siirtää käyttäjän takaisin edelliseen työskentelyhakemistoon, joka on tallennettu hakemistorakenteeseen. Se toimii yhdessä `pushd`-komennon kanssa, joka lisää hakemiston pinoon.

## Käyttö
Perussyntaksi `popd`-komennolle on seuraava:

```bash
popd [options] [arguments]
```

## Yleiset vaihtoehdot
- `-n`: Älä muuta nykyistä hakemistoa, vain tulosta pino.
- `+N`: Siirry hakemistoon, joka on N-askelta pinoon (esim. `+1` tarkoittaa ensimmäistä hakemistoa).
- `-N`: Siirry hakemistoon, joka on N-askelta pinon loppupäästä (esim. `-1` tarkoittaa viimeistä hakemistoa).

## Yleiset esimerkit

### Esimerkki 1: Siirtyminen takaisin edelliseen hakemistoon
```bash
pushd /home/kayttaja/dokumentit
# Tehdään jotain dokumenttien kanssa
popd
```

### Esimerkki 2: Siirtyminen tiettyyn hakemistoon pinosta
```bash
pushd /home/kayttaja/dokumentit
pushd /var/log
popd +1
```

### Esimerkki 3: Nykyisen hakemiston näyttäminen ilman siirtymistä
```bash
pushd /home/kayttaja
popd -n
```

## Vinkit
- Käytä `pushd` ja `popd` yhdessä tehokkaasti, jotta voit navigoida helposti useiden hakemistojen välillä.
- Hyödynnä `+N` ja `-N` vaihtoehtoja, jos haluat siirtyä suoraan tiettyyn hakemistoon pinosta.
- Muista tarkistaa nykyinen hakemisto komennolla `pwd` varmistaaksesi, että olet oikeassa paikassa.