# [Linux] Bash top käyttö: Näyttää järjestelmän prosessit ja niiden resurssinkäytön

## Yleiskatsaus
`top`-komento on tehokas työkalu, joka näyttää reaaliaikaisesti järjestelmän prosessit ja niiden resurssinkäytön. Se tarjoaa käyttäjälle mahdollisuuden seurata prosessien toimintaa, CPU:n ja muistin käyttöä sekä muita tärkeitä järjestelmätietoja.

## Käyttö
Perussyntaksi `top`-komennolle on seuraava:
```
top [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d [aika]`: Määrittää päivitysvälin sekunneissa.
- `-n [kerrat]`: Määrittää, kuinka monta kertaa `top`-näyttö päivitetään ennen sulkemista.
- `-u [käyttäjä]`: Näyttää vain tietyn käyttäjän prosessit.
- `-p [PID]`: Näyttää vain tietyn prosessin, jonka prosessitunnus (PID) on annettu.

## Yleiset esimerkit
1. **Perus `top`-komento**:
   ```
   top
   ```
   Tämä avaa `top`-käyttöliittymän, jossa näkyvät kaikki prosessit.

2. **Määritä päivitysväli**:
   ```
   top -d 5
   ```
   Tämä päivittää `top`-näyttöä viiden sekunnin välein.

3. **Näytä vain tietyn käyttäjän prosessit**:
   ```
   top -u käyttäjänimi
   ```
   Tämä näyttää vain valitun käyttäjän prosessit.

4. **Näytä vain tietty prosessi**:
   ```
   top -p 1234
   ```
   Tämä näyttää vain prosessin, jonka PID on 1234.

5. **Rajoita päivityksiä**:
   ```
   top -n 10
   ```
   Tämä päivittää näyttöä kymmenen kertaa ja sulkee sitten automaattisesti.

## Vinkit
- Voit käyttää näppäimistön komentoja `top`-tilassa, kuten `k` prosessin tappamiseen tai `r` prioriteetin muuttamiseen.
- Muista, että `top`-komento voi kuluttaa järjestelmän resursseja, joten käytä sitä harkiten erityisesti kuormitetuissa järjestelmissä.
- Voit tallentaa `top`-asetukset ja mukautetut näkymät, mikä helpottaa toistuvaa käyttöä.