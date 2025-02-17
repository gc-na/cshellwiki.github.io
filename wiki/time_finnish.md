# [Linux] Bash time käyttö: Suoritusajan mittaaminen

## Yleiskatsaus
`time`-komento on työkalu, jota käytetään ohjelmien suoritusajan mittaamiseen. Se näyttää, kuinka kauan ohjelman suorittaminen kestää, sekä muita hyödyllisiä tietoja, kuten käytetyn prosessorin ajan ja järjestelmän ajan.

## Käyttö
Perus syntaksi `time`-komennolle on seuraava:

```bash
time [options] [arguments]
```

## Yleiset vaihtoehdot
- `-p`: Tulostaa tulokset POSIX-yhteensopivassa muodossa.
- `-o <tiedosto>`: Tallentaa tulosteen määriteltyyn tiedostoon.
- `-v`: Näyttää yksityiskohtaisemman raportin ohjelman suorittamisesta.

## Yleiset esimerkit
1. Suorita komento ja mittaa sen kesto:
   ```bash
   time ls -l
   ```

2. Tallenna tulokset tiedostoon:
   ```bash
   time -o tulokset.txt sleep 2
   ```

3. Käytä yksityiskohtaisempaa raportointia:
   ```bash
   time -v find / -name "example.txt"
   ```

4. Mittaa useita komentoja peräkkäin:
   ```bash
   { time tar -czf archive.tar.gz /path/to/directory; } 2> time_output.txt
   ```

## Vinkit
- Käytä `-p`-vaihtoehtoa, jos tarvitset tulokset skriptin käsittelyä varten.
- Muista, että `time`-komento ei ole sama kuin `time`-komento, joka on osa shelliä; se on erillinen komento.
- Voit yhdistää `time`-komennon muihin komentoihin, kuten `&&` tai `;`, suorittaaksesi useita komentoja peräkkäin ja mitata niiden kestoa.