# [Linux] Bash docker brug: Administrer containere og billeder

## Oversigt
Docker er et værktøj, der bruges til at automatisere udrulningen af applikationer i containere. Det giver udviklere mulighed for at pakke deres applikationer og alle deres afhængigheder i en standardiseret enhed, hvilket gør det lettere at køre dem på tværs af forskellige miljøer.

## Brug
Den grundlæggende syntaks for docker-kommandoen er som følger:

```bash
docker [muligheder] [argumenter]
```

## Almindelige muligheder
- `run`: Kører en ny container.
- `ps`: Viser kørende containere.
- `images`: Viser alle tilgængelige billeder.
- `rm`: Fjerner en eller flere containere.
- `rmi`: Fjerner et eller flere billeder.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger docker-kommandoen:

1. **Køre en ny container**:
   ```bash
   docker run hello-world
   ```
   Dette eksempel downloader et simpelt "hello world"-billede og kører det i en container.

2. **Liste kørende containere**:
   ```bash
   docker ps
   ```
   Denne kommando viser alle de containere, der i øjeblikket kører på systemet.

3. **Liste alle billeder**:
   ```bash
   docker images
   ```
   Her vises en liste over alle de billeder, der er tilgængelige på din maskine.

4. **Fjerne en container**:
   ```bash
   docker rm [container_id]
   ```
   Erstat `[container_id]` med ID'en på den container, du ønsker at fjerne.

5. **Fjerne et billede**:
   ```bash
   docker rmi [image_id]
   ```
   Erstat `[image_id]` med ID'en på det billede, du ønsker at fjerne.

## Tips
- Sørg for at holde dine billeder opdaterede for at undgå sikkerhedsproblemer.
- Brug `docker-compose` til at håndtere flere containere og deres indbyrdes afhængigheder.
- Test altid dine containere i et sikkert miljø, inden du implementerer dem i produktion.