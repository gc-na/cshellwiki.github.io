# [Linux] Bash umask användning: Ställer in standardbehörigheter för nya filer och kataloger

## Översikt
`umask`-kommandot används för att ställa in standardbehörigheter för nya filer och kataloger som skapas i ett Unix-liknande operativsystem. Det definierar vilka behörigheter som ska tas bort från de standardbehörigheter som tilldelas av systemet.

## Användning
Den grundläggande syntaxen för `umask`-kommandot är:

```bash
umask [alternativ] [argument]
```

## Vanliga alternativ
- `-S`: Visar umask-värdet i symbolisk form.
- `-p`: Visar det aktuella umask-värdet för den aktuella sessionen.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `umask`:

1. **Visa det aktuella umask-värdet:**
   ```bash
   umask
   ```

2. **Ställa in umask-värdet till 022:**
   ```bash
   umask 022
   ```

3. **Ställa in umask-värdet med symbolisk notation:**
   ```bash
   umask u=rwx,g=rx,o=rx
   ```

4. **Visa umask-värdet i symbolisk form:**
   ```bash
   umask -S
   ```

5. **Ställa in umask-värdet till 007:**
   ```bash
   umask 007
   ```

## Tips
- Tänk på att umask-värdet påverkar endast nya filer och kataloger, inte befintliga.
- Kontrollera alltid ditt umask-värde innan du skapar nya filer för att säkerställa att de får rätt behörigheter.
- Om du arbetar i en delad miljö, var försiktig med att ändra umask-värdet, eftersom det kan påverka andra användare.