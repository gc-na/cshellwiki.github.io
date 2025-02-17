# [Linux] Bash tput användning: Styra terminalens utseende

## Översikt
`tput` är ett kommandoradsverktyg som används för att styra terminalens utseende och beteende. Det gör det möjligt att ändra textfärg, bakgrundsfärg, cursorposition och andra terminalinställningar, vilket kan förbättra användarupplevelsen i skript och program.

## Användning
Den grundläggande syntaxen för `tput` är:

```bash
tput [alternativ] [argument]
```

## Vanliga alternativ
- `setaf [nummer]`: Ställer in textfärgen (0-7 för standardfärger).
- `setab [nummer]`: Ställer in bakgrundsfärgen (0-7 för standardfärger).
- `clear`: Rensar terminalskärmen.
- `cup [rad] [kolumn]`: Flyttar cursor till angiven rad och kolumn.
- `bold`: Aktiverar fetstil.
- `reset`: Återställer terminalinställningarna till standard.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `tput`:

### Ändra textfärg
För att ändra textfärgen till röd:

```bash
tput setaf 1
echo "Detta är röd text"
tput sgr0  # Återställ till standardfärg
```

### Ändra bakgrundsfärg
För att ställa in bakgrundsfärgen till blå:

```bash
tput setab 4
echo "Detta har en blå bakgrund"
tput sgr0  # Återställ till standardbakgrund
```

### Flytta cursor
För att flytta cursor till rad 5, kolumn 10:

```bash
tput cup 5 10
echo "Cursor flyttad hit"
```

### Rensa skärmen
För att rensa terminalskärmen:

```bash
tput clear
```

### Aktivera fetstil
För att aktivera fetstil:

```bash
tput bold
echo "Detta är fetstil"
tput sgr0  # Återställ till normal stil
```

## Tips
- Använd `tput sgr0` för att återställa terminalinställningarna efter att du har gjort ändringar, så att andra kommandon inte påverkas.
- Testa olika färgnummer för att se vilka färger som är tillgängliga på din terminal.
- Kombinera `tput` med andra kommandon i skript för att skapa mer interaktiva och visuellt tilltalande terminalapplikationer.