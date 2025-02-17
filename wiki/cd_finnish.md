# [Linux] Bash cd käyttö: Siirtyminen hakemistoon

## Yleiskatsaus
`cd` (change directory) -komento on Bashin peruskomento, jota käytetään hakemiston vaihtamiseen. Sen avulla voit navigoida tiedostojärjestelmässä ja siirtyä haluamaasi hakemistoon.

## Käyttö
Perussyntaksi `cd`-komennolle on seuraava:

```bash
cd [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `..` - Siirtyy edelliseen hakemistoon.
- `~` - Siirtyy käyttäjän kotihakemistoon.
- `-` - Siirtyy edelliseen hakemistoon, johon olit viimeksi siirtynyt.

## Yleiset esimerkit
- Siirtyminen kotihakemistoon:
  ```bash
  cd ~
  ```

- Siirtyminen edelliseen hakemistoon:
  ```bash
  cd ..
  ```

- Siirtyminen tiettyyn hakemistoon, esimerkiksi "asiakirjat":
  ```bash
  cd ~/asiakirjat
  ```

- Siirtyminen edelliseen hakemistoon:
  ```bash
  cd -
  ```

## Vinkit
- Käytä `pwd`-komentoa tarkistaaksesi nykyisen hakemistosi.
- Voit käyttää tab-näppäintä hakemistojen täydentämiseen, mikä nopeuttaa navigointia.
- Muista, että hakemistopolut ovat tapausherkkiä, joten varmista, että kirjoitat ne oikein.