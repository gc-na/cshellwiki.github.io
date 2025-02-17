# [Linux] Bash @ käyttö: Komentojen suorittaminen taustalla

## Overview
`@`-komento Bashissa mahdollistaa komentojen suorittamisen taustalla, jolloin voit jatkaa työskentelyä terminaalissa ilman, että odotat komentojen valmistumista.

## Usage
Perussyntaksi `@`-komennolle on seuraava:

```
@ [options] [arguments]
```

## Common Options
- `&`: Suorittaa komennon taustalla.
- `disown`: Poistaa taustalla olevan prosessin hallinnan terminaalista.
- `nohup`: Estää prosessin lopettamisen, kun käyttäjä kirjautuu ulos.

## Common Examples
1. Suorita komento taustalla:
   ```bash
   long_running_command &
   ```

2. Käytä `nohup`-komentoa, jotta prosessi jatkuu kirjautumisen jälkeen:
   ```bash
   nohup long_running_command &
   ```

3. Poista taustaprosessi hallinnasta:
   ```bash
   disown %1
   ```

## Tips
- Käytä `jobs`-komentoa tarkistaaksesi taustaprosessit.
- Varmista, että käytät `nohup`-komentoa, jos haluat prosessin jatkavan toimintaansa kirjautuessasi ulos.
- Muista, että taustalla suoritetut komennot eivät näytä tulostetta suoraan terminaalissa, joten voit ohjata tulosteen tiedostoon, jos tarvitset sen myöhemmin.