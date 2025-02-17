# [Linux] Bash netstat käyttö: Verkkoyhteyksien tarkastelu

## Yleiskatsaus
`netstat` on komento, jota käytetään verkkoyhteyksien, reititystaulukoiden ja verkkoprotokollien tilan tarkasteluun. Se tarjoaa tietoa aktiivisista yhteyksistä, avoimista porteista ja muista verkkoasetuksista.

## Käyttö
Perussyntaksi `netstat`-komennolle on seuraava:

```bash
netstat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a`: Näyttää kaikki yhteydet ja kuuntelupisteet.
- `-t`: Näyttää vain TCP-yhteydet.
- `-u`: Näyttää vain UDP-yhteydet.
- `-n`: Näyttää osoitteet ja portit numeerisessa muodossa.
- `-l`: Näyttää vain kuuntelevat yhteydet.

## Yleiset esimerkit
1. Näytä kaikki aktiiviset yhteydet:
   ```bash
   netstat -a
   ```

2. Näytä vain TCP-yhteydet:
   ```bash
   netstat -t
   ```

3. Näytä vain UDP-yhteydet numeerisessa muodossa:
   ```bash
   netstat -un
   ```

4. Näytä kuuntelevat portit:
   ```bash
   netstat -l
   ```

5. Näytä reititystaulu:
   ```bash
   netstat -r
   ```

## Vinkit
- Käytä `-p`-vaihtoehtoa nähdäksesi, mitkä prosessit käyttävät tiettyjä yhteyksiä.
- Yhdistä `grep`-komento suodattaaksesi tuloksia, esimerkiksi:
  ```bash
  netstat -tuln | grep 80
  ```
- Muista, että `netstat` voi vaatia järjestelmänvalvojan oikeuksia joissakin järjestelmissä, joten käytä `sudo`-komentoa tarvittaessa.