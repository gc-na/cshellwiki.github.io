# [Linux] Bash mpstat käyttö: CPU:n käyttötilastojen näyttäminen

## Yleiskatsaus
mpstat-komento on osa sysstat-pakettia ja se näyttää CPU:n käyttötilastot. Se tarjoaa tietoa prosessorin kuormituksesta, mikä auttaa järjestelmänvalvojia ja käyttäjiä ymmärtämään järjestelmän suorituskykyä ja mahdollisia pullonkauloja.

## Käyttö
Perussyntaksi mpstat-komennolle on seuraava:
```
mpstat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-P ALL`: Näyttää kaikkien prosessoriydinten tilastot.
- `-u`: Näyttää vain käyttötilastot.
- `-h`: Näyttää tulokset ihmislukemassa muodossa.
- `interval`: Aika, jonka jälkeen tilastot päivitetään (esim. 1 sekunti).
- `count`: Kuinka monta kertaa tilastot näytetään.

## Yleiset esimerkit
1. Näytä kaikkien prosessoriydinten tilastot:
   ```bash
   mpstat -P ALL
   ```

2. Näytä CPU:n käyttötilastot 1 sekunnin välein 5 kertaa:
   ```bash
   mpstat 1 5
   ```

3. Näytä vain käyttötilastot ihmislukemassa muodossa:
   ```bash
   mpstat -u -h
   ```

4. Näytä tilastot vain yhdelle prosessoriytimelle (esim. ydin 0):
   ```bash
   mpstat -P 0
   ```

## Vinkit
- Käytä `mpstat`-komentoa yhdessä muiden suorituskykytyökalujen, kuten `top` tai `htop`, kanssa saadaksesi kattavamman kuvan järjestelmän tilasta.
- Seuraa prosessorin kuormitusta säännöllisesti, erityisesti kuormitetuissa ympäristöissä, jotta voit tunnistaa mahdolliset ongelmat ajoissa.
- Hyödynnä `-h`-vaihtoehtoa, jos haluat tulokset helposti luettavassa muodossa, erityisesti suurilla tietomäärillä.