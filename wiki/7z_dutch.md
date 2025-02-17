# [Linux] Bash 7z gebruik: Bestanden en mappen comprimeren en decomprimeren

## Overzicht
De `7z`-opdracht is een krachtige tool voor het comprimeren en decomprimeren van bestanden en mappen. Het maakt gebruik van het 7z-bestandsformaat, dat bekend staat om zijn hoge compressieverhouding en ondersteuning voor verschillende compressiemethoden.

## Gebruik
De basis syntaxis van de `7z`-opdracht is als volgt:

```bash
7z [opties] [argumenten]
```

## Veelvoorkomende Opties
- `a`: Voeg bestanden toe aan een archief.
- `x`: Extraheer bestanden uit een archief.
- `l`: Lijst de inhoud van een archief.
- `d`: Verwijder bestanden uit een archief.
- `t`: Test de integriteit van een archief.

## Veelvoorkomende Voorbeelden

1. **Een archief maken:**
   Om een archief te maken met de naam `mijnarchief.7z` en de bestanden `bestand1.txt` en `bestand2.txt` toe te voegen, gebruik je:

   ```bash
   7z a mijnarchief.7z bestand1.txt bestand2.txt
   ```

2. **Bestanden extraheren:**
   Om bestanden uit een archief genaamd `mijnarchief.7z` te extraheren, gebruik je:

   ```bash
   7z x mijnarchief.7z
   ```

3. **Inhoud van een archief weergeven:**
   Om de inhoud van `mijnarchief.7z` te bekijken, gebruik je:

   ```bash
   7z l mijnarchief.7z
   ```

4. **Bestanden verwijderen uit een archief:**
   Om `bestand1.txt` te verwijderen uit `mijnarchief.7z`, gebruik je:

   ```bash
   7z d mijnarchief.7z bestand1.txt
   ```

5. **Integriteit van een archief testen:**
   Om de integriteit van `mijnarchief.7z` te testen, gebruik je:

   ```bash
   7z t mijnarchief.7z
   ```

## Tips
- Zorg ervoor dat je de juiste opties gebruikt om onbedoeld gegevensverlies te voorkomen, vooral bij het verwijderen van bestanden uit een archief.
- Gebruik de `-p` optie om een wachtwoord in te stellen voor extra beveiliging van je archieven.
- Maak regelmatig back-ups van belangrijke archieven om gegevensverlies te voorkomen.