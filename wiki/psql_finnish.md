# [Linux] Bash psql käyttö: Suora pääsy PostgreSQL-tietokantaan

## Yleiskatsaus
`psql` on PostgreSQL-tietokannan komentoriviliittymä, joka mahdollistaa käyttäjille suoran pääsyn tietokantoihin. Sen avulla voit suorittaa SQL-kyselyitä, hallita tietokantoja ja tarkastella tietoja helposti komentoriviltä.

## Käyttö
Perussyntaksi `psql`-komennolle on seuraava:

```bash
psql [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h` : Määrittää palvelimen isäntänimen tai IP-osoitteen.
- `-U` : Määrittää käyttäjänimen, jolla kirjaudutaan sisään.
- `-d` : Määrittää käytettävän tietokannan nimen.
- `-p` : Määrittää portin, jota käytetään yhteyden muodostamiseen.
- `-f` : Suorittaa SQL-tiedoston komennot.

## Yleiset esimerkit
1. Yhteyden muodostaminen tietokantaan:
   ```bash
   psql -h localhost -U käyttäjänimi -d tietokanta
   ```

2. SQL-kyselyn suorittaminen:
   ```bash
   psql -d tietokanta -c "SELECT * FROM taulu;"
   ```

3. SQL-tiedoston suorittaminen:
   ```bash
   psql -d tietokanta -f tiedosto.sql
   ```

4. Tietokannan luominen:
   ```bash
   psql -U käyttäjänimi -c "CREATE DATABASE uusi_tietokanta;"
   ```

## Vinkit
- Käytä `\?` komennolla `psql`-tilassa saadaksesi lisätietoja käytettävissä olevista komennoista ja vaihtoehdoista.
- Varmista, että sinulla on oikeudet tietokannan hallintaan ennen kuin yrität suorittaa hallintokäskyjä.
- Hyödynnä `\d`-komentoa nähdäksesi tietokannan taulut ja niiden rakenteet.