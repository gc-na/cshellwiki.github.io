# [Linux] Bash ss käyttö: Verkko- ja sokettitietojen tarkastelu

## Yleiskatsaus
`ss` (socket statistics) on komento, jota käytetään verkko- ja sokettitietojen tarkasteluun Linux-järjestelmissä. Se tarjoaa tietoa avoimista yhteyksistä, soketeista ja niiden tilasta, mikä on hyödyllistä verkon diagnosoinnissa ja hallinnassa.

## Käyttö
Perussyntaksi `ss`-komennolle on seuraava:

```bash
ss [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-t`: Näyttää vain TCP-yhteydet.
- `-u`: Näyttää vain UDP-yhteydet.
- `-l`: Näyttää vain kuuntelevat soketit.
- `-p`: Näyttää prosessit, jotka käyttävät soketteja.
- `-n`: Näyttää osoitteet ja portit numeerisessa muodossa.

## Yleiset esimerkit
- Näytä kaikki avoimet TCP-yhteydet:
  ```bash
  ss -t
  ```

- Näytä kaikki kuuntelevat soketit:
  ```bash
  ss -l
  ```

- Näytä kaikki UDP-yhteydet:
  ```bash
  ss -u
  ```

- Näytä soketit prosessitietojen kanssa:
  ```bash
  ss -p
  ```

- Näytä kaikki yhteydet numeerisessa muodossa:
  ```bash
  ss -n
  ```

## Vinkit
- Käytä `ss`-komentoa yhdessä `grep`-komennon kanssa suodattaaksesi tuloksia, esimerkiksi:
  ```bash
  ss -t | grep 80
  ```
- Voit yhdistää useita vaihtoehtoja, kuten:
  ```bash
  ss -tunlp
  ```
- Muista, että `ss` on nopeampi ja tehokkaampi vaihtoehto verrattuna vanhempiin komentoihin, kuten `netstat`.