# [Linux] Bash modprobe käyttö: Laitteiden ajureiden hallinta

## Yleiskatsaus
`modprobe` on komento, jota käytetään Linux-järjestelmissä laitteiden ajureiden lataamiseen ja hallintaan. Se mahdollistaa ajureiden automaattisen lataamisen riippuvuuksien perusteella, mikä helpottaa laitteistotuen hallintaa.

## Käyttö
Perussyntaksi `modprobe`-komennolle on seuraava:

```bash
modprobe [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-r`, `--remove`: Poistaa moduulin (ajurin) käytöstä.
- `-n`, `--dry-run`: Näyttää, mitä komento tekisi ilman, että se todella suoritetaan.
- `-v`, `--verbose`: Näyttää lisätietoja komennon suorittamisesta.
- `--show`: Näyttää moduulin tiedot ilman sen lataamista.

## Yleiset esimerkit
1. **Moduulin lataaminen**:
   ```bash
   modprobe nvidia
   ```
   Tämä komento lataa NVIDIA:n grafiikka-ajurin.

2. **Moduulin poistaminen**:
   ```bash
   modprobe -r nvidia
   ```
   Tämä komento poistaa NVIDIA:n grafiikka-ajurin käytöstä.

3. **Kuivaharjoitus (dry run)**:
   ```bash
   modprobe -n nvidia
   ```
   Tämä komento näyttää, mitä tapahtuisi, jos NVIDIA-ajuri yritettäisiin ladata, mutta ei suorita latausta.

4. **Yksityiskohtaiset tiedot**:
   ```bash
   modprobe --show nvidia
   ```
   Tämä komento näyttää tietoja NVIDIA-moduulista ilman sen lataamista.

## Vinkit
- Varmista, että ajuri on saatavilla ja oikein asennettu ennen sen lataamista.
- Käytä `-v`-vaihtoehtoa virheiden selvittämiseen, jos moduulin lataaminen epäonnistuu.
- Tarkista riippuvuudet ennen moduulin lataamista, jotta vältät ongelmat laitteiston toiminnassa.