# [Linux] C Shell (csh) strace gebruik: Volg systeemaanroepen en signalen

## Overzicht
De `strace`-opdracht is een krachtig hulpmiddel dat wordt gebruikt om systeemaanroepen en signalen van een proces te volgen. Het biedt inzicht in de interactie van een programma met de kernel, wat nuttig kan zijn voor foutopsporing en prestatie-analyse.

## Gebruik
De basis syntaxis van de `strace`-opdracht is als volgt:

```csh
strace [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Geef een samenvatting van systeemaanroepen en hun statistieken.
- `-e`: Beperk de output tot specifieke systeemaanroepen.
- `-p`: Volg een bestaand proces met de opgegeven PID.
- `-o`: Schrijf de output naar een bestand in plaats van naar de standaarduitvoer.
- `-f`: Volg ook kindprocessen die door het doelproces worden gemaakt.

## Veelvoorkomende Voorbeelden

1. **Basis gebruik van strace**:
   Volg de systeemaanroepen van een programma, bijvoorbeeld `ls`:
   ```csh
   strace ls
   ```

2. **Output naar een bestand schrijven**:
   Schrijf de output van `strace` naar een bestand genaamd `output.txt`:
   ```csh
   strace -o output.txt ls
   ```

3. **Volgen van een bestaand proces**:
   Volg een proces met PID 1234:
   ```csh
   strace -p 1234
   ```

4. **Samenvatting van systeemaanroepen**:
   Verkrijg een samenvatting van de systeemaanroepen die door `cat` worden gemaakt:
   ```csh
   strace -c cat bestand.txt
   ```

5. **Beperk de output tot specifieke aanroepen**:
   Volg alleen de `open` en `close` systeemaanroepen van een proces:
   ```csh
   strace -e trace=open,close ls
   ```

## Tips
- Gebruik `-f` om ook kindprocessen te volgen, wat nuttig is bij programma's die meerdere processen aanmaken.
- Combineer `-c` met andere opties voor een snelle samenvatting van de prestaties van een programma.
- Wees voorzichtig met het volgen van processen die veel systeemaanroepen genereren, omdat de output snel overweldigend kan worden.