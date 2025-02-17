# [Linux] Bash who käyttö: Näyttää kirjautuneet käyttäjät

## Overview
`who`-komento näyttää tietoja kaikista tällä hetkellä kirjautuneista käyttäjistä järjestelmässä. Se tarjoaa tietoa käyttäjien nimistä, kirjautumisaikasta ja muista tärkeistä tiedoista, kuten käytettävästä terminaalista.

## Usage
Perussyntaksi `who`-komennolle on seuraava:

```bash
who [options] [arguments]
```

## Common Options
- `-a`: Näyttää kaikki tiedot, mukaan lukien kirjautumattomat käyttäjät ja muut tiedot.
- `-b`: Näyttää viimeisen järjestelmän käynnistyksen ajan.
- `-q`: Näyttää vain käyttäjien nimet ja niiden lukumäärän.
- `--help`: Näyttää apuviestin, joka sisältää tietoa komennosta ja sen käytöstä.

## Common Examples
Tässä on muutamia käytännön esimerkkejä `who`-komennon käytöstä:

1. **Peruskomento**: Näyttää kaikki kirjautuneet käyttäjät.
   ```bash
   who
   ```

2. **Kaikkien tietojen näyttäminen**: Näyttää kaikki tiedot kirjautuneista käyttäjistä.
   ```bash
   who -a
   ```

3. **Viimeisen käynnistyksen ajan näyttäminen**: Näyttää, milloin järjestelmä viimeksi käynnistettiin.
   ```bash
   who -b
   ```

4. **Käyttäjien lukumäärän näyttäminen**: Näyttää vain kirjautuneiden käyttäjien nimet ja niiden lukumäärän.
   ```bash
   who -q
   ```

## Tips
- Käytä `who`-komentoa yhdessä muiden komentojen, kuten `grep`, kanssa suodataksesi tietoja tiettyjen käyttäjien perusteella.
- Muista, että `who` näyttää vain aktiiviset kirjautumiset; se ei näytä käyttäjiä, jotka ovat kirjautuneet ulos.
- Voit käyttää `man who` saadaksesi lisätietoja ja nähdäksesi kaikki käytettävissä olevat vaihtoehdot.