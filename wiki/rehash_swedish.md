# [Linux] Bash rehash användning: Uppdatera kommandon i skalet

## Översikt
Kommandot `rehash` används i Bash för att uppdatera den interna listan över kommandon som skalet känner till. Detta är särskilt användbart när nya program eller skript har lagts till i systemets sökvägar, så att du kan köra dem utan att behöva starta om terminalen.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
rehash [alternativ]
```

## Vanliga alternativ
`rehash` har inga specifika alternativ, men det kan användas i olika sammanhang där du behöver uppdatera kommandon.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `rehash`:

1. **Uppdatera kommandon efter installation av ett nytt program:**
   Om du har installerat ett nytt program och vill att Bash ska känna igen det, kan du helt enkelt köra:
   ```bash
   rehash
   ```

2. **Använda `rehash` efter att ha lagt till skript i din PATH:**
   Om du har lagt till en ny katalog i din PATH och vill att Bash ska känna till skripten där, kör:
   ```bash
   rehash
   ```

## Tips
- Använd `rehash` regelbundet efter installation av nya program för att säkerställa att du alltid kan köra dem utan problem.
- Om du har många skript eller program i din PATH, kan det vara bra att köra `rehash` efter att ha gjort ändringar för att undvika att få "kommando inte funnet"-fel.
- Kom ihåg att `rehash` är specifikt för vissa skal, så se till att du använder det i rätt sammanhang.