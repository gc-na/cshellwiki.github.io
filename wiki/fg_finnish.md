# [Linux] Bash fg käyttö: Siirtää taustaprosessin eteen

## Yleiskatsaus
`fg`-komento Bashissa siirtää taustalla olevan prosessin (background job) eteenpäin, jolloin se saa käyttöliittymän ja voi vastaanottaa syötteitä. Tämä on hyödyllistä, kun haluat palata aiemmin keskeytettyyn tai taustalle siirrettyyn prosessiin.

## Käyttö
Perussyntaksi `fg`-komennolle on seuraava:

```bash
fg [options] [arguments]
```

## Yleiset vaihtoehdot
- `%n`: Siirtää prosessin, jonka tunnus on `n`. Esimerkiksi `%1` siirtää ensimmäisen taustaprosessin.
- `-`: Siirtää viimeksi taustalle siirretyn prosessin.

## Yleiset esimerkit

1. **Siirrä ensimmäinen taustaprosessi eteen:**
   ```bash
   fg %1
   ```

2. **Siirrä viimeksi taustalle siirretty prosessi eteen:**
   ```bash
   fg -
   ```

3. **Jos käytät useita prosesseja, voit tarkistaa niiden tilan komennolla `jobs`:**
   ```bash
   jobs
   ```
   Tämän jälkeen voit siirtää haluamasi prosessin eteen käyttämällä `fg`-komentoa.

## Vinkit
- Varmista, että tiedät, mikä prosessi on taustalla ennen `fg`-komennon käyttöä. Voit tarkistaa sen `jobs`-komennolla.
- Jos haluat keskeyttää prosessin, voit käyttää `Ctrl + Z`, jolloin se siirtyy taustalle ja voit myöhemmin siirtää sen eteen `fg`-komennolla.
- Muista, että `fg`-komento toimii vain taustaprosessien kanssa, joten varmista, että prosessi on taustalla ennen sen siirtämistä eteen.