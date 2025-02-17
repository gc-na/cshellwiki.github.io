# [Linux] Bash cp användning: Kopiera filer och kataloger

## Översikt
`cp`-kommandot används för att kopiera filer och kataloger i Linux och andra Unix-liknande operativsystem. Det är ett grundläggande verktyg för filhantering som gör det enkelt att duplicera data.

## Användning
Den grundläggande syntaxen för `cp`-kommandot är:

```bash
cp [alternativ] [källfil] [målfil]
```

## Vanliga alternativ
- `-r`: Kopiera kataloger rekursivt.
- `-i`: Fråga innan en befintlig fil skrivs över.
- `-u`: Kopiera endast om källfilen är nyare än målfilerna eller om målfilerna inte finns.
- `-v`: Visa detaljerad information om vad som kopieras.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `cp`:

1. **Kopiera en fil till en annan plats:**
   ```bash
   cp fil.txt /sökväg/till/mål/
   ```

2. **Kopiera en katalog och dess innehåll:**
   ```bash
   cp -r /sökväg/till/katalog /sökväg/till/mål/
   ```

3. **Kopiera en fil och be om bekräftelse om den redan finns:**
   ```bash
   cp -i fil.txt /sökväg/till/mål/
   ```

4. **Kopiera en fil och visa vad som kopieras:**
   ```bash
   cp -v fil.txt /sökväg/till/mål/
   ```

5. **Uppdatera en fil endast om källan är nyare:**
   ```bash
   cp -u fil.txt /sökväg/till/mål/
   ```

## Tips
- Använd `-i` alternativet för att undvika oavsiktlig överskrivning av filer.
- Kontrollera alltid sökvägarna noggrant för att säkerställa att du kopierar till rätt plats.
- När du kopierar stora kataloger, överväg att använda `-v` för att få feedback om processen.