# [Linux] Bash ls käyttö: Näyttää tiedostot ja kansiot

## Yleiskatsaus
`ls`-komento on yksi yleisimmistä komentoista Linux- ja Unix-pohjaisissa käyttöjärjestelmissä. Se näyttää nykyisessä hakemistossa olevat tiedostot ja kansiot, mikä auttaa käyttäjiä navigoimaan tiedostojärjestelmässä.

## Käyttö
Perussyntaksi `ls`-komennolle on seuraava:

```bash
ls [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Näyttää tiedostot yksityiskohtaisessa muodossa, mukaan lukien tiedoston oikeudet, omistaja, koko ja viimeisin muokkausaika.
- `-a`: Näyttää myös piilotetut tiedostot, jotka alkavat pisteellä (.) 
- `-h`: Näyttää tiedostokoot ihmislukuisessa muodossa (esim. Kt, Mt).
- `-R`: Näyttää hakemistot ja niiden sisällön rekursiivisesti.
- `-t`: Järjestää tiedostot viimeisen muokkauksen mukaan.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `ls`-komennosta:

1. Näytä kaikki tiedostot ja kansiot nykyisessä hakemistossa:
   ```bash
   ls
   ```

2. Näytä kaikki tiedostot, mukaan lukien piilotetut:
   ```bash
   ls -a
   ```

3. Näytä tiedostot yksityiskohtaisessa muodossa:
   ```bash
   ls -l
   ```

4. Näytä tiedostot ihmislukuisessa muodossa:
   ```bash
   ls -lh
   ```

5. Näytä tiedostot rekursiivisesti:
   ```bash
   ls -R
   ```

6. Järjestä tiedostot viimeisen muokkauksen mukaan:
   ```bash
   ls -lt
   ```

## Vinkit
- Käytä `ls -lh` saadaksesi helposti luettavat tiedostokoot, erityisesti suurissa hakemistoissa.
- Voit yhdistää useita vaihtoehtoja, kuten `ls -la` näyttääksesi kaikki tiedostot yksityiskohtaisesti.
- Muista, että `ls`-komento ei näytä tiedostoja, joilla ei ole lukuoikeuksia nykyiselle käyttäjälle.