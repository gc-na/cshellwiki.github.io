# [Linux] Bash nl käyttö: Rivinumerointi tiedostoissa

## Yleiskatsaus
`nl`-komento on Linuxissa käytettävä työkalu, joka lisää rivinumeroita tekstitiedostoihin. Se on erityisen hyödyllinen, kun halutaan viitata tiettyihin riveihin tai parantaa tiedoston luettavuutta.

## Käyttö
Perussyntaksi `nl`-komennolle on seuraava:

```bash
nl [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-b` : Määrittelee, miten tyhjät rivit käsitellään (esim. `-b a` lisää numerot kaikkiin riveihin).
- `-f` : Määrittelee, kuinka usein numerointi alkaa uudelleen (esim. `-f 2` aloittaa numeroinnin jokaiselta toiselta sivulta).
- `-n` : Määrittelee numeroinnin muodon (esim. `-n ln` käyttää vasenta numeroa).
- `-w` : Määrittelee rivinumeron leveyden (esim. `-w 5` varaa viisi merkkiä numerolle).

## Yleiset esimerkit
1. **Rivinumeroiden lisääminen tiedostoon:**
   ```bash
   nl tiedosto.txt
   ```
   Tämä komento lisää rivinumerot tiedoston `tiedosto.txt` jokaiselle riville.

2. **Tyhjien rivien numerointi:**
   ```bash
   nl -b a tiedosto.txt
   ```
   Tässä komennossa kaikki rivit, mukaan lukien tyhjät, saavat numerot.

3. **Numeroinnin aloittaminen uudelleen jokaiselta toiselta sivulta:**
   ```bash
   nl -f 2 tiedosto.txt
   ```
   Tämä komento aloittaa numeroinnin uudelleen jokaiselta toiselta sivulta.

4. **Rivinumeron leveyden määrittäminen:**
   ```bash
   nl -w 5 tiedosto.txt
   ```
   Tässä komennossa rivinumerot varataan viisi merkkiä, jolloin numerot ovat tasapainoisempia.

## Vinkit
- Käytä `man nl` saadaksesi lisätietoja ja vaihtoehtoja komennosta.
- Yhdistä `nl` muihin komentoihin, kuten `cat`, saadaksesi rivinumerot yhdistettynä tiedostojen sisällön näyttämiseen.
- Kokeile eri vaihtoehtoja, kuten `-n`, saadaksesi juuri haluamasi numeroinnin muodon.