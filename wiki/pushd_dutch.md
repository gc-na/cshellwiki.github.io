# [Linux] Bash pushd gebruik: Navigeer tussen directories

## Overview
De `pushd` opdracht in Bash wordt gebruikt om de huidige directory op de stack te plaatsen en vervolgens naar een andere directory te navigeren. Dit maakt het eenvoudig om tussen verschillende directories te schakelen zonder de huidige directory te verliezen.

## Usage
De basis syntaxis van de `pushd` opdracht is als volgt:

```bash
pushd [opties] [argumenten]
```

## Common Options
Hier zijn enkele veelvoorkomende opties voor `pushd`:

- `+n`: Navigeert naar de n-de directory in de stack.
- `-n`: Navigeert naar de vorige directory zonder deze aan de stack toe te voegen.
- `--help`: Toont hulpinformatie over het gebruik van de opdracht.

## Common Examples
Hier zijn enkele praktische voorbeelden van het gebruik van `pushd`:

1. **Navigeren naar een directory:**
   ```bash
   pushd /pad/naar/directory
   ```

2. **Navigeren naar een directory en de huidige directory op de stack plaatsen:**
   ```bash
   pushd ~/Documenten
   ```

3. **Teruggaan naar de vorige directory:**
   ```bash
   pushd -
   ```

4. **Navigeren naar de tweede directory in de stack:**
   ```bash
   pushd +1
   ```

## Tips
- Gebruik `popd` om de laatst toegevoegde directory van de stack te verwijderen en terug te keren naar de vorige directory.
- Combineer `pushd` met `dirs` om de huidige stack van directories te bekijken.
- Het gebruik van `pushd` en `popd` kan je workflow verbeteren door snel tussen directories te schakelen zonder je huidige locatie te vergeten.