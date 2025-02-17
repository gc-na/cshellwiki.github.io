# [Linux] Bash käyttäjät: Käyttäjätietojen näyttäminen

## Yleiskatsaus
`users`-komento näyttää nykyisten käyttäjien nimet, jotka ovat kirjautuneet järjestelmään. Se on hyödyllinen työkalu, kun halutaan nopeasti tarkistaa, ketkä ovat aktiivisesti kirjautuneina.

## Käyttö
Perussyntaksi `users`-komennolle on seuraava:

```bash
users [options] [arguments]
```

## Yleiset vaihtoehdot
- `-a`: Näyttää kaikki käyttäjät, mukaan lukien ne, jotka ovat kirjautuneet sisään useita kertoja.
- `-r`: Näyttää vain rekisteröidyt käyttäjät.

## Yleiset esimerkit
1. **Nykyisten käyttäjien näyttäminen**:
   ```bash
   users
   ```

2. **Kaikkien käyttäjien näyttäminen**:
   ```bash
   users -a
   ```

3. **Rekisteröityjen käyttäjien näyttäminen**:
   ```bash
   users -r
   ```

## Vinkit
- Käytä `who`-komentoa yhdessä `users`-komennon kanssa saadaksesi lisätietoja käyttäjistä, kuten heidän kirjautumisaikansa ja IP-osoitteensa.
- Voit yhdistää `users`-komennon muihin komentoihin, kuten `wc -w`, saadaksesi tietää, kuinka monta käyttäjää on kirjautuneena:
  ```bash
  users | wc -w
  ```