# [Linux] Bash rmdir käyttö: Poistaa tyhjät hakemistot

## Yleiskatsaus
`rmdir`-komento on Bash-komento, jota käytetään tyhjien hakemistojen poistamiseen. Komento ei voi poistaa hakemistoja, jotka sisältävät tiedostoja tai muita hakemistoja.

## Käyttö
Perussyntaksi `rmdir`-komennolle on seuraava:

```bash
rmdir [valinnat] [argumentit]
```

## Yleiset Valinnat
- `--ignore-fail-on-non-empty`: Ohittaa virheen, jos hakemisto ei ole tyhjä.
- `--verbose`: Näyttää lisätietoja poistoprosessista.
- `--help`: Näyttää aputiedot komennosta.

## Yleiset Esimerkit
Poistetaan tyhjät hakemistot:

```bash
rmdir tyhjahakemisto
```

Poistetaan useita tyhjiä hakemistoja kerralla:

```bash
rmdir hakemisto1 hakemisto2
```

Käytetään `--verbose`-valintaa, jotta saadaan lisätietoja:

```bash
rmdir --verbose tyhjahakemisto
```

Ohitetaan virhe, jos hakemisto ei ole tyhjä:

```bash
rmdir --ignore-fail-on-non-empty ei_tyhjahakemisto
```

## Vinkit
- Varmista, että hakemisto on tyhjennetty ennen `rmdir`-komennon käyttöä.
- Käytä `--verbose`-valintaa, jos haluat nähdä, mitä komento tekee.
- Jos haluat poistaa hakemiston, joka ei ole tyhjä, käytä `rm -r`-komentoa sen sijaan.