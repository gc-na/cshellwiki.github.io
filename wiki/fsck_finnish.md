# [Linux] Bash fsck käyttö: Tiedostojärjestelmän tarkistus ja korjaus

## Yleiskatsaus
`fsck` (file system consistency check) on komento, jota käytetään tiedostojärjestelmien tarkistamiseen ja mahdollisten virheiden korjaamiseen Linux- ja Unix-pohjaisissa käyttöjärjestelmissä. Se auttaa varmistamaan, että tiedostojärjestelmä on eheä ja toimiva.

## Käyttö
Perussyntaksi `fsck`-komennolle on seuraava:
```bash
fsck [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a` tai `--auto`: Korjaa automaattisesti löydetyt virheet ilman käyttäjän vahvistusta.
- `-n` tai `--no`: Suorittaa tarkistuksen ilman korjauksia.
- `-y`: Vastaa automaattisesti "kyllä" kaikkiin kysymyksiin, jotka vaativat käyttäjän vahvistusta.
- `-f`: Pakottaa tarkistuksen, vaikka tiedostojärjestelmä olisi merkitty ehjäksi.

## Yleiset esimerkit
1. **Perustarkistus**:
   Tarkista tiedostojärjestelmä `/dev/sda1`:
   ```bash
   fsck /dev/sda1
   ```

2. **Automaattinen korjaus**:
   Korjaa automaattisesti virheet tiedostojärjestelmässä:
   ```bash
   fsck -a /dev/sda1
   ```

3. **Tarkistus ilman korjauksia**:
   Suorita tarkistus ilman korjaustoimenpiteitä:
   ```bash
   fsck -n /dev/sda1
   ```

4. **Pakotettu tarkistus**:
   Pakota tarkistus, vaikka tiedostojärjestelmä olisi ehjä:
   ```bash
   fsck -f /dev/sda1
   ```

## Vinkit
- Suorita `fsck` vain, kun tiedostojärjestelmä ei ole käytössä. Tämä voi vaatia järjestelmän käynnistämistä pelkästään komentoriviltä.
- Varmista, että sinulla on varmuuskopiot tärkeistä tiedostoista ennen `fsck`-komennon käyttöä, erityisesti, jos käytät automaattisia korjauksia.
- Käytä `-y`-vaihtoehtoa vain, jos olet varma, että haluat hyväksyä kaikki ehdotetut muutokset.