# [Linux] Bash nohup käyttö: Estää prosessin lopettamisen kirjautumisen sulkemisen yhteydessä

## Yleiskatsaus
`nohup` (no hang up) on Bash-komento, joka sallii prosessien jatkamisen, vaikka käyttäjä kirjautuisi ulos tai sulkisi terminaalin. Tämä on erityisen hyödyllistä pitkäkestoisissa prosesseissa, jotka eivät saisi keskeytyä.

## Käyttö
Perussyntaksi `nohup`-komennolle on seuraava:

```bash
nohup [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `&` - Suorittaa komennon taustalla.
- `-h` - Näyttää apua ja ohjeita komennosta.
- `-p` - Määrittää prosessin tunnuksen (PID) käytettäväksi.

## Yleiset esimerkit
1. **Suorita skripti taustalla:**
   ```bash
   nohup ./my_script.sh &
   ```
   Tämä komento suorittaa `my_script.sh`-skriptin taustalla, jolloin se jatkaa toimintaansa, vaikka kirjautuisit ulos.

2. **Tallennus ulostuloon:**
   ```bash
   nohup my_command > output.log &
   ```
   Tässä komennossa `my_command` suoritetaan, ja sen ulostulo tallennetaan `output.log`-tiedostoon.

3. **Käytä yhdessä `&`-merkin kanssa:**
   ```bash
   nohup python my_script.py > output.log 2>&1 &
   ```
   Tämä komento suorittaa Python-skriptin taustalla ja ohjaa sekä standardi- että virheulostulot samaan tiedostoon.

## Vinkit
- Varmista, että käytät `&`-merkkiä, jos haluat prosessin suorittavan taustalla.
- Tarkista `nohup.out`-tiedosto, jos et määritä ulostuloa, sillä kaikki ulostulo tallennetaan oletuksena tähän tiedostoon.
- Käytä `ps`-komentoa tarkistaaksesi, että prosessi on edelleen käynnissä, kun olet kirjautunut ulos.