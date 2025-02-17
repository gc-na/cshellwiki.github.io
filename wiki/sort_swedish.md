# [Linux] Bash sort användning: Sortera rader i textfiler

## Översikt
Kommandot `sort` används för att sortera rader i textfiler eller standardinmatning. Det kan hantera både numeriska och alfabetiska sorteringar och erbjuder flera alternativ för att anpassa sorteringsprocessen.

## Användning
Den grundläggande syntaxen för kommandot `sort` är:

```bash
sort [alternativ] [argument]
```

## Vanliga alternativ
- `-r`: Sortera i omvänd ordning.
- `-n`: Sortera numeriskt istället för alfabetiskt.
- `-k`: Ange en specifik kolumn att sortera efter.
- `-u`: Ta bort dubbletter från sorteringsresultatet.
- `-o`: Skriv ut resultatet till en fil istället för standardutmatning.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `sort`:

1. **Sortera en fil alfabetiskt:**
   ```bash
   sort fil.txt
   ```

2. **Sortera en fil i omvänd ordning:**
   ```bash
   sort -r fil.txt
   ```

3. **Sortera numeriskt:**
   ```bash
   sort -n nummer.txt
   ```

4. **Sortera efter en specifik kolumn (t.ex. kolumn 2):**
   ```bash
   sort -k 2 fil.txt
   ```

5. **Ta bort dubbletter och sortera:**
   ```bash
   sort -u fil.txt
   ```

6. **Spara sorterat resultat till en ny fil:**
   ```bash
   sort -o sorterad.txt fil.txt
   ```

## Tips
- Använd `-n` för att säkerställa att siffror sorteras korrekt, särskilt om filen innehåller både text och siffror.
- Kombinera flera alternativ för att skräddarsy sorteringen efter dina behov, till exempel `sort -r -n`.
- Tänk på att `sort` är känsligt för stora och små bokstäver; använd `-f` för att ignorera skillnader i bokstavsstorlek.