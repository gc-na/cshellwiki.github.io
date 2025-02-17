# [Linux] Bash id käyttö: käyttäjän tunnistaminen

## Overview
`id`-komento näyttää käyttäjän ja ryhmien tunnistetiedot. Se tarjoaa tietoa käyttäjän UID:stä (User ID), GID:stä (Group ID) ja käyttäjän jäsenyyksistä eri ryhmissä.

## Usage
Perussyntaksi `id`-komennolle on seuraava:

```bash
id [options] [arguments]
```

## Common Options
- `-u`: Näyttää vain käyttäjän UID:n.
- `-g`: Näyttää vain käyttäjän GID:n.
- `-G`: Näyttää kaikki ryhmien GID:t, joihin käyttäjä kuuluu.
- `-n`: Näyttää nimet (esim. käyttäjänimi tai ryhmän nimi) sen sijaan, että näyttäisi numerot.

## Common Examples
1. **Perustiedot käyttäjästä:**
   ```bash
   id
   ```

2. **Näytä vain käyttäjän UID:**
   ```bash
   id -u
   ```

3. **Näytä vain käyttäjän GID:**
   ```bash
   id -g
   ```

4. **Näytä kaikki ryhmät, joihin käyttäjä kuuluu:**
   ```bash
   id -G
   ```

5. **Näytä käyttäjänimi ja UID:**
   ```bash
   id -un
   ```

## Tips
- Käytä `id`-komentoa ongelmien vianetsintään, kun haluat varmistaa, että käyttäjä on oikeassa ryhmässä.
- Voit yhdistää `id`-komennon muihin komentoihin, kuten `grep`, suodataksesi tietoa tarkemmin.
- Muista, että `id`-komento toimii myös muiden käyttäjien tietojen tarkasteluun, jos sinulla on tarvittavat oikeudet, esimerkiksi `id username`.