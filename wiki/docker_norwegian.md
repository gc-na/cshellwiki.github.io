# [Linux] Bash docker bruk: Administrere containere og bilder

## Oversikt
Docker er et verktøy som brukes til å automatisere distribusjonen av programvare i containere. Containere er lette, bærbare og selvforsynte enheter som kan kjøre programvare i isolerte miljøer. Docker gjør det enkelt å bygge, kjøre og administrere disse containerne.

## Bruk
Den grunnleggende syntaksen for docker-kommandoen er:

```bash
docker [alternativer] [argumenter]
```

## Vanlige alternativer
- `run`: Kjør en ny container.
- `ps`: Vis kjørende containere.
- `images`: Vis tilgjengelige bilder.
- `rm`: Fjern en eller flere containere.
- `rmi`: Fjern ett eller flere bilder.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke docker:

### Kjør en ny container
For å kjøre en ny container fra et bilde, kan du bruke:

```bash
docker run ubuntu
```

### Vis kjørende containere
For å se en liste over alle kjørende containere, kan du bruke:

```bash
docker ps
```

### Vis tilgjengelige bilder
For å se hvilke bilder som er tilgjengelige på systemet ditt, kan du bruke:

```bash
docker images
```

### Fjern en container
For å fjerne en spesifikk container, kan du bruke:

```bash
docker rm <container_id>
```

### Fjern et bilde
For å fjerne et spesifikt bilde, kan du bruke:

```bash
docker rmi <image_id>
```

## Tips
- Bruk `docker-compose` for å håndtere flere containere som en enkelt applikasjon.
- Hold bildene dine oppdatert for å unngå sikkerhetsproblemer.
- Bruk `docker logs <container_id>` for å se loggene til en container, noe som kan være nyttig for feilsøking.