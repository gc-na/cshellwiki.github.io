# [Linux] Bash fold käyttö: Tekstirivien katkaiseminen

## Yleiskatsaus
`fold`-komento on työkalu, jota käytetään tekstirivien katkaisemiseen tiettyyn leveyteen. Se on erityisen hyödyllinen, kun halutaan varmistaa, että teksti mahtuu tiettyyn tilaan, kuten tulostukseen tai näyttöön.

## Käyttö
Perussyntaksi `fold`-komennolle on seuraava:

```bash
fold [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-w, --width=N`: Määrittää rivin maksimi leveyden merkkeinä (oletus on 80 merkkiä).
- `-s, --break-at-space`: Katkaisee rivin vain sanan kohdalla, ei keskellä sanaa.
- `-b, --bytes`: Katkaisee rivit tietyllä tavumäärällä sen sijaan, että käyttäisi merkkejä.

## Yleiset esimerkit
1. **Peruskäyttö**: Katkaise tiedoston rivit 50 merkkiin.
   ```bash
   fold -w 50 tiedosto.txt
   ```

2. **Sanakatkaisu**: Katkaise rivit sanan kohdalla.
   ```bash
   fold -s -w 50 tiedosto.txt
   ```

3. **Tavupohjainen katkaisu**: Katkaise rivit 30 tavun mukaan.
   ```bash
   fold -b -w 30 tiedosto.txt
   ```

4. **Useita tiedostoja**: Katkaise useita tiedostoja kerralla.
   ```bash
   fold -w 60 tiedosto1.txt tiedosto2.txt
   ```

## Vinkit
- Käytä `-s`-vaihtoehtoa, jos haluat säilyttää sanojen eheyden, erityisesti pitkissä teksteissä.
- Testaa eri leveyksiä ennen kuin päätät lopullisen arvon, jotta saat parhaan mahdollisen ulkoasun.
- Voit yhdistää `fold`-komennon muihin komentoihin, kuten `cat`, putkittamalla tuloksen toiseen komentoihin. Esimerkiksi:
   ```bash
   cat tiedosto.txt | fold -w 70
   ```