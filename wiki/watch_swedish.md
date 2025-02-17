# [Linux] Bash watch användning: övervaka kommandon i realtid

## Översikt
`watch`-kommandot används för att köra ett angivet kommando med jämna mellanrum och visa dess utdata i realtid. Detta är särskilt användbart för att övervaka förändringar i systemstatus eller filinnehåll.

## Användning
Den grundläggande syntaxen för `watch`-kommandot är:

```bash
watch [alternativ] [kommandon]
```

## Vanliga alternativ
- `-n, --interval`: Anger hur många sekunder som ska gå mellan körningarna av kommandot. Standard är 2 sekunder.
- `-d, --differences`: Markera skillnader mellan på varandra följande utdata.
- `-t, --no-title`: Tar bort titeln från övre delen av skärmen.
- `-x`: Kör kommandot med angivna argument.

## Vanliga exempel
Här är några praktiska exempel på hur `watch` kan användas:

1. Övervaka systemets minnesanvändning:
   ```bash
   watch -n 5 free -h
   ```

2. Övervaka en katalog för att se nya filer:
   ```bash
   watch -n 10 ls -l /path/to/directory
   ```

3. Visa skillnader i utdata från ett kommando:
   ```bash
   watch -d df -h
   ```

4. Övervaka en process med `ps`:
   ```bash
   watch -n 2 'ps aux | grep process_name'
   ```

## Tips
- Använd `-d` för att enkelt se vad som har förändrats mellan körningarna.
- Justera intervallet med `-n` för att anpassa hur ofta du vill se uppdateringar.
- Om du övervakar ett kommando som producerar mycket utdata, överväg att använda `-t` för att få en renare vy utan titel.