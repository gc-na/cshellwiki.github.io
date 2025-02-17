# [Linux] Bash rsync användning: Synkronisera filer och kataloger

## Översikt
Rsync är ett kraftfullt verktyg för att synkronisera filer och kataloger mellan olika platser, antingen lokalt eller över nätverket. Det är särskilt användbart för säkerhetskopiering och överföring av stora mängder data, eftersom det endast överför ändrade delar av filer, vilket sparar tid och bandbredd.

## Användning
Den grundläggande syntaxen för rsync är:

```bash
rsync [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Arkivera läge; kopierar filer och kataloger rekursivt och bevarar nästan alla attribut.
- `-v`: Verbos; visar detaljerad information om vad som kopieras.
- `-z`: Komprimera data under överföring för att spara bandbredd.
- `-r`: Rekursiv; kopiera kataloger och deras innehåll.
- `--delete`: Ta bort filer i destinationen som inte längre finns i källan.

## Vanliga exempel
Här är några praktiska exempel på hur man använder rsync:

1. **Kopiera en lokal katalog till en annan lokal plats:**
   ```bash
   rsync -av /källa/katalog/ /destination/katalog/
   ```

2. **Kopiera filer från en lokal katalog till en fjärrserver:**
   ```bash
   rsync -av /lokal/katalog/ användare@server:/fjärr/katalog/
   ```

3. **Kopiera filer från en fjärrserver till en lokal katalog:**
   ```bash
   rsync -av användare@server:/fjärr/katalog/ /lokal/katalog/
   ```

4. **Synkronisera och ta bort filer som inte längre finns i källan:**
   ```bash
   rsync -av --delete /källa/katalog/ /destination/katalog/
   ```

## Tips
- Använd `-n` (eller `--dry-run`) för att simulera en rsync-operation utan att faktiskt kopiera några filer. Detta är användbart för att se vad som skulle hända innan du gör det.
- Kontrollera alltid att du har rätt sökvägar för källan och destinationen för att undvika oavsiktlig datarförlust.
- Överväg att använda `-z` för att komprimera data om du överför stora filer över långsamma nätverksanslutningar.