# [Linux] Bash sqlite3 käyttö: SQLite-tietokannan hallinta

## Yleiskatsaus
`sqlite3` on komentorivipohjainen työkalu, joka mahdollistaa SQLite-tietokantojen luomisen, hallinnan ja kyselyjen suorittamisen. Se tarjoaa käyttäjille mahdollisuuden työskennellä tietokantojen kanssa suoraan terminaalista.

## Käyttö
Perussyntaksi `sqlite3`-komennolle on seuraava:

```bash
sqlite3 [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-help`: Näyttää apu- ja käyttöohjeet.
- `-version`: Näyttää käytössä olevan SQLite-version.
- `-init <tiedosto>`: Suorittaa annetun tiedoston komennot tietokannan alussa.
- `<tietokanta>`: Tietokannan nimi, jota halutaan käyttää tai luoda.

## Yleiset esimerkit
1. **Tietokannan luominen tai avaaminen**:
   ```bash
   sqlite3 mydatabase.db
   ```

2. **Taulun luominen**:
   ```bash
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

3. **Tietojen lisääminen tauluun**:
   ```bash
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Matti');"
   ```

4. **Tietojen kysely**:
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

5. **Taulun poistaminen**:
   ```bash
   sqlite3 mydatabase.db "DROP TABLE users;"
   ```

## Vinkit
- Käytä `-init`-vaihtoehtoa, jos haluat suorittaa useita komentoja yhdellä kertaa tiedostosta.
- Muista aina varmuuskopioida tietokantasi ennen suuria muutoksia.
- Hyödynnä SQL-kyselyjen tehokkuutta oppimalla perus SQL-syntaksia, jotta voit tehdä monimutkaisempia kyselyitä.