# [Linux] C Shell (csh) docker gebruik: Beheer van containerapplicaties

## Overzicht
De `docker` opdracht is een krachtig hulpmiddel voor het beheren van containerapplicaties. Met Docker kunnen gebruikers applicaties in containers verpakken, verspreiden en uitvoeren, wat zorgt voor een consistente omgeving, ongeacht waar de applicatie draait.

## Gebruik
De basis syntaxis van de `docker` opdracht is als volgt:

```bash
docker [opties] [argumenten]
```

## Veelvoorkomende Opties
- `run`: Start een nieuwe container.
- `ps`: Lijst actieve containers.
- `images`: Toon beschikbare afbeeldingen.
- `pull`: Haal een afbeelding op van een externe repository.
- `build`: Bouw een afbeelding vanuit een Dockerfile.

## Veelvoorkomende Voorbeelden

1. **Een nieuwe container starten:**
   ```bash
   docker run hello-world
   ```

2. **Actieve containers weergeven:**
   ```bash
   docker ps
   ```

3. **Afbeeldingen ophalen:**
   ```bash
   docker pull ubuntu
   ```

4. **Een afbeelding bouwen vanuit een Dockerfile:**
   ```bash
   docker build -t mijn-app .
   ```

5. **Alle beschikbare afbeeldingen weergeven:**
   ```bash
   docker images
   ```

## Tips
- Gebruik `docker-compose` voor het beheren van multi-container applicaties.
- Houd je Docker-images schoon door ongebruikte afbeeldingen en containers regelmatig te verwijderen met `docker system prune`.
- Documenteer je Dockerfiles goed om de onderhoudbaarheid te verbeteren.