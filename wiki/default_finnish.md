# [Linux] Bash oletuskomento: [tiedostojen listaus]

## Yleiskatsaus
`ls`-komento on yksi Bashin peruskomentoja, jota käytetään tiedostojen ja hakemistojen listaamiseen nykyisessä työskentelyhakemistossa. Se tarjoaa käyttäjälle mahdollisuuden nähdä, mitä tiedostoja ja kansioita on saatavilla.

## Käyttö
Perussyntaksi `ls`-komennolle on seuraava:

```bash
ls [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Näyttää tiedostot pitkänä listana, joka sisältää lisätietoja, kuten oikeudet, omistajan ja koon.
- `-a`: Näyttää myös piilotetut tiedostot, jotka alkavat pisteellä.
- `-h`: Näyttää tiedostokoot ihmislukuisessa muodossa (esim. Kt, Mt).
- `-R`: Listaa hakemistot ja niiden sisällön rekursiivisesti.

## Yleiset esimerkit
- Peruslistaus nykyisessä hakemistossa:
  ```bash
  ls
  ```

- Pitkä listaus, joka näyttää lisätietoja:
  ```bash
  ls -l
  ```

- Listaus, joka sisältää myös piilotetut tiedostot:
  ```bash
  ls -a
  ```

- Listaus, joka näyttää tiedostokoot ihmislukuisessa muodossa:
  ```bash
  ls -lh
  ```

- Rekursiivinen listaaminen kaikista hakemistoista ja tiedostoista:
  ```bash
  ls -R
  ```

## Vinkit
- Käytä `ls -lh` -komentoa saadaksesi helposti luettavat tiedostokoot, mikä on erityisen hyödyllistä suurten hakemistojen tarkastelussa.
- Yhdistä vaihtoehtoja, kuten `ls -la`, saadaksesi sekä piilotetut tiedostot että lisätiedot yhdellä komennolla.
- Voit käyttää `tab`-näppäintä täydentämään tiedostonimiä, mikä nopeuttaa työskentelyäsi komentorivillä.