# [Linux] Bash date användning: Hämta och formatera datum och tid

## Översikt
`date`-kommandot används för att visa och formatera datum och tid i olika format. Det kan också användas för att ställa in systemets datum och tid.

## Användning
Den grundläggande syntaxen för `date`-kommandot är:

```bash
date [alternativ] [argument]
```

## Vanliga alternativ
- `+FORMAT`: Specificera ett format för utdata.
- `-u`: Visa datum och tid i UTC (koordinated universal time).
- `-d STRING`: Ange ett specifikt datum och tid att visa.
- `-s STRING`: Ställ in systemets datum och tid till det angivna värdet.

## Vanliga exempel
- Visa det aktuella datumet och tiden:
  ```bash
  date
  ```

- Visa datumet i ett specifikt format (t.ex. ÅÅÅÅ-MM-DD):
  ```bash
  date +"%Y-%m-%d"
  ```

- Visa datum och tid i UTC:
  ```bash
  date -u
  ```

- Visa ett specifikt datum (t.ex. 1 januari 2023):
  ```bash
  date -d "2023-01-01"
  ```

- Ställ in systemets datum och tid (kräver root-behörighet):
  ```bash
  sudo date -s "2023-01-01 12:00:00"
  ```

## Tips
- Använd `date +"%c"` för att visa datum och tid i ett format som är lätt att läsa.
- Experimentera med olika format för att få utdata som passar dina behov.
- Var försiktig när du ställer in systemets datum och tid, eftersom det kan påverka schemalagda uppgifter och loggar.