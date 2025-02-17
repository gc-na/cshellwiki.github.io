# [Linux] Bash source käyttö: Suorita komentosarjat nykyisessä ympäristössä

## Overview
`source`-komento Bashissa mahdollistaa komentosarjan suorittamisen nykyisessä kuoriprosessissa. Tämä tarkoittaa, että kaikki komentosarjassa määritetyt ympäristömuuttujat ja toiminnot ovat käytettävissä heti sen suorittamisen jälkeen, ilman että erillistä prosessia käynnistetään.

## Usage
Perussyntaksi `source`-komennolle on seuraava:

```bash
source [options] [arguments]
```

Voit myös käyttää lyhennettä `.` (piste) komennon sijasta:

```bash
. [options] [arguments]
```

## Common Options
- `-e`: Lopettaa virheiden vuoksi, jos komentosarjassa esiintyy virhe.
- `-u`: Aktivoi muuttujat, jotka on määritelty vain, jos ne ovat olemassa.

## Common Examples

### Esimerkki 1: Komentosarjan suorittaminen
Suorita komentosarja nimeltä `script.sh` nykyisessä ympäristössä:

```bash
source script.sh
```

### Esimerkki 2: Ympäristömuuttujien asettaminen
Jos `script.sh` sisältää ympäristömuuttujan määrittelyn, voit käyttää sitä seuraavasti:

```bash
source script.sh
echo $MY_VARIABLE
```

### Esimerkki 3: Komentosarjan suorittaminen lyhenteellä
Voit käyttää myös pistettä `.` komennon sijasta:

```bash
. script.sh
```

## Tips
- Käytä `source`-komentoa, kun haluat, että komentosarjasi vaikuttaa nykyiseen ympäristöösi, kuten muuttujien asettamiseen.
- Varmista, että komentosarjasi on suoritettavissa ja että se ei sisällä virheitä, jotta vältät ongelmat ympäristössäsi.
- Hyödynnä `set -e` komennon käyttöä komentosarjassasi, jotta se lopettaa suorituksen virhetilanteissa.