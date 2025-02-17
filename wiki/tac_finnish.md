# [Linux] Bash tac käyttö: Tiedoston rivien kääntäminen

## Yleiskatsaus
`tac`-komento on Bashissa käytettävä työkalu, joka kääntää tiedoston rivit ylösalaisin. Se lukee tiedoston rivit alhaalta ylöspäin ja tulostaa ne käänteisessä järjestyksessä. Tämä voi olla hyödyllistä, kun halutaan tarkastella tiedoston viimeisiä rivejä ensin.

## Käyttö
Perussyntaksi `tac`-komennolle on seuraava:

```bash
tac [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-r`, `--regexp`: Käytä säännöllisiä lausekkeita rivien erottamiseen.
- `-s`, `--separator`: Määritä erottelija, jota käytetään rivien välillä (oletuksena on rivinvaihto).
- `-b`, `--before`: Tulosta erottelija ennen riviä.

## Yleiset esimerkit

### Esimerkki 1: Peruskäyttö
Tulosta tiedoston `esimerkki.txt` rivit käänteisessä järjestyksessä.

```bash
tac esimerkki.txt
```

### Esimerkki 2: Erottelijan käyttö
Tulosta tiedoston `esimerkki.txt` rivit käänteisessä järjestyksessä käyttäen erottelijana pilkkua.

```bash
tac -s ',' esimerkki.txt
```

### Esimerkki 3: Säännöllisten lausekkeiden käyttö
Tulosta tiedoston `esimerkki.txt` rivit, jotka sisältävät sanan "testi", käänteisessä järjestyksessä.

```bash
tac -r 'testi' esimerkki.txt
```

## Vinkit
- Käytä `tac`-komentoa yhdessä putkien kanssa, esimerkiksi yhdistämällä se `grep`-komennon kanssa, jotta voit etsiä ja kääntää vain tietyt rivit.
- Muista, että `tac` ei muokkaa alkuperäistä tiedostoa, vaan tulostaa tuloksen terminaaliin. Voit ohjata tulosteen toiseen tiedostoon käyttämällä `>`-merkkiä.
- `tac` on erityisen hyödyllinen lokitiedostojen tarkastelussa, kun haluat nähdä viimeisimmät tapahtumat ensin.