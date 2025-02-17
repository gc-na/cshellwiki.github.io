# [Linux] Bash write käyttö: Viestien lähettäminen käyttäjille

## Overview
`write`-komento mahdollistaa viestien lähettämisen suoraan toisen käyttäjän terminaaliin Linux-järjestelmässä. Tämä on hyödyllistä, kun haluat kommunikoida reaaliaikaisesti ilman sähköpostia tai muita viestintävälineitä.

## Usage
Perussyntaksi `write`-komennolle on seuraava:

```
write [käyttäjä] [tty]
```

- `käyttäjä`: Käyttäjänimi, jolle viesti lähetetään.
- `tty`: (valinnainen) Terminaali, johon viesti lähetetään. Jos jätät tämän pois, käytetään oletusterminaalia.

## Common Options
- `-n`: Älä lähetä viestiä, jos vastaanottaja ei ole kirjautuneena sisään.
- `-s`: Lähetä viesti vain, jos vastaanottaja on kirjautuneena sisään.
- `-h`: Näytä apuviesti komennosta.

## Common Examples

### Esimerkki 1: Viestin lähettäminen käyttäjälle
Voit lähettää viestin käyttäjälle nimeltä "matti" seuraavasti:

```bash
write matti
Tervetuloa! Miten menee?
```

### Esimerkki 2: Viestin lähettäminen tiettyyn terminaaliin
Jos tiedät, että matti on kirjautuneena terminaaliin `pts/1`, voit lähettää viestin suoraan sinne:

```bash
write matti pts/1
Hei Matti, oletko valmis kokoukseen?
```

### Esimerkki 3: Viestin lähettäminen ilman terminaalia
Voit lähettää viestin ilman terminaalin määrittämistä, jolloin se menee oletusterminaaliin:

```bash
write matti
Muista tarkistaa sähköpostisi!
```

## Tips
- Varmista, että vastaanottaja on kirjautuneena sisään, jotta viesti menee perille.
- Käytä `Ctrl + D` lopettaaksesi viestin kirjoittamisen ja lähettääksesi sen.
- Muista, että vastaanottaja voi estää viestit käyttämällä `mesg n` -komentoa, jolloin et voi lähettää viestejä hänelle.