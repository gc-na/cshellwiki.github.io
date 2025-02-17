# [Linux] Bash docker-compose användning: Hantera multi-container Docker-applikationer

## Översikt
`docker-compose` är ett verktyg som används för att definiera och köra fler-container Docker-applikationer. Med hjälp av en YAML-fil kan du konfigurera tjänster, nätverk och volymer, vilket gör det enkelt att hantera komplexa applikationer med flera komponenter.

## Användning
Den grundläggande syntaxen för `docker-compose` är:

```bash
docker-compose [alternativ] [argument]
```

## Vanliga alternativ
- `up`: Startar och kör tjänster definierade i `docker-compose.yml`.
- `down`: Stoppar och tar bort tjänster, nätverk och volymer som skapats av `up`.
- `build`: Bygger bilder för tjänsterna.
- `logs`: Visar loggar för tjänsterna.
- `ps`: Visar status för tjänsterna.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `docker-compose`:

1. **Starta tjänster**:
   ```bash
   docker-compose up
   ```

2. **Starta tjänster i bakgrunden**:
   ```bash
   docker-compose up -d
   ```

3. **Stoppa och ta bort tjänster**:
   ```bash
   docker-compose down
   ```

4. **Bygga bilder**:
   ```bash
   docker-compose build
   ```

5. **Visa loggar**:
   ```bash
   docker-compose logs
   ```

## Tips
- Använd `-d` flaggan för att köra tjänster i bakgrunden, vilket frigör terminalen för andra kommandon.
- Kontrollera alltid din `docker-compose.yml` fil för korrekt syntax innan du kör kommandon.
- Använd `docker-compose ps` för att snabbt se statusen för dina tjänster och deras containrar.
- Tänk på att använda versionering i din `docker-compose.yml` för att säkerställa kompatibilitet med olika Docker-versioner.