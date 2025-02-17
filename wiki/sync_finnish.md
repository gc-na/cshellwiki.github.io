# [Linux] Bash sync käyttö: Tiedostojärjestelmän synkronointi

## Yleiskatsaus
`sync`-komento on yksinkertainen työkalu, joka varmistaa, että kaikki tiedostojärjestelmän välimuistissa olevat tiedot kirjoitetaan pysyvään muistiin. Tämä on erityisen tärkeää, kun halutaan varmistaa, että kaikki muutokset, kuten tiedostojen luominen tai muokkaaminen, tallennetaan oikein ennen järjestelmän sammutusta tai uudelleenkäynnistystä.

## Käyttö
Perussyntaksi `sync`-komennolle on seuraava:

```bash
sync [options] [arguments]
```

## Yleiset vaihtoehdot
- `-f`: Pakottaa välimuistin tyhjentämisen, vaikka tiedostojärjestelmä ei olisi muuttunut.
- `-d`: Varmistaa, että tiedostojärjestelmän tiedot synkronoidaan ennen kuin komento päättyy.

## Yleiset esimerkit
1. **Perus synkronointi**:
   ```bash
   sync
   ```
   Tämä komento synkronoi kaikki välimuistissa olevat tiedot.

2. **Pakotettu synkronointi**:
   ```bash
   sync -f
   ```
   Tämä komento pakottaa välimuistin tyhjentämisen, vaikka ei olisi tapahtunut muutoksia.

3. **Synkronointi ja uudelleenkäynnistys**:
   ```bash
   sync && reboot
   ```
   Tämä komento synkronoi tiedot ja käynnistää sitten järjestelmän uudelleen.

## Vinkit
- Käytä `sync`-komentoa ennen järjestelmän sammutusta tai uudelleenkäynnistystä varmistaaksesi, että kaikki tiedot on tallennettu.
- Voit yhdistää `sync`-komennon muihin komentoihin, kuten `shutdown` tai `reboot`, varmistaaksesi, että tiedot synkronoidaan ennen toiminnan suorittamista.
- Muista, että `sync` ei palauta mitään tietoa, joten se ei näytä mitään tulosteita onnistuneesta synkronoinnista.