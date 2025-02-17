# [Linux] Bash strace användning: Spåra systemanrop och signaler

## Översikt
`strace` är ett kraftfullt verktyg i Linux som används för att spåra systemanrop och signaler som görs av ett program. Det är särskilt användbart för felsökning och analys av programbeteende, eftersom det ger insikt i hur programmet interagerar med operativsystemet.

## Användning
Den grundläggande syntaxen för `strace` är:

```bash
strace [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Sammanställ statistik över systemanrop.
- `-e`: Filtrera systemanrop som ska spåras (t.ex. `-e trace=open` för att endast spåra öppningsanrop).
- `-o filnamn`: Skriv ut strace-resultatet till en fil istället för till standardutgången.
- `-p PID`: Spåra ett redan körande program med det angivna process-ID:t.
- `-f`: Följ barnprocesser som skapas av programmet.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `strace`:

1. Spåra ett program och visa systemanrop i realtid:
   ```bash
   strace ls
   ```

2. Spara strace-utdata till en fil:
   ```bash
   strace -o output.txt ls
   ```

3. Spåra endast öppningsanrop:
   ```bash
   strace -e trace=open ls
   ```

4. Spåra ett redan körande program:
   ```bash
   strace -p 1234
   ```

5. Sammanställ statistik över systemanrop:
   ```bash
   strace -c ls
   ```

## Tips
- Använd `-f` om programmet skapar barnprocesser som du också vill spåra.
- Tänk på att `strace` kan påverka prestandan hos programmet som spåras, så använd det med försiktighet i produktionsmiljöer.
- För djupare analys, kombinera `strace` med andra verktyg som `grep` för att filtrera specifika systemanrop.