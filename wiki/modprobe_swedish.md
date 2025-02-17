# [Linux] Bash modprobe användning: Ladda moduler i kärnan

## Översikt
Kommandot `modprobe` används för att ladda och avlasta kärnmoduler i Linux. Det hanterar beroenden mellan moduler och säkerställer att alla nödvändiga moduler laddas när en specifik modul aktiveras.

## Användning
Den grundläggande syntaxen för `modprobe` är:

```bash
modprobe [alternativ] [argument]
```

## Vanliga alternativ
- `-r`, `--remove`: Avlasta en modul.
- `-n`, `--dry-run`: Visa vilka moduler som skulle laddas utan att faktiskt göra det.
- `-v`, `--verbose`: Visa detaljerad information om vad som händer under körningen.
- `--show-depends`: Visa beroenden för en modul.

## Vanliga exempel
Ladda en modul:
```bash
modprobe <modulnamn>
```

Avlasta en modul:
```bash
modprobe -r <modulnamn>
```

Visa beroenden för en modul:
```bash
modprobe --show-depends <modulnamn>
```

Kör en torrkörning för att se vilka moduler som skulle laddas:
```bash
modprobe -n <modulnamn>
```

## Tips
- Kontrollera alltid vilka moduler som är laddade med `lsmod` innan du försöker ladda nya moduler.
- Använd `modprobe -v` för att få mer information om vad som händer när du laddar eller avlastar moduler.
- Var försiktig när du avlastar moduler, eftersom det kan påverka systemets stabilitet om moduler som används av andra processer tas bort.