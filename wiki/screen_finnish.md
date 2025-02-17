# [Linux] Bash screen käyttö: Moniajo terminaalissa

## Overview
`screen` on tehokas työkalu, joka mahdollistaa useiden terminaalisiistien hallinnan yhdestä ikkunasta. Se on erityisen hyödyllinen etäyhteyksissä, koska se mahdollistaa istuntojen jatkamisen ja katkaisemisen ilman, että käynnissä olevat prosessit pysähtyvät.

## Usage
Perussyntaksi `screen`-komennolle on seuraava:

```bash
screen [options] [arguments]
```

## Common Options
- `-S <nimi>`: Määrittää istunnon nimen, mikä helpottaa sen löytämistä myöhemmin.
- `-d -r`: Katkaisee ja palauttaa etäistunnon.
- `-list`: Näyttää kaikki käynnissä olevat `screen`-istunnot.
- `-L`: Aktivoi lokitiedostojen tallentamisen, jolloin voit tarkastella istunnon tulosteita myöhemmin.

## Common Examples
1. **Uuden `screen`-istunnon luominen:**
   ```bash
   screen
   ```

2. **Istunnon nimeäminen:**
   ```bash
   screen -S oma_istunto
   ```

3. **Istunnon katkaiseminen:**
   - Paina `Ctrl + A`, sitten `D`.

4. **Etäistunnon palauttaminen:**
   ```bash
   screen -r oma_istunto
   ```

5. **Kaikkien istuntojen listaaminen:**
   ```bash
   screen -list
   ```

6. **Istunnon lokittaminen:**
   ```bash
   screen -L
   ```

## Tips
- Käytä istunnon nimeämistä, jotta löydät sen helpommin myöhemmin.
- Muista katkaista istunto, jos et aio käyttää sitä pitkään aikaan, jotta resurssit eivät jää turhaan käyttöön.
- Hyödynnä lokitiedostoja, jotta voit tarkastella aiempia komentoja ja tulosteita.