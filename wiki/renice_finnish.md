# [Linux] Bash renice käyttö: Muuttaa prosessien prioriteettia

## Yleiskatsaus
`renice`-komento Bashissa käytetään prosessien prioriteettien muuttamiseen. Se mahdollistaa käyttäjien säätää prosessien aikarajoja, mikä voi parantaa järjestelmän suorituskykyä ja reaktiokykyä.

## Käyttö
Perussyntaksi `renice`-komennolle on seuraava:

```bash
renice [options] [arguments]
```

## Yleiset vaihtoehdot
- `-n, --priority <arvo>`: Asettaa uuden prioriteettiarvon prosessille. Arvo voi olla negatiivinen (korkea prioriteetti) tai positiivinen (matala prioriteetti).
- `-p, --pid <prosessi_id>`: Määrittää prosessin tunnuksen, jonka prioriteettia halutaan muuttaa.
- `-g, --pgroup <ryhmä_id>`: Muuttaa prioriteettia kaikille prosessille, jotka kuuluvat tiettyyn prosessiryhmään.
- `-u, --user <käyttäjä>`: Muuttaa prioriteettia kaikille prosesseille, jotka kuuluvat tietylle käyttäjälle.

## Yleiset esimerkit
1. Muuta prosessin prioriteettiä tunnuksella 1234 arvoon 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Muuta kaikkien käyttäjän "user1" prosessien prioriteettiä arvoon -5:
   ```bash
   renice -n -5 -u user1
   ```

3. Muuta prosessiryhmän prioriteettiä, jonka ryhmä ID on 5678 arvoon 15:
   ```bash
   renice -n 15 -g 5678
   ```

## Vinkit
- Käytä `renice`-komentoa varoen, sillä liian korkea prioriteetti voi vaikuttaa negatiivisesti järjestelmän muihin prosesseihin.
- Tarkista prosessien nykyiset prioriteetit ennen muutoksia komennolla `ps -o pid,ni,cmd`.
- Muista, että vain prosessin omistaja tai järjestelmänvalvoja voi muuttaa prosessien prioriteetteja.