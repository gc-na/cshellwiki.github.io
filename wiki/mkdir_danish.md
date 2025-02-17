# [Linux] Bash mkdir brug: Opretter nye mapper

## Oversigt
`mkdir` (make directory) er en Bash-kommando, der bruges til at oprette nye mapper i filsystemet. Denne kommando er grundlæggende for organisering af filer og mapper i Linux-miljøer.

## Brug
Den grundlæggende syntaks for `mkdir`-kommandoen er som følger:

```bash
mkdir [muligheder] [argumenter]
```

## Almindelige muligheder
- `-p`: Opretter mappen og alle nødvendige overordnede mapper, hvis de ikke allerede findes.
- `-v`: Viser en meddelelse for hver oprettet mappe.
- `-m`: Angiver de tilladelser, der skal anvendes på den oprettede mappe.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `mkdir`:

1. Opret en enkelt mappe:
   ```bash
   mkdir minMappe
   ```

2. Opret flere mapper på én gang:
   ```bash
   mkdir mappe1 mappe2 mappe3
   ```

3. Opret en mappe og alle nødvendige overordnede mapper:
   ```bash
   mkdir -p /sti/til/ny/mappe
   ```

4. Opret en mappe og vis en meddelelse:
   ```bash
   mkdir -v nyMappe
   ```

5. Opret en mappe med specifikke tilladelser:
   ```bash
   mkdir -m 755 offentligMappe
   ```

## Tips
- Brug `-p`-muligheden, når du opretter en mappe i en dyb struktur for at undgå fejl, hvis de overordnede mapper ikke eksisterer.
- Tjek altid, om mappen allerede findes, for at undgå fejlmeddelelser.
- Overvej at bruge `-v` for at få feedback om, hvilke mapper der er blevet oprettet, især når du opretter flere mapper ad gangen.