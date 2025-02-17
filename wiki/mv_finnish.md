# [Linux] Bash mv käyttö: Tiedostojen ja kansioiden siirtäminen tai nimeäminen

## Yleiskatsaus
`mv`-komento on Bash-komento, jota käytetään tiedostojen ja kansioiden siirtämiseen tai nimeämiseen. Se on yksi peruskomento, jota käytetään usein tiedostojärjestelmässä.

## Käyttö
Perussyntaksi `mv`-komennolle on seuraava:

```bash
mv [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-i`: Kysy vahvistusta ennen olemassa olevan tiedoston ylikirjoittamista.
- `-u`: Siirrä vain, jos lähdetiedosto on uudempi kuin kohdetiedosto tai jos kohdetiedostoa ei ole.
- `-v`: Näytä siirrettävät tiedostot yksityiskohtaisesti.

## Yleiset esimerkit
Siirretään tiedosto nimeltä `dokumentti.txt` kansioon `asiakirjat`:

```bash
mv dokumentti.txt asiakirjat/
```

Nimetään tiedosto `vanha_nimi.txt` uudelleen `uusi_nimi.txt`:ksi:

```bash
mv vanha_nimi.txt uusi_nimi.txt
```

Siirretään useita tiedostoja kerralla kansioon `kuvat`:

```bash
mv kuva1.jpg kuva2.jpg kuva3.jpg kuvat/
```

Käytetään interaktiivista vaihtoehtoa, jolloin kysytään vahvistusta ennen ylikirjoittamista:

```bash
mv -i vanha_tiedosto.txt uusi_tiedosto.txt
```

## Vinkit
- Käytä `-v`-vaihtoehtoa, jos haluat nähdä, mitä tiedostoja siirretään.
- Varmista, että tiedostopolut ovat oikein, erityisesti kun käytät suhteellisia polkuja.
- Ole varovainen ylikirjoittaessasi tiedostoja, erityisesti ilman `-i`-vaihtoehtoa, jotta et menetä tärkeitä tietoja.