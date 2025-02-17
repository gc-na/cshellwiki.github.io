# [Linux] Bash ln brug: Opretter links mellem filer

## Oversigt
`ln`-kommandoen bruges til at oprette links mellem filer i Unix-lignende operativsystemer. Der findes to typer links: hårde links og bløde links (symboliske links). Hårde links refererer direkte til filens inode, mens bløde links peger på filens sti.

## Brug
Den grundlæggende syntaks for `ln`-kommandoen er som følger:

```
ln [muligheder] [argumenter]
```

## Almindelige muligheder
- `-s`: Opretter et symbolsk link i stedet for et hårdt link.
- `-f`: Tvinger oprettelsen af linket, hvis destinationen allerede findes.
- `-n`: Behandler eksisterende destinationer som almindelige filer, ikke som links.
- `-v`: Viser detaljerede oplysninger om, hvad der sker under oprettelsen af linket.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `ln`-kommandoen kan bruges:

### Opret et hårdt link
```bash
ln fil.txt link_til_fil.txt
```
Dette opretter et hårdt link til `fil.txt` med navnet `link_til_fil.txt`.

### Opret et symbolsk link
```bash
ln -s fil.txt link_til_fil.txt
```
Dette opretter et symbolsk link til `fil.txt`, hvilket gør det muligt at referere til filen via `link_til_fil.txt`.

### Tving oprettelse af et link
```bash
ln -f fil.txt link_til_fil.txt
```
Hvis `link_til_fil.txt` allerede eksisterer, vil denne kommando overskrive det eksisterende link.

### Opret et symbolsk link til en mappe
```bash
ln -s /sti/til/mappe link_til_mappe
```
Dette opretter et symbolsk link til en mappe, hvilket gør det lettere at navigere til den.

## Tips
- Brug symboliske links til at oprette genveje til filer eller mapper, der kan ændre sig i sti, da de er mere fleksible end hårde links.
- Vær opmærksom på, at hårde links ikke kan oprettes til mapper, og de kan ikke krydse filsystemgrænser.
- Kontroller altid, om destinationen allerede findes, især når du bruger `-f`-muligheden, for at undgå utilsigtet at overskrive filer.