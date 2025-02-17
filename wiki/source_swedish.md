# [Linux] Bash source användning: Ladda in skript i den aktuella skalen

## Översikt
Kommandot `source` används i Bash för att köra ett skript i den aktuella skalinstansen. Detta innebär att alla variabler och funktioner som definieras i skriptet blir tillgängliga i den aktuella sessionen, vilket skiljer sig från att köra skriptet direkt, där en ny skalinstans skapas.

## Användning
Den grundläggande syntaxen för kommandot `source` är:

```bash
source [alternativ] [argument]
```

Ett alternativt sätt att använda kommandot är att använda punkten (`.`) istället för `source`.

## Vanliga alternativ
- **`-`**: Används för att ange att skriptet ska köras i en ny skalinstans, men detta är inte standardanvändning för `source`.
  
## Vanliga exempel
Här är några praktiska exempel på hur man använder `source`:

1. Ladda ett skript som heter `myscript.sh`:

   ```bash
   source myscript.sh
   ```

2. Använda punkten för att ladda samma skript:

   ```bash
   . myscript.sh
   ```

3. Ladda en konfigurationsfil, som `.bashrc`, för att uppdatera den aktuella sessionens inställningar:

   ```bash
   source ~/.bashrc
   ```

4. Ladda en miljövariabelsfil:

   ```bash
   source env_variables.sh
   ```

## Tips
- Använd `source` för att ladda skript som innehåller funktioner eller variabler som du vill använda i din nuvarande session.
- Kontrollera att skriptet har körbehörighet innan du försöker ladda det.
- Använd `source` för att snabbt uppdatera din miljö utan att behöva starta om terminalen.