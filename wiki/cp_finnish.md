# [Linux] Bash cp käyttö: Tiedostojen kopioiminen

## Yleiskatsaus
`cp`-komento on Bash-käsky, jota käytetään tiedostojen ja hakemistojen kopioimiseen. Se mahdollistaa tiedostojen siirtämisen paikasta toiseen, joko samalla laitteella tai eri laitteilla.

## Käyttö
Perussyntaksi `cp`-komennolle on seuraava:

```bash
cp [valinnat] [argumentit]
```

## Yleiset valinnat
- `-r`: Kopioi hakemiston ja sen sisällön rekursiivisesti.
- `-i`: Kysyy vahvistusta ennen olemassa olevan tiedoston korvaamista.
- `-u`: Kopioi vain, jos lähdetiedosto on uudempi kuin kohdetiedosto tai jos kohdetiedostoa ei ole.
- `-v`: Näyttää, mitä tiedostoja kopioidaan (verbose-tila).

## Yleiset esimerkit

1. **Yksittäisen tiedoston kopioiminen:**
   ```bash
   cp tiedosto.txt kopio_tiedosto.txt
   ```

2. **Hakemiston kopioiminen rekursiivisesti:**
   ```bash
   cp -r hakemisto/ kopio_hakemisto/
   ```

3. **Tiedoston kopioiminen ja vahvistus ennen korvaamista:**
   ```bash
   cp -i tiedosto.txt kohde_tiedosto.txt
   ```

4. **Kopioi vain uudemmat tiedostot:**
   ```bash
   cp -u tiedosto.txt kohde_tiedosto.txt
   ```

5. **Näytä kopiointiprosessi:**
   ```bash
   cp -v tiedosto.txt kohde_tiedosto.txt
   ```

## Vinkit
- Käytä `-i`-valintaa, kun olet epävarma siitä, että tiedostoja ei korvata vahingossa.
- Muista käyttää `-r`-valintaa, kun kopioit hakemistoja, jotta kaikki alihakemistot ja tiedostot kopioituvat oikein.
- Voit yhdistää useita valintoja, kuten `cp -riv`, jolloin saat sekä rekursiivisen kopioinnin että verbose-tilan päälle.