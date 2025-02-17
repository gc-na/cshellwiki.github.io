# [Linux] Bash modprobe gebruik: Laad of verwijder kernelmodules

## Overzicht
De `modprobe` opdracht wordt gebruikt om kernelmodules te laden of te verwijderen in Linux-systemen. Het beheert automatisch afhankelijkheden tussen modules, waardoor het een handige tool is voor systeembeheerders en gebruikers die met hardware of specifieke functionaliteiten werken.

## Gebruik
De basis syntaxis van de `modprobe` opdracht is als volgt:

```bash
modprobe [opties] [argumenten]
```

## Veelvoorkomende opties
- `-r` : Verwijder een module.
- `--list` : Toon een lijst van beschikbare modules.
- `--show` : Toon informatie over een module zonder deze te laden.
- `--quiet` : Voorkom het tonen van waarschuwingen en meldingen.

## Veelvoorkomende voorbeelden

1. **Een module laden**
   Om de module `dummy` te laden, gebruik je de volgende opdracht:

   ```bash
   modprobe dummy
   ```

2. **Een module verwijderen**
   Om de module `dummy` te verwijderen, gebruik je:

   ```bash
   modprobe -r dummy
   ```

3. **Lijst van beschikbare modules**
   Om een lijst van beschikbare modules te bekijken, gebruik je:

   ```bash
   modprobe --list
   ```

4. **Informatie over een module tonen**
   Om informatie over de module `dummy` te tonen zonder deze te laden, gebruik je:

   ```bash
   modprobe --show dummy
   ```

## Tips
- Controleer altijd of de module al geladen is voordat je probeert deze opnieuw te laden om conflicten te voorkomen.
- Gebruik `modprobe -r` om afhankelijkheden automatisch te beheren bij het verwijderen van modules.
- Raadpleeg de documentatie van je specifieke distributie voor extra opties en informatie over modules die beschikbaar zijn voor jouw systeem.