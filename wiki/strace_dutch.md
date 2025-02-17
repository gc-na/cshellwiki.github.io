# [Linux] Bash strace gebruik: systeemaanroep-tracering

## Overzicht
De `strace`-opdracht is een krachtige tool in Linux die wordt gebruikt om systeemaanroepen en signalen die door een proces worden gemaakt, te traceren. Dit is bijzonder nuttig voor het debuggen van applicaties en het begrijpen van hun interactie met het besturingssysteem.

## Gebruik
De basisstructuur van de `strace`-opdracht is als volgt:

```bash
strace [opties] [argumenten]
```

## Veelvoorkomende opties
- `-e trace=<type>`: Beperk de uitvoer tot specifieke systeemaanroepen, zoals `file` of `network`.
- `-p <pid>`: Volg een bestaand proces met het opgegeven proces-ID.
- `-o <bestand>`: Schrijf de uitvoer naar een bestand in plaats van naar de standaarduitvoer.
- `-c`: Geef een samenvatting van systeemaanroepen en hun statistieken weer.
- `-f`: Volg ook kindprocessen die door het hoofdproces worden gemaakt.

## Veelvoorkomende voorbeelden

1. **Basis gebruik van strace**:
   ```bash
   strace ls
   ```
   Dit toont alle systeemaanroepen die worden uitgevoerd door het `ls`-commando.

2. **Systeemaanroepen filteren**:
   ```bash
   strace -e trace=open,read ls
   ```
   Dit toont alleen de `open` en `read` systeemaanroepen die door `ls` worden uitgevoerd.

3. **Een bestaand proces volgen**:
   ```bash
   strace -p 1234
   ```
   Dit volgt het proces met het proces-ID 1234 en toont de systeemaanroepen die het maakt.

4. **Uitvoer naar een bestand schrijven**:
   ```bash
   strace -o output.txt ls
   ```
   Dit schrijft de uitvoer van `strace` naar het bestand `output.txt`.

5. **Statistieken van systeemaanroepen**:
   ```bash
   strace -c ls
   ```
   Dit geeft een samenvatting van de systeemaanroepen die door `ls` zijn uitgevoerd, inclusief het aantal en de tijd die aan elke aanroep is besteed.

## Tips
- Gebruik `strace` in combinatie met andere commando's om de uitvoer te filteren en gerichter te analyseren.
- Wees voorzichtig met het volgen van processen in productieomgevingen, omdat `strace` de prestaties kan beïnvloeden.
- Combineer `strace` met de `-f` optie om ook kindprocessen te traceren, wat nuttig kan zijn bij complexe applicaties.