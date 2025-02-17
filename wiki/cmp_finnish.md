# [Linux] Bash cmp käyttö: Vertaa kahta tiedostoa

## Yleiskatsaus
`cmp`-komento on työkalu, jota käytetään kahden tiedoston vertailuun. Se tarkistaa tiedostojen sisällön ja ilmoittaa, ovatko ne samat vai eri. Jos tiedostot eroavat, `cmp` näyttää ensimmäisen eron sijainnin.

## Käyttö
Perussyntaksi `cmp`-komennolle on seuraava:
```
cmp [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Näyttää kaikki erot tavuittain.
- `-s`: Ei tulosta mitään, mutta palauttaa arvon 0, jos tiedostot ovat samat, ja 1, jos ne eroavat.
- `-i OFFSET`: Aloittaa vertailun tietyistä tavuista.
- `-n N`: Vertaa vain ensimmäisiä N tavua.

## Yleiset esimerkit
1. **Perusvertailu**:
   Vertaa kahta tiedostoa ja näyttää ensimmäisen eron.
   ```bash
   cmp tiedosto1.txt tiedosto2.txt
   ```

2. **Erojen näyttäminen tavuittain**:
   Näyttää kaikki erot tavuittain.
   ```bash
   cmp -l tiedosto1.txt tiedosto2.txt
   ```

3. **Vertailu ilman tulostusta**:
   Tarkistaa, ovatko tiedostot samat, mutta ei tulosta mitään.
   ```bash
   cmp -s tiedosto1.txt tiedosto2.txt
   ```

4. **Vertailu tietyistä tavuista**:
   Vertaa tiedostoja alkaen tietyistä tavuista.
   ```bash
   cmp -i 10 tiedosto1.txt tiedosto2.txt
   ```

5. **Rajoitettu vertailu**:
   Vertaa vain ensimmäisiä 100 tavua.
   ```bash
   cmp -n 100 tiedosto1.txt tiedosto2.txt
   ```

## Vinkit
- Käytä `-s`-vaihtoehtoa, kun haluat tarkistaa tiedostojen samankaltaisuuden ilman ylimääräistä tulostusta.
- `cmp` on erityisen hyödyllinen suurten tiedostojen vertailussa, koska se voi nopeasti löytää ensimmäiset erot.
- Muista, että `cmp` vertaa tiedostoja tavuittain, joten se on herkkä pienillekin muutoksille tiedostojen sisällössä.