# [Linux] Bash rmmod käyttö: Poistaa moduuleja Linux-kernelistä

## Yleiskatsaus
`rmmod`-komento on käytössä Linux-järjestelmissä ja sen avulla voidaan poistaa moduuleja kernelistä. Moduulit ovat ohjelmisto-osia, jotka laajentavat kernelin toiminnallisuutta, ja `rmmod` mahdollistaa niiden poistamisen, kun niitä ei enää tarvita.

## Käyttö
Perussyntaksi `rmmod`-komennolle on seuraava:

```bash
rmmod [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-f`: Pakottaa moduulin poistamisen, vaikka se olisi käytössä.
- `-n`: Näyttää vain, mitä moduuli poistettaisiin, ilman varsinaista poistoa.
- `--help`: Näyttää apuviestin ja käytettävissä olevat vaihtoehdot.

## Yleiset esimerkit
Poista moduuli nimeltä `example_module`:

```bash
rmmod example_module
```

Pakota moduulin `example_module` poistaminen:

```bash
rmmod -f example_module
```

Näytä, mitä moduuli poistettaisiin ilman varsinaista poistoa:

```bash
rmmod -n example_module
```

## Vinkit
- Varmista, että moduuli ei ole käytössä ennen sen poistamista, jotta vältät mahdolliset järjestelmäongelmat.
- Käytä `lsmod`-komentoa tarkistaaksesi, mitkä moduulit ovat tällä hetkellä ladattuna.
- Ole varovainen `-f`-vaihtoehdon käytössä, sillä se voi aiheuttaa järjestelmän epävakauden, jos moduuli on kriittisessä käytössä.