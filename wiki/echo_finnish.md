# [Linux] Bash echo käyttö: Tulostaa tekstiä komentoriville

## Yleiskatsaus
`echo`-komento on Bashin peruskomento, joka tulostaa annettua tekstiä tai muuttujan arvoja komentoriville. Sitä käytetään usein skripteissä ja komentorivillä tiedon näyttämiseen.

## Käyttö
Perussyntaksi `echo`-komennolle on seuraava:

```
echo [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-n`: Älä tulosta rivinvaihtoa lopussa.
- `-e`: Ota käyttöön erikoismerkit, kuten `\n` (rivinvaihto) ja `\t` (tabulaattori).
- `-E`: Estää erikoismerkkien käytön (oletus).

## Yleiset esimerkit
Tulostetaan yksinkertainen teksti:
```bash
echo "Hei maailma!"
```

Tulostetaan teksti ilman rivinvaihtoa:
```bash
echo -n "Tämä on ilman rivinvaihtoa."
```

Tulostetaan teksti erikoismerkkien kanssa:
```bash
echo -e "Rivi 1\nRivi 2"
```

Tulostetaan ympäristömuuttujan arvo:
```bash
echo "Käyttäjänimi: $USER"
```

## Vinkit
- Käytä `-n`-vaihtoehtoa, kun haluat liittää useita tulosteita samaan riviin.
- Muista, että `echo` voi tulostaa myös muuttujien arvoja, mikä tekee siitä hyödyllisen skripteissä.
- Erikoismerkkien käyttö `-e`-vaihtoehdolla voi helpottaa monimutkaisempien tulosteiden luomista.