# [Linux] Bash printf brug: Formateret output til terminalen

## Oversigt
`printf`-kommandoen i Bash bruges til at formatere og udskrive tekst til terminalen. Den giver mere kontrol over output sammenlignet med den enklere `echo`-kommando, hvilket gør den ideel til at vise data i et specifikt format.

## Brug
Den grundlæggende syntaks for `printf`-kommandoen er:

```bash
printf [options] [arguments]
```

## Almindelige muligheder
- `-v var`: Gem output i variablen `var` i stedet for at udskrive det.
- `--help`: Vis hjælp og information om brugen af `printf`.
- `--version`: Vis versionsinformation for `printf`.

## Almindelige eksempler

### Eksempel 1: Simpel tekstudskrivning
```bash
printf "Hej, verden!\n"
```
Dette vil udskrive "Hej, verden!" efterfulgt af et linjeskift.

### Eksempel 2: Formatering af tal
```bash
printf "Tal: %.2f\n" 3.14159
```
Dette vil udskrive "Tal: 3.14", hvor tallet er formateret til to decimaler.

### Eksempel 3: Udspecificering af flere argumenter
```bash
printf "Navn: %s, Alder: %d\n" "Alice" 30
```
Dette vil udskrive "Navn: Alice, Alder: 30", hvor `%s` bruges til strenge og `%d` til heltal.

### Eksempel 4: Udspecificering af bredde
```bash
printf "|%10s|%5d|\n" "Banan" 12
```
Dette vil udskrive "Banan" med en bredde på 10 tegn og tallet 12 med en bredde på 5 tegn, hvilket giver et pænt justeret output.

## Tips
- Brug `\n` for at tilføje linjeskift i din output.
- Vær opmærksom på format-specifikatorerne; de bestemmer, hvordan dataene vises.
- `printf` er mere pålidelig end `echo`, især når det kommer til specialtegn og formatering.