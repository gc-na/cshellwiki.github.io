# [Linux] Bash last käyttö: Näyttää käyttäjien kirjautumistiedot

## Overview
`last`-komento näyttää käyttäjien kirjautumistiedot ja järjestelmän käynnistykset. Se lukee tietoja `/var/log/wtmp`-tiedostosta, joka tallentaa kaikki kirjautumiset ja kirjautumiset ulos.

## Usage
Perussyntaksi `last`-komennolle on seuraava:

```bash
last [options] [arguments]
```

## Common Options
- `-a`: Näyttää viimeisen kirjautumisen isäntänimen.
- `-n [number]`: Määrittää näytettävien kirjautumisten määrän.
- `-R`: Poistaa isäntänimen näytöstä.
- `-x`: Näyttää myös järjestelmän käynnistykset ja sammutukset.

## Common Examples
### Esimerkki 1: Näytä kaikki kirjautumiset
```bash
last
```

### Esimerkki 2: Näytä viimeiset 5 kirjautumista
```bash
last -n 5
```

### Esimerkki 3: Näytä kirjautumiset isäntänimellä
```bash
last -a
```

### Esimerkki 4: Näytä myös järjestelmän käynnistykset
```bash
last -x
```

## Tips
- Käytä `last -n [number]` rajoittaaksesi tuloksia, jos haluat vain viimeisimmät kirjautumiset.
- Voit yhdistää `last`-komennon putkistoon muiden komentojen kanssa, kuten `grep`, suodattaaksesi tietoja.
- Muista, että `last` näyttää vain kirjautumiset, jotka on tallennettu wtmp-tiedostoon, joten vanhemmat tiedot voivat olla kadonneet, jos tiedosto on kierrätetty.