# [Linux] Bash printenv Användning: Visa miljövariabler

## Översikt
Kommandot `printenv` används för att visa miljövariabler i Bash. Det listar alla miljövariabler som är tillgängliga för den aktuella användarsessionen, vilket kan vara användbart för att felsöka eller förstå systemets konfiguration.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
printenv [alternativ] [argument]
```

## Vanliga alternativ
- `-0`, `--null`: Avskilj resultat med null-tecken istället för nya rader.
- `VARIABEL`: Om du anger namnet på en specifik variabel, kommer endast värdet för den variabeln att visas.

## Vanliga exempel
Visa alla miljövariabler:

```bash
printenv
```

Visa värdet av en specifik miljövariabel, till exempel `HOME`:

```bash
printenv HOME
```

Visa miljövariabler med null-tecken som avskiljare:

```bash
printenv -0
```

## Tips
- Använd `printenv` för att snabbt kontrollera miljöinställningar innan du kör skript eller program.
- Kombinera `printenv` med andra kommandon, som `grep`, för att filtrera specifika variabler. Till exempel:

```bash
printenv | grep PATH
```

- Tänk på att `printenv` endast visar miljövariabler och inte lokala variabler som kan vara definierade i din session.