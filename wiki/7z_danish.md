# [Linux] Bash 7z brug: Komprimering og dekomprimering af filer

## Oversigt
7z er et kommandolinjeværktøj, der bruges til at komprimere og dekomprimere filer og mapper. Det understøtter flere komprimeringsformater, herunder 7z, ZIP, RAR og mere, hvilket gør det til et alsidigt værktøj til filhåndtering.

## Brug
Den grundlæggende syntaks for 7z-kommandoen er som følger:

```
7z [muligheder] [argumenter]
```

## Almindelige muligheder
- `a`: Tilføj filer til en arkiv.
- `x`: Udpak filer fra et arkiv.
- `l`: Vis indholdet af et arkiv.
- `d`: Slet filer fra et arkiv.
- `t`: Test integriteten af et arkiv.

## Almindelige eksempler
### Komprimere en mappe
For at komprimere en mappe kaldet `minmappe` til en 7z-fil, kan du bruge følgende kommando:

```bash
7z a minmappe.7z minmappe/
```

### Udpak en 7z-fil
For at udpakke en 7z-fil kaldet `minfil.7z`, kan du bruge:

```bash
7z x minfil.7z
```

### Liste indholdet af et arkiv
For at se indholdet af en 7z-fil, kan du køre:

```bash
7z l minfil.7z
```

### Slette filer fra et arkiv
For at slette en fil kaldet `fil.txt` fra et arkiv, kan du bruge:

```bash
7z d minfil.7z fil.txt
```

### Teste et arkivs integritet
For at teste integriteten af et arkiv, kan du bruge:

```bash
7z t minfil.7z
```

## Tips
- Sørg for at have den nyeste version af 7z installeret for at få adgang til de nyeste funktioner og forbedringer.
- Brug `-p` muligheden til at tilføje en adgangskode til dine arkiver for ekstra sikkerhed.
- Overvej at bruge `-m0=lzma2` for at opnå bedre komprimeringsforhold, når du opretter arkiver.