# [Linux] Bash sort käyttö: Järjestää tiedostojen rivit

## Yleiskatsaus
`sort`-komento on Bashissa käytettävä työkalu, joka järjestää tiedostojen rivit aakkosjärjestykseen tai numeerisesti. Se on hyödyllinen komento, kun haluat järjestää tietoa helposti ja nopeasti.

## Käyttö
Perussyntaksi `sort`-komennolle on seuraava:

```bash
sort [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-r`: Järjestää rivit käänteisessä järjestyksessä.
- `-n`: Järjestää rivit numeerisesti.
- `-u`: Poistaa kaksoiskappaleet, jolloin vain ainutlaatuiset rivit jäävät.
- `-k`: Määrittää, minkä kentän mukaan järjestetään.
- `-o`: Määrittää tulostustiedoston nimen.

## Yleiset esimerkit
### 1. Perusjärjestäminen
Järjestää tiedoston `data.txt` rivit aakkosjärjestykseen:
```bash
sort data.txt
```

### 2. Käänteinen järjestäminen
Järjestää tiedoston `data.txt` rivit käänteisessä aakkosjärjestyksessä:
```bash
sort -r data.txt
```

### 3. Numeerinen järjestäminen
Järjestää tiedoston `numbers.txt` rivit numeerisesti:
```bash
sort -n numbers.txt
```

### 4. Ainulaatuisten rivien saaminen
Poistaa kaksoiskappaleet tiedostosta `data.txt` ja järjestää rivit:
```bash
sort -u data.txt
```

### 5. Kenttäkohtainen järjestäminen
Järjestää tiedoston `data.txt` toisen kentän mukaan (oletetaan, että kentät on erotettu välilyönneillä):
```bash
sort -k 2 data.txt
```

### 6. Tulostaminen toiseen tiedostoon
Järjestää tiedoston `data.txt` ja tallentaa tuloksen `sorted_data.txt`-tiedostoon:
```bash
sort data.txt -o sorted_data.txt
```

## Vinkit
- Käytä `-o`-vaihtoehtoa, kun haluat tallentaa järjestetyt rivit suoraan tiedostoon, jotta alkuperäinen tiedosto ei muutu.
- Voit yhdistää `sort`-komennon muihin komentoihin, kuten `uniq`, saadaksesi tehokkaampia tuloksia.
- Muista, että `sort` käsittelee oletuksena aakkosjärjestystä, joten numeeriset tiedot kannattaa järjestää `-n`-vaihtoehdolla.