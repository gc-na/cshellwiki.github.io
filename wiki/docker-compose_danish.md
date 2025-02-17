# [Linux] Bash docker-compose brug: Administrer containeriserede applikationer

## Oversigt
`docker-compose` er et værktøj, der bruges til at definere og køre multi-container Docker-applikationer. Med en enkelt YAML-fil kan du konfigurere alle de tjenester, der er nødvendige for din applikation, og derefter starte dem med en enkelt kommando.

## Brug
Den grundlæggende syntaks for `docker-compose` er:

```bash
docker-compose [muligheder] [argumenter]
```

## Almindelige muligheder
- `up`: Starter de definerede tjenester.
- `down`: Stopper og fjerner de kørende tjenester.
- `build`: Bygger billederne til de tjenester, der er defineret i `docker-compose.yml`.
- `logs`: Viser logfilerne for de kørende tjenester.
- `ps`: Viser status for de kørende tjenester.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `docker-compose`:

1. **Starte tjenester**:
   ```bash
   docker-compose up
   ```

2. **Starte tjenester i baggrunden**:
   ```bash
   docker-compose up -d
   ```

3. **Stoppe og fjerne tjenester**:
   ```bash
   docker-compose down
   ```

4. **Bygge billeder**:
   ```bash
   docker-compose build
   ```

5. **Se logfiler**:
   ```bash
   docker-compose logs
   ```

6. **Tjekke status for tjenester**:
   ```bash
   docker-compose ps
   ```

## Tips
- Brug `-d` flaget for at køre tjenester i baggrunden, så du kan fortsætte med at bruge terminalen.
- Sørg for at have en korrekt konfigureret `docker-compose.yml` fil for at undgå fejl.
- Brug `docker-compose up --build` for at sikre, at billederne altid er opdaterede, når du starter dine tjenester.