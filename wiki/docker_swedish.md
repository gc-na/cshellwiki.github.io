# [Linux] Bash docker användning: Hantera containrar och bilder

## Översikt
Docker är en plattform som används för att automatisera distributionen av applikationer i containrar. En container är en lättvikts, fristående och körbar programvarupaket som innehåller allt som behövs för att köra en programvara, inklusive kod, körbibliotek, systemverktyg och inställningar.

## Användning
Den grundläggande syntaxen för docker-kommandot är:

```
docker [alternativ] [argument]
```

## Vanliga alternativ
- `run`: Skapar och kör en container.
- `ps`: Visar aktiva containrar.
- `images`: Visar tillgängliga bilder.
- `pull`: Hämtar en bild från ett register.
- `build`: Bygger en bild från en Dockerfile.

## Vanliga exempel
Här är några praktiska exempel på hur man använder docker-kommandot:

1. **Köra en enkel container**:
   ```bash
   docker run hello-world
   ```

2. **Lista aktiva containrar**:
   ```bash
   docker ps
   ```

3. **Hämta en bild från Docker Hub**:
   ```bash
   docker pull ubuntu
   ```

4. **Bygga en bild från en Dockerfile**:
   ```bash
   docker build -t my-image .
   ```

5. **Lista alla tillgängliga bilder**:
   ```bash
   docker images
   ```

## Tips
- Använd `docker-compose` för att hantera flera containrar som en enhet.
- Håll dina bilder små genom att använda lätta basbilder.
- Rensa upp oanvända bilder och containrar med `docker system prune` för att spara diskutrymme.