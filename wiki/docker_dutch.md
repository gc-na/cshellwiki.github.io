# [Linux] Bash docker gebruik: Beheer van containerapplicaties

## Overzicht
De `docker` opdracht is een krachtige tool voor het beheren van containerapplicaties. Met Docker kunnen ontwikkelaars en systeembeheerders applicaties in containers verpakken, verspreiden en uitvoeren. Dit maakt het eenvoudig om software te isoleren en te schalen.

## Gebruik
De basis syntaxis van de `docker` opdracht is als volgt:

```bash
docker [opties] [argumenten]
```

## Veelvoorkomende Opties
- `run`: Start een nieuwe container.
- `ps`: Toont actieve containers.
- `stop`: Stopt een draaiende container.
- `rm`: Verwijdert een container.
- `images`: Lijst beschikbare afbeeldingen.
- `pull`: Haalt een afbeelding op van een register.

## Veelvoorkomende Voorbeelden

1. **Een nieuwe container starten:**
   ```bash
   docker run hello-world
   ```

2. **Lijst van actieve containers weergeven:**
   ```bash
   docker ps
   ```

3. **Een specifieke container stoppen:**
   ```bash
   docker stop <container_id>
   ```

4. **Een container verwijderen:**
   ```bash
   docker rm <container_id>
   ```

5. **Afbeeldingen ophalen van Docker Hub:**
   ```bash
   docker pull ubuntu
   ```

## Tips
- Zorg ervoor dat je regelmatig je afbeeldingen en containers opruimt om schijfruimte te besparen.
- Gebruik `docker-compose` voor het beheren van multi-container applicaties.
- Controleer altijd de documentatie van specifieke afbeeldingen voor extra configuratie-instellingen en opties.