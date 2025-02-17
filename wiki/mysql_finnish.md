# [Linux] Bash mysql käyttö: Tietokannan hallinta ja kyselyt

## Yleiskatsaus
`mysql` on komentorivipohjainen työkalu, jota käytetään MySQL-tietokannan hallintaan. Sen avulla voit suorittaa SQL-kyselyitä, hallita tietokantoja ja käyttäjiä sekä tehdä muita tietokantatoimintoja suoraan komentoriviltä.

## Käyttö
Perussyntaksi `mysql`-komennolle on seuraava:

```bash
mysql [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-u [käyttäjä]`: Määrittää käyttäjänimen, jolla kirjaudutaan MySQL-tietokantaan.
- `-p`: Kehottaa syöttämään salasanan.
- `-h [isäntä]`: Määrittää MySQL-palvelimen isäntänimen tai IP-osoitteen.
- `-D [tietokanta]`: Määrittää käytettävän tietokannan.
- `--execute="[kysely]"`: Suorittaa annetun SQL-kyselyn suoraan komentoriviltä.

## Yleiset esimerkit

1. **Kirjautuminen MySQL:ään käyttäjänä "root":**

   ```bash
   mysql -u root -p
   ```

2. **Tietokannan luominen:**

   ```bash
   mysql -u root -p -e "CREATE DATABASE esimerkki_tietokanta;"
   ```

3. **Tietokannan valitseminen ja taulun luominen:**

   ```bash
   mysql -u root -p -D esimerkki_tietokanta -e "CREATE TABLE asiakkaita (id INT AUTO_INCREMENT PRIMARY KEY, nimi VARCHAR(100));"
   ```

4. **Tietojen lisääminen tauluun:**

   ```bash
   mysql -u root -p -D esimerkki_tietokanta -e "INSERT INTO asiakkaita (nimi) VALUES ('Matti Meikäläinen');"
   ```

5. **Tietojen hakeminen taulusta:**

   ```bash
   mysql -u root -p -D esimerkki_tietokanta -e "SELECT * FROM asiakkaita;"
   ```

## Vinkit
- Käytä `--execute`-vaihtoehtoa, jos haluat suorittaa SQL-kyselyitä suoraan komentoriviltä ilman interaktiivista istuntoa.
- Muista käyttää `-D`-vaihtoehtoa, kun haluat työskennellä tietyn tietokannan parissa.
- Hyödynnä `mysql`-komennon mahdollisuuksia skriptauksessa, jotta voit automatisoida tietokantatoimintoja.