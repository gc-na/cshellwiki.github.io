# [Linux] C Shell (csh) md5sum gebruik: Controleer de integriteit van bestanden

## Overzicht
De `md5sum`-opdracht genereert en controleert MD5-hashes van bestanden. Dit is nuttig om de integriteit van bestanden te verifiëren, bijvoorbeeld na het downloaden of overdragen van bestanden.

## Gebruik
De basis syntaxis van de `md5sum`-opdracht is als volgt:

```csh
md5sum [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-b`: Behandel bestanden als binaire bestanden.
- `-c`: Controleer MD5-hashes van bestanden die zijn opgeslagen in een bestand.
- `-t`: Behandel bestanden als tekstbestanden.
- `--help`: Toon een helpbericht met informatie over het gebruik van de opdracht.

## Veelvoorkomende Voorbeelden

1. **MD5-hash genereren van een bestand:**

```csh
md5sum voorbeeld.txt
```

2. **MD5-hash genereren en opslaan in een bestand:**

```csh
md5sum voorbeeld.txt > hash.txt
```

3. **Controleer de MD5-hash van een bestand met een hashbestand:**

```csh
md5sum -c hash.txt
```

4. **MD5-hash genereren van meerdere bestanden:**

```csh
md5sum bestand1.txt bestand2.txt
```

## Tips
- Gebruik altijd de `-c` optie om de integriteit van bestanden te controleren na het downloaden.
- Sla de MD5-hashes op in een apart bestand voor toekomstige referentie.
- Wees voorzichtig met het gebruik van MD5 voor cryptografische doeleinden, aangezien het niet meer als veilig wordt beschouwd voor gevoelige gegevens.