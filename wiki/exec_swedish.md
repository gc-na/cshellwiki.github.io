# [Linux] Bash exec användning: Utför ett kommando i den aktuella processen

## Översikt
`exec`-kommandot används för att ersätta den aktuella processen med ett nytt kommando. Detta innebär att det nya kommandot körs i samma process som den som anropade `exec`, vilket gör att den ursprungliga processen inte längre existerar efter att kommandot har körts.

## Användning
Den grundläggande syntaxen för `exec`-kommandot är:

```bash
exec [alternativ] [argument]
```

## Vanliga alternativ
- `-a` : Anger ett alternativt namn för det nya programmet.
- `-l` : Gör att det nya programmet körs som en inloggningsshell.
- `-p` : Bevarar miljövariabler och sökvägar.

## Vanliga exempel
Här är några praktiska exempel på hur `exec` kan användas:

### Ersätta en shell med ett nytt kommando
```bash
exec ls -l
```
Detta kommando kommer att ersätta den aktuella shell-processen med `ls -l`, vilket listar filerna i den aktuella katalogen.

### Använda exec för att köra ett skript
```bash
exec ./mitt_skript.sh
```
Detta kommer att köra `mitt_skript.sh` och ersätta den aktuella processen med skriptet.

### Använda exec med alternativt namn
```bash
exec -a nytt_namn /bin/bash
```
Detta kommando startar en ny bash-session men ger den ett alternativt namn, `nytt_namn`.

## Tips
- Använd `exec` när du vill spara resurser genom att undvika att skapa en ny process.
- Var försiktig med `exec`, eftersom det kommer att avsluta den nuvarande processen. Se till att du inte behöver återgå till den ursprungliga processen.
- Om du vill köra ett kommando men behålla den aktuella processen, överväg att använda `&` för att köra det i bakgrunden istället.