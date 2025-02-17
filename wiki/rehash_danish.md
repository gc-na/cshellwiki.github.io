# [Linux] Bash rehash brug: Opdater kommander i shell

## Overview
`rehash`-kommandoen bruges i Bash til at opdatere shellens interne cache over tilgængelige kommandoer. Når du installerer nye programmer eller ændrer eksisterende, kan det være nødvendigt at køre `rehash` for at sikre, at shellen genkender de nye eller ændrede kommandoer.

## Usage
Den grundlæggende syntaks for `rehash`-kommandoen er:

```bash
rehash [options] [arguments]
```

## Common Options
`rehash` har ikke mange indstillinger, men her er nogle relevante:

- **-h, --help**: Viser hjælp til brugen af `rehash`.
- **-v, --version**: Viser versionsoplysninger om `rehash`.

## Common Examples

### Opdatering af kommandoer
For at opdatere shellens kommando-cache, kan du blot køre:

```bash
rehash
```

### Vise hjælp
Hvis du har brug for hjælp til `rehash`, kan du bruge:

```bash
rehash --help
```

### Tjekke version
For at se hvilken version af `rehash` du bruger, kan du køre:

```bash
rehash --version
```

## Tips
- Kør `rehash` efter installation af nye programmer for at sikre, at de bliver genkendt af shellen.
- Hvis du har ændret placeringen af et program, kan det også være en god idé at køre `rehash`.
- `rehash` er ikke altid nødvendigt, da mange moderne sheller automatisk opdaterer deres kommando-cache, men det kan være nyttigt i specifikke situationer.