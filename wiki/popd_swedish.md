# [Linux] Bash popd användning: Hantera katalogstackar

## Översikt
Kommandot `popd` används för att ta bort den översta katalogen från katalogstacken och byta till den nya översta katalogen. Det är ett användbart verktyg för att navigera mellan olika kataloger utan att behöva ange hela sökvägar.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
popd [alternativ] [argument]
```

## Vanliga alternativ
- `-n`: Gör ingen ändring av den aktuella katalogen, men tar bort katalogen från stacken.
- `+n`: Anger en specifik plats i stacken att poppa till, där `n` är indexet för katalogen i stacken (0 är den översta).

## Vanliga exempel
Här är några praktiska exempel på hur man använder `popd`:

1. **Poppa den översta katalogen**:
   ```bash
   popd
   ```
   Detta kommando tar bort den översta katalogen från stacken och byter till den nya översta katalogen.

2. **Poppa en specifik katalog från stacken**:
   ```bash
   popd +1
   ```
   Detta kommando tar bort katalogen som ligger på index 1 i stacken och byter till den katalogen.

3. **Poppa utan att byta katalog**:
   ```bash
   popd -n
   ```
   Detta kommando tar bort den översta katalogen från stacken men ändrar inte den aktuella katalogen.

## Tips
- Använd `pushd` för att lägga till kataloger i stacken innan du använder `popd`, så att du enkelt kan navigera tillbaka.
- Kontrollera din katalogstack med kommandot `dirs` för att se vilka kataloger som finns i stacken.
- Tänk på att indexeringen börjar från 0, så den översta katalogen är alltid index 0.