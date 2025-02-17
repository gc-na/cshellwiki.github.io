# [Linux] Bash readonly användning: Skapa oföränderliga variabler

## Översikt
`readonly` är ett Bash-kommando som används för att deklarera variabler som oföränderliga. När en variabel har markerats som readonly kan dess värde inte ändras under den aktuella sessionen, vilket hjälper till att förhindra oavsiktliga ändringar.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
readonly [options] [arguments]
```

## Vanliga alternativ
- `-p`: Visar en lista över alla readonly variabler i den aktuella sessionen.

## Vanliga exempel

### Exempel 1: Skapa en readonly variabel
```bash
readonly MY_VAR="Hej världen"
```
I detta exempel skapas en variabel `MY_VAR` med värdet "Hej världen". Den kan inte ändras senare.

### Exempel 2: Försök att ändra en readonly variabel
```bash
readonly MY_VAR="Hej världen"
MY_VAR="Ny värde"  # Detta kommer att ge ett felmeddelande
```
Detta försök att ändra `MY_VAR` kommer att resultera i ett fel, eftersom variabeln är readonly.

### Exempel 3: Visa alla readonly variabler
```bash
readonly -p
```
Detta kommando listar alla variabler som har markerats som readonly i den aktuella sessionen.

## Tips
- Använd `readonly` för att skydda viktiga variabler från oavsiktliga ändringar, särskilt i skript.
- Kom ihåg att readonly variabler endast är oföränderliga under den aktuella sessionen; de kan återställas om sessionen startas om.
- Det är en bra praxis att namnge readonly variabler med stora bokstäver för att särskilja dem från vanliga variabler.