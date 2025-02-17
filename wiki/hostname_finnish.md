# [Linux] Bash hostname käyttö: Näyttää tai määrittää järjestelmän nimen

## Overview
`hostname`-komento on työkalu, jota käytetään näyttämään tai määrittämään järjestelmän nimen (hostname) Linux- ja Unix-pohjaisissa käyttöjärjestelmissä. Järjestelmän nimi on tärkeä, sillä se auttaa tunnistamaan laitteet verkossa.

## Usage
Perussyntaksi `hostname`-komennolle on seuraava:

```bash
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn`: Näyttää täydellisen pätevän järjestelmän nimen (FQDN).
- `-i`, `--ip-address`: Näyttää järjestelmän IP-osoitteen.
- `-s`, `--short`: Näyttää lyhyen järjestelmän nimen.
- `-V`, `--version`: Näyttää version tiedot.
- `--help`: Näyttää apu- ja käyttöohjeet.

## Common Examples
1. **Näytä nykyinen järjestelmän nimi:**
   ```bash
   hostname
   ```

2. **Näytä täydellinen pätevä järjestelmän nimi:**
   ```bash
   hostname -f
   ```

3. **Näytä järjestelmän IP-osoite:**
   ```bash
   hostname -i
   ```

4. **Määritä uusi järjestelmän nimi:**
   ```bash
   sudo hostname uusi_nimi
   ```

5. **Näytä lyhyt järjestelmän nimi:**
   ```bash
   hostname -s
   ```

## Tips
- Muista, että järjestelmän nimen muuttaminen saattaa vaatia järjestelmän uudelleenkäynnistämistä tai palveluiden uudelleenkäynnistämistä, jotta muutokset tulevat voimaan.
- Käytä `hostname`-komentoa yhdessä muiden verkko- ja järjestelmänhallintatyökalujen kanssa, kuten `ping` tai `ssh`, helpottaaksesi verkon hallintaa.
- Tarkista säännöllisesti järjestelmän nimi, erityisesti palvelimilla, joissa on useita verkkoliittymiä tai joissa käytetään virtuaalikoneita.