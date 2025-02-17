# [Linux] Bash chkconfig käyttö: Palveluiden hallinta

## Yleiskatsaus
`chkconfig` on komento, jota käytetään Linux-järjestelmissä palveluiden (daemonien) hallintaan. Sen avulla voit tarkistaa, muuttaa ja hallita palveluiden käynnistymistä eri käyttöjärjestelmän käynnistystasoilla.

## Käyttö
Perussyntaksi `chkconfig`-komennolle on seuraava:

```bash
chkconfig [valinnat] [argumentit]
```

## Yleiset valinnat
- `--list`: Näyttää kaikki palvelut ja niiden nykyiset käynnistystasot.
- `--add`: Lisää uuden palvelun `chkconfig`-hallintaan.
- `--del`: Poistaa palvelun `chkconfig`-hallinnasta.
- `--level <taso>`: Määrittää, millä käyttöjärjestelmän tasoilla palvelu käynnistyy (esim. 2345).
- `on`: Ota palvelu käyttöön.
- `off`: Poista palvelu käytöstä.

## Yleiset esimerkit

1. **Näytä kaikki palvelut ja niiden käynnistystasot:**
   ```bash
   chkconfig --list
   ```

2. **Lisää uusi palvelu:**
   ```bash
   chkconfig --add myservice
   ```

3. **Poista palvelu hallinnasta:**
   ```bash
   chkconfig --del myservice
   ```

4. **Ota palvelu käyttöön tietyillä tasoilla:**
   ```bash
   chkconfig --level 2345 myservice on
   ```

5. **Poista palvelu käytöstä:**
   ```bash
   chkconfig --level 2345 myservice off
   ```

## Vinkit
- Varmista, että palvelun skripti on sijoitettu oikeaan hakemistoon (`/etc/init.d/`), jotta `chkconfig` voi hallita sitä.
- Käytä `chkconfig --list` -komentoa säännöllisesti varmistaaksesi, että kaikki tarvittavat palvelut ovat oikeilla tasoilla.
- Muista, että muutokset, jotka teet `chkconfig`-komennolla, vaikuttavat vain palveluiden käynnistymiseen järjestelmän käynnistyksen yhteydessä.