# [Linux] Bash vigr käyttö: Muokkaa järjestelmän viemäriä

## Yleiskatsaus
`vigr` on komento, jota käytetään järjestelmän viemärin (passwd, group, shadow) muokkaamiseen turvallisesti. Se avaa viemärin tekstieditorissa, jolloin käyttäjät voivat tehdä muutoksia käyttäjä- ja ryhmätiliin liittyviin tietoihin.

## Käyttö
Perussyntaksi komennolle on seuraava:
```
vigr [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-s`: Käynnistää `vigr` turvallisessa tilassa, jolloin muutokset tallennetaan vain, jos tiedosto on muuttunut.
- `-f`: Määrittää tiedoston, jota haluat muokata, esimerkiksi `vigr -f /etc/passwd`.
- `-h`: Näyttää apua ja käytön ohjeet.

## Yleiset esimerkit
1. **Viemärin muokkaaminen**:
   ```bash
   vigr
   ```
   Tämä avaa oletustiedoston, joka on yleensä `/etc/passwd`.

2. **Erityisen tiedoston muokkaaminen**:
   ```bash
   vigr -f /etc/group
   ```
   Tämä avaa ryhmätiedoston muokattavaksi.

3. **Turvallinen muokkaus**:
   ```bash
   vigr -s
   ```
   Tämä avaa viemärin turvallisessa tilassa, varmistaen, että tiedostoa ei tallenneta, jos se ei ole muuttunut.

## Vinkit
- Käytä `-s`-vaihtoehtoa aina, kun muokkaat järjestelmän viemäreitä, jotta vältät vahingossa tapahtuvat muutokset.
- Varmista, että sinulla on tarvittavat oikeudet muokata viemäreitä, sillä ne vaativat usein pääkäyttäjän oikeudet.
- Tee varmuuskopio alkuperäisestä tiedostosta ennen muokkauksia, jotta voit palauttaa sen tarvittaessa.