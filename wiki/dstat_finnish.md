# [Linux] Bash dstat käyttö: Järjestelmän suorituskyvyn valvonta

## Yleiskatsaus
`dstat` on tehokas työkalu, joka yhdistää useita järjestelmän suorituskyvyn valvontatyökaluja. Se tarjoaa reaaliaikaista tietoa järjestelmän resursseista, kuten CPU:sta, muistista, levyistä ja verkosta, ja auttaa käyttäjiä analysoimaan järjestelmän toimintaa.

## Käyttö
Perussyntaksi `dstat`-komennolle on seuraava:

```bash
dstat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Näyttää CPU-käytön.
- `-d`: Näyttää levyn käytön.
- `-n`: Näyttää verkon käytön.
- `-m`: Näyttää muistin käytön.
- `--help`: Näyttää apu- ja käyttöohjeet.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `dstat`-komennon käytöstä:

1. **Perustietojen näyttäminen:**
   ```bash
   dstat
   ```

2. **CPU- ja muistitietojen näyttäminen:**
   ```bash
   dstat -c -m
   ```

3. **Levy- ja verkkotietojen näyttäminen:**
   ```bash
   dstat -d -n
   ```

4. **Tietojen tallentaminen tiedostoon:**
   ```bash
   dstat > dstat_output.txt
   ```

5. **Tietojen näyttäminen tietyllä aikavälillä:**
   ```bash
   dstat -t 5
   ```

## Vinkit
- Käytä `dstat`-komentoa yhdessä muiden työkalujen, kuten `grep`in tai `awk`in, kanssa suodattaaksesi ja analysoidaksesi tietoja tarkemmin.
- Voit yhdistää useita vaihtoehtoja samaan komentoihin saadaksesi kattavampaa tietoa järjestelmästä.
- Hyödynnä `--help`-vaihtoehtoa, jos tarvitset lisätietoja käytettävissä olevista vaihtoehdoista ja argumenteista.