# [Linux] Bash lsmod gebruik: Toont geladen kernelmodules

## Overzicht
De `lsmod`-opdracht in Linux toont een lijst van momenteel geladen kernelmodules. Dit is nuttig voor systeembeheerders en gebruikers die willen controleren welke modules actief zijn en hun afhankelijkheden.

## Gebruik
De basis syntaxis van de `lsmod`-opdracht is als volgt:

```bash
lsmod [opties] [argumenten]
```

## Veelvoorkomende opties
- **-h, --help**: Toont een helpbericht met informatie over het gebruik van de opdracht.
- **-v, --verbose**: Geeft meer gedetailleerde informatie over de geladen modules.

## Veelvoorkomende voorbeelden

1. **Toon alle geladen modules**:
   ```bash
   lsmod
   ```

2. **Toon geladen modules met gedetailleerde informatie**:
   ```bash
   lsmod -v
   ```

3. **Gebruik met grep om een specifieke module te vinden**:
   ```bash
   lsmod | grep <module_naam>
   ```

4. **Toon alleen de modules met hun afhankelijkheden**:
   ```bash
   lsmod | awk '{print $1, $3}'
   ```

## Tips
- Gebruik `lsmod` in combinatie met andere opdrachten zoals `modinfo` om meer informatie over specifieke modules te krijgen.
- Controleer regelmatig de geladen modules om te zorgen dat er geen ongewenste of verouderde modules actief zijn.
- Vergeet niet dat wijzigingen aan modules invloed kunnen hebben op de stabiliteit van je systeem, dus wees voorzichtig bij het laden of verwijderen van modules.