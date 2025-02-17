# [Linux] Bash rmmod gebruik: Verwijder een kernelmodule

## Overzicht
De `rmmod`-opdracht wordt gebruikt om een geladen kernelmodule uit de Linux-kernel te verwijderen. Dit kan nodig zijn om systeembronnen vrij te maken of om conflicten met andere modules te voorkomen.

## Gebruik
De basis syntaxis van de `rmmod`-opdracht is als volgt:

```bash
rmmod [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-f`: Forceert het verwijderen van de module, zelfs als deze in gebruik is.
- `-n`: Negeert de controle op de module en verwijdert deze zonder waarschuwing.
- `--all`: Verwijdert alle modules die kunnen worden verwijderd.

## Veelvoorkomende Voorbeelden

1. **Verwijder een specifieke module:**

   ```bash
   rmmod mijn_module
   ```

2. **Forceer het verwijderen van een module:**

   ```bash
   rmmod -f mijn_module
   ```

3. **Verwijder alle verwijderbare modules:**

   ```bash
   rmmod --all
   ```

4. **Verwijder een module met een specifieke optie:**

   ```bash
   rmmod -n mijn_module
   ```

## Tips
- Controleer altijd of de module in gebruik is voordat je deze probeert te verwijderen, om systeeminstabiliteit te voorkomen.
- Gebruik de `lsmod`-opdracht om een lijst van geladen modules te bekijken voordat je `rmmod` gebruikt.
- Wees voorzichtig met het gebruik van de `-f`-optie, omdat dit kan leiden tot onverwachte systeemgedragingen.