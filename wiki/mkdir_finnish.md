# [Linux] Bash mkdir käyttö: Luo hakemistoja

## Yleiskatsaus
`mkdir`-komento (make directory) on Bash-komento, jota käytetään uusien hakemistojen luomiseen tiedostojärjestelmässä. Tämä komento on hyödyllinen, kun haluat järjestää tiedostoja ja kansioita tehokkaasti.

## Käyttö
Perussyntaksi `mkdir`-komennolle on seuraava:

```bash
mkdir [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-p`: Luo tarvittaessa vanhemmat hakemistot.
- `-v`: Näyttää viestin jokaisesta luodusta hakemistosta.
- `--help`: Näyttää aputiedot `mkdir`-komennosta.

## Yleiset esimerkit
1. **Yhden hakemiston luominen:**
   ```bash
   mkdir uusi_hakemisto
   ```

2. **Useamman hakemiston luominen kerralla:**
   ```bash
   mkdir hakemisto1 hakemisto2 hakemisto3
   ```

3. **Hakemiston luominen vanhempien hakemistojen kanssa:**
   ```bash
   mkdir -p vanhempi/hakemisto/uusi_hakemisto
   ```

4. **Hakemiston luominen ja viestin näyttäminen:**
   ```bash
   mkdir -v uusi_hakemisto
   ```

## Vinkit
- Käytä `-p`-vaihtoehtoa, kun haluat luoda monitasoisia hakemistoja ilman virheilmoituksia, jos vanhempi hakemisto on jo olemassa.
- Tarkista aina, että sinulla on tarvittavat käyttöoikeudet hakemiston luomiseen haluamaasi sijaintiin.
- Hyödynnä `-v`-vaihtoehtoa, jos haluat varmistaa, että hakemistot on luotu onnistuneesti.