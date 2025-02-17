# [Linux] Bash dmesg användning: Visa kernelmeddelanden

## Översikt
Kommandot `dmesg` används för att visa meddelanden från kärnan (kernel) i Linux-systemet. Dessa meddelanden kan ge insikter om systemets hårdvarukomponenter, drivrutiner och andra viktiga systemhändelser.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
dmesg [alternativ] [argument]
```

## Vanliga alternativ
- `-C`: Rensa meddelandeloggen.
- `-c`: Visa meddelanden och rensa loggen efteråt.
- `-n LEVEL`: Ställ in nivån för meddelanden som ska visas.
- `-T`: Visa tidsstämplar i mänskligt läsbart format.
- `--help`: Visa hjälpmeddelande för kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `dmesg`:

1. Visa alla kärnmeddelanden:
   ```bash
   dmesg
   ```

2. Visa meddelanden med tidsstämplar:
   ```bash
   dmesg -T
   ```

3. Rensa meddelandeloggen:
   ```bash
   dmesg -C
   ```

4. Visa meddelanden med en specifik nivå:
   ```bash
   dmesg -n 1
   ```

5. Visa meddelanden och rensa loggen efteråt:
   ```bash
   dmesg -c
   ```

## Tips
- Använd `dmesg | less` för att bläddra igenom långa loggar.
- Kombinera `dmesg` med `grep` för att filtrera specifika meddelanden, till exempel:
  ```bash
  dmesg | grep error
  ```
- Kontrollera dmesg-loggar efter att ha installerat ny hårdvara eller drivrutiner för att säkerställa att allt fungerar korrekt.