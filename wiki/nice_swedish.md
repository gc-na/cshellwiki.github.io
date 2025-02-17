# [Linux] Bash nice användning: Justera processprioritet

## Översikt
Kommandot `nice` används för att starta ett program med en specifik prioritet. Genom att justera prioriteten kan användaren styra hur mycket CPU-resurser ett program får i förhållande till andra processer som körs på systemet.

## Användning
Den grundläggande syntaxen för kommandot `nice` är:

```bash
nice [alternativ] [kommando]
```

## Vanliga alternativ
- `-n, --adjustment`: Anger justeringen av prioriteten. Värdet kan vara mellan -20 (högsta prioritet) och 19 (lägsta prioritet). Standardvärdet är 10.
- `--help`: Visar hjälpmeddelande med information om kommandot.
- `--version`: Visar versionsinformation för `nice`.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `nice`:

1. Starta ett program med standardprioritet:
    ```bash
    nice my_program
    ```

2. Starta ett program med högre prioritet (lägre värde):
    ```bash
    nice -n -5 my_program
    ```

3. Starta ett program med lägre prioritet (högre värde):
    ```bash
    nice -n 15 my_program
    ```

4. Kontrollera prioriteten för en redan körande process:
    ```bash
    ps -o pid,ni,cmd | grep my_program
    ```

## Tips
- Använd `nice` för att undvika att ett program tar över systemresurser, vilket kan påverka andra användares upplevelse.
- Kom ihåg att endast användare med tillräckliga rättigheter kan sänka prioriteten för processer (dvs. ge dem högre prioritet).
- Använd `renice` för att ändra prioriteten för en redan körande process.