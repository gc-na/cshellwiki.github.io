# [Linux] Bash pr käyttö: Tiedostojen tulostaminen sivuittain

## Yleiskatsaus
`pr`-komento on työkalu, jota käytetään tiedostojen muotoiluun ja tulostamiseen sivuittain. Se jakaa tiedoston sisällön useisiin sarakkeisiin, mikä helpottaa lukemista ja tulostamista erityisesti suurille tekstidokumenteille.

## Käyttö
Perussyntaksi `pr`-komennolle on seuraava:

```bash
pr [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h, --header`: Määrittää otsikon, joka tulostetaan jokaisen sivun yläosaan.
- `-n`: Poistaa numeroinnin tulosteesta.
- `-s`: Määrittää, kuinka monta tyhjää riviä tulostetaan sarakkeiden väliin.
- `-t`: Poistaa tyhjät rivit tulosteesta.
- `-w, --width`: Määrittää tulosteen leveyden tietyksi arvoksi.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `pr`-komennon käytöstä:

1. **Perustulostus**:
   Tulostaa tiedoston sivuittain oletusasetuksilla.
   ```bash
   pr tiedosto.txt
   ```

2. **Otsikon lisääminen**:
   Lisää otsikon tulosteeseen.
   ```bash
   pr -h "Otsikko" tiedosto.txt
   ```

3. **Sarakkeiden määrän määrittäminen**:
   Tulostaa tiedoston kahdessa sarakkeessa.
   ```bash
   pr -2 tiedosto.txt
   ```

4. **Tulosteen leveyden määrittäminen**:
   Määrittää tulosteen leveydeksi 80 merkkiä.
   ```bash
   pr -w 80 tiedosto.txt
   ```

5. **Tyhjien rivien poistaminen**:
   Poistaa tyhjät rivit tulosteesta.
   ```bash
   pr -t tiedosto.txt
   ```

## Vinkit
- Käytä `man pr` saadaksesi lisätietoja ja täydellisen vaihtoehtoluettelon.
- Kokeile eri vaihtoehtoja ja yhdistelmiä, jotta löydät parhaan tavan esittää tietosi.
- Muista, että `pr`-komento on erityisen hyödyllinen suurille tiedostoille, joten käytä sitä, kun työskentelet laajojen tekstidokumenttien kanssa.