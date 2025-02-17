# [Linux] Bash tee användning: Kopiera och skriv ut data

## Översikt
Kommandot `tee` används för att läsa från standardinmatning och skriva till både standardutmatning och en eller flera filer. Det är särskilt användbart när du vill se utdata på skärmen samtidigt som du sparar den i en fil.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
tee [alternativ] [argument]
```

## Vanliga alternativ
- `-a`, `--append`: Lägg till utdata i slutet av filen istället för att skriva över den.
- `-i`, `--ignore-interrupts`: Ignorera avbrottssignaler.
- `--help`: Visa hjälpmeddelande för kommandot.
- `--version`: Visa versionsinformation för `tee`.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `tee`:

1. **Skriva ut och spara utdata till en fil:**
   ```bash
   echo "Hej världen" | tee fil.txt
   ```

2. **Lägga till utdata i en befintlig fil:**
   ```bash
   echo "Ny rad" | tee -a fil.txt
   ```

3. **Skriva ut utdata till flera filer:**
   ```bash
   echo "Data till flera filer" | tee fil1.txt fil2.txt
   ```

4. **Använda med en annan kommando:**
   ```bash
   ls -l | tee lista.txt
   ```

## Tips
- Använd `-a` alternativet om du vill bevara tidigare innehåll i filen när du skriver till den.
- Tänk på att `tee` kan användas i kedjor med andra kommandon för att fånga utdata på olika steg i en process.
- Om du bara vill se utdata utan att spara den, kan du använda `cat` istället för `tee`.