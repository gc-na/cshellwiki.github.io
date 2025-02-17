# [Linux] Bash export brug: Sætter miljøvariabler

## Oversigt
`export`-kommandoen i Bash bruges til at sætte miljøvariabler, så de kan tilgås af underordnede processer. Når en variabel eksporteres, bliver den tilgængelig for alle programmer, der køres fra den aktuelle shell-session.

## Brug
Den grundlæggende syntaks for `export`-kommandoen er som følger:

```bash
export [options] [arguments]
```

## Almindelige muligheder
- `-p`: Viser alle nuværende eksportede variabler.
- `VAR=value`: Opretter eller ændrer en variabel og eksporterer den.

## Almindelige eksempler

### Eksportere en ny variabel
For at oprette og eksportere en ny variabel, kan du bruge følgende kommando:

```bash
export MY_VAR="Hello, World!"
```

### Vise eksportede variabler
For at se alle de variabler, der er blevet eksporteret, kan du bruge:

```bash
export -p
```

### Ændre en eksisterende variabel
Hvis du vil ændre værdien af en eksisterende eksporteret variabel, kan du gøre det som følger:

```bash
export MY_VAR="New Value"
```

### Eksportere flere variabler
Du kan også eksportere flere variabler på én gang:

```bash
export VAR1="Value1" VAR2="Value2"
```

## Tips
- Husk, at eksportering af en variabel kun gælder for den aktuelle shell-session og dens underordnede processer. For at gøre ændringer permanente, skal du tilføje dem til din shell-konfigurationsfil (f.eks. `.bashrc`).
- Brug `unset`-kommandoen til at fjerne en eksporteret variabel, hvis den ikke længere er nødvendig:

```bash
unset MY_VAR
```
- Vær opmærksom på, at eksportering af variabler kan påvirke scripts og programmer, så det er en god idé at dokumentere ændringerne.