# [Linux] Bash pwd käyttö: Näyttää nykyisen työskentelyhakemiston

## Yleiskatsaus
`pwd` (print working directory) -komento näyttää nykyisen työskentelyhakemiston absoluuttisen polun. Tämä komento on hyödyllinen, kun haluat tietää, missä hakemistossa olet työskentelemässä komentorivillä.

## Käyttö
Perussyntaksi `pwd`-komennolle on seuraava:

```bash
pwd [options] [arguments]
```

## Yleiset vaihtoehdot
- `-L`: Näyttää symbolisen linkin mukaisen polun.
- `-P`: Näyttää fyysisen polun, joka ei sisällä symbolisia linkkejä.

## Yleiset esimerkit
1. **Peruskomento**: Näyttää nykyisen hakemiston.
   ```bash
   pwd
   ```

2. **Symbolisen linkin polku**: Näyttää nykyisen hakemiston symbolisen linkin mukaisen polun.
   ```bash
   pwd -L
   ```

3. **Fyysinen polku**: Näyttää nykyisen hakemiston fyysisen polun.
   ```bash
   pwd -P
   ```

## Vinkit
- Käytä `pwd`-komentoa ennen ja jälkeen hakemistojen vaihtamisen, jotta tiedät, missä olet.
- Voit yhdistää `pwd`-komennon muihin komentoihin, kuten `cd`, saadaksesi selkeämmän käsityksen hakemistopolusta.
- Muista, että `pwd`-komento on erittäin hyödyllinen skriptien kirjoittamisessa, kun haluat varmistaa, että työskentelet oikeassa hakemistossa.