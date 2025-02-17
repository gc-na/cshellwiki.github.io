# [Linux] Bash whoami käyttö: Näyttää nykyisen käyttäjän nimen

## Yleiskatsaus
`whoami`-komento näyttää nykyisen käyttäjän nimen, joka on kirjautunut sisään järjestelmään. Tämä komento on hyödyllinen, kun haluat varmistaa, että olet oikeassa käyttäjätilissä, erityisesti monikäyttäjäympäristöissä.

## Käyttö
Perussyntaksi `whoami`-komennolle on seuraava:

```
whoami [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `--help`: Näyttää aputiedot ja käytön.
- `--version`: Näyttää ohjelman version.

## Yleiset esimerkit
1. **Nykyisen käyttäjän nimen näyttäminen:**
   ```bash
   whoami
   ```

2. **Apua komennosta:**
   ```bash
   whoami --help
   ```

3. **Version tarkistaminen:**
   ```bash
   whoami --version
   ```

## Vinkit
- Käytä `whoami`-komentoa ennen ja jälkeen käyttäjätilin vaihtamisen varmistaaksesi, että olet kirjautunut oikeaan tiliin.
- Tämä komento on erityisen hyödyllinen skripteissä, joissa haluat tarkistaa, mikä käyttäjä suorittaa skriptin.