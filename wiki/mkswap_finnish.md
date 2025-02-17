# [Linux] Bash mkswap käyttö: Vaihtotilan luominen

## Yleiskatsaus
`mkswap`-komento luo vaihtotilan (swap space) tiedostolle tai osiolle, jota käytetään muistin laajentamiseen. Tämä on erityisen hyödyllistä, kun fyysinen muisti (RAM) on loppumassa, ja se mahdollistaa järjestelmän vakauden parantamisen.

## Käyttö
Perussyntaksi `mkswap`-komennolle on seuraava:

```bash
mkswap [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-f`, `--force`: Pakottaa vaihtotilan luomisen, vaikka tiedosto tai osio ei olisi tyhjennetty.
- `-L`, `--label`: Määrittää vaihtotilan nimen (label).
- `-p`, `--pagesize`: Määrittää sivukoon, jota käytetään vaihtotilassa.

## Yleiset esimerkit
1. **Perusvaihtotilan luominen tiedostolle**:
   ```bash
   sudo fallocate -l 1G /swapfile
   sudo mkswap /swapfile
   ```

2. **Vaihtotilan luominen tiedostolle ja sen nimeäminen**:
   ```bash
   sudo mkswap -L my_swap /swapfile
   ```

3. **Pakotettu vaihtotilan luominen**:
   ```bash
   sudo mkswap -f /dev/sdX1
   ```

## Vinkit
- Varmista, että tiedosto tai osio, jolle luot vaihtotilan, on tyhjennetty ennen `mkswap`-komennon suorittamista.
- Käytä `swapon`-komentoa aktivoidaksesi luomasi vaihtotila.
- Tarkista järjestelmän muistinkäyttö ja vaihtotilan tila komennolla `free -h`.