# [Linux] Bash journalctl käyttö: Näyttää järjestelmälokit

## Overview
`journalctl` on komento, joka mahdollistaa järjestelmälogien tarkastelun ja hallinnan systemd-journalissa. Se tarjoaa käyttäjille mahdollisuuden selata ja suodattaa lokitietoja eri kriteerien mukaan, mikä on hyödyllistä vianetsinnässä ja järjestelmänvalvonnassa.

## Usage
Perussyntaksi `journalctl`-komennolle on seuraava:

```bash
journalctl [options] [arguments]
```

## Common Options
- `-b` tai `--boot`: Näyttää lokitiedot vain nykyisestä käynnistyksestä.
- `-f` tai `--follow`: Seuraa lokitietoja reaaliajassa, kuin `tail -f`.
- `-u` tai `--unit`: Suodattaa lokitietoja tietyn palveluyksikön mukaan.
- `--since`: Näyttää lokitiedot tietystä ajankohdasta alkaen.
- `--until`: Näyttää lokitiedot tiettyyn ajankohtaan saakka.

## Common Examples
1. Näytä kaikki lokitiedot:
   ```bash
   journalctl
   ```

2. Näytä lokitiedot vain nykyisestä käynnistyksestä:
   ```bash
   journalctl -b
   ```

3. Seuraa lokitietoja reaaliajassa:
   ```bash
   journalctl -f
   ```

4. Suodata lokitietoja tietyn palveluyksikön mukaan (esim. `ssh.service`):
   ```bash
   journalctl -u ssh.service
   ```

5. Näytä lokitiedot tietystä ajankohdasta alkaen:
   ```bash
   journalctl --since "2023-10-01 10:00:00"
   ```

## Tips
- Käytä `-p`-valitsinta suodattaaksesi lokitietoja lokitason mukaan, esimerkiksi `journalctl -p err` näyttää vain virheelliset lokit.
- Voit yhdistää useita vaihtoehtoja, kuten `journalctl -b -u nginx.service -f` seuratakseen Nginx-palvelun lokitietoja nykyisestä käynnistyksestä.
- Muista, että lokitiedot voivat olla suuria, joten suodatus ja aikarajojen asettaminen voivat helpottaa tietojen käsittelyä.