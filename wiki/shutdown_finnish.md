# [Linux] Bash shutdown käyttö: Sammuttaa tai käynnistää järjestelmä

## Yleiskatsaus
`shutdown`-komento on käytössä Linux- ja Unix-pohjaisissa järjestelmissä, ja sen avulla voidaan sammuttaa tai käynnistää järjestelmä turvallisesti. Komento mahdollistaa myös aikarajojen asettamisen ja järjestelmän ilmoittamisen käyttäjille ennen sammuttamista.

## Käyttö
Perussyntaksi `shutdown`-komennolle on seuraava:

```bash
shutdown [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h` tai `--halt`: Sammuttaa järjestelmän.
- `-r` tai `--reboot`: Käynnistää järjestelmän uudelleen.
- `-P` tai `--poweroff`: Samalla tavalla kuin `-h`, mutta varmistaa, että virta katkaistaan.
- `+m`: Asettaa aikarajan minuutteina, esimerkiksi `+5` sammuttaa järjestelmän viiden minuutin kuluttua.
- `hh:mm`: Asettaa tarkka aika, jolloin järjestelmä sammutetaan, esimerkiksi `23:00`.

## Yleiset esimerkit
1. **Sammuta järjestelmä heti:**
   ```bash
   shutdown -h now
   ```

2. **Käynnistä järjestelmä uudelleen:**
   ```bash
   shutdown -r now
   ```

3. **Sammuta järjestelmä viiden minuutin kuluttua:**
   ```bash
   shutdown +5
   ```

4. **Sammuta järjestelmä tiettynä aikana (esim. klo 22:00):**
   ```bash
   shutdown 22:00
   ```

5. **Sammuta järjestelmä ja ilmoita käyttäjille:**
   ```bash
   shutdown -h +10 "Järjestelmä sammuu 10 minuutin kuluttua. Tallenna työsi!"
   ```

## Vinkit
- Varmista, että olet kirjautunut järjestelmään pääkäyttäjänä tai sinulla on tarvittavat oikeudet `shutdown`-komennon suorittamiseen.
- Käytä `shutdown -c` peruuttaaksesi aikaisemmin asetetun sammuttamisen.
- Ilmoita käyttäjille etukäteen, jotta he voivat tallentaa työnsä ennen järjestelmän sammuttamista tai uudelleenkäynnistämistä.