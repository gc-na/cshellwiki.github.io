# [Linux] Bash dmesg käyttö: Näyttää ydinviestit

## Yleiskatsaus
`dmesg`-komento näyttää ydinviestit, jotka liittyvät järjestelmän käynnistämiseen ja laitteistotapahtumiin. Se on hyödyllinen työkalu ongelmien diagnosointiin ja järjestelmän tilan tarkastamiseen.

## Käyttö
Perussyntaksi `dmesg`-komennolle on seuraava:
```bash
dmesg [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-C` tai `--clear`: Tyhjentää nykyiset dmesg-viestit.
- `-c` tai `--clear`: Tyhjentää viestit ja näyttää ne sitten.
- `-n <taso>`: Asettaa lokitason, joka määrittää, mitkä viestit näytetään.
- `-T`: Näyttää aikaleimat inhimillisessä muodossa.
- `-H`: Näyttää viestit "human-readable" -muodossa.

## Yleiset esimerkit
1. Näytä kaikki dmesg-viestit:
   ```bash
   dmesg
   ```

2. Näytä dmesg-viestit aikaleimoilla:
   ```bash
   dmesg -T
   ```

3. Tyhjennä dmesg-viestit ja näytä ne:
   ```bash
   dmesg -c
   ```

4. Suodata viestit tietyllä tasolla (esim. vain virheet):
   ```bash
   dmesg -n 3
   ```

5. Näytä vain viimeiset 10 viestiä:
   ```bash
   dmesg | tail -n 10
   ```

## Vinkit
- Käytä `dmesg -T` -vaihtoehtoa, jos haluat nähdä aikaleimat helpommin luettavassa muodossa.
- Tyhjennä viestit säännöllisesti, jos työskentelet laitteistodiagnostiikan parissa, jotta vanhat viestit eivät häiritse.
- Yhdistä `dmesg`-komento muihin komentoihin, kuten `grep`, suodataksesi tiettyjä viestejä tai virheitä.