# [Linux] Bash dig brug: Hent DNS-oplysninger

## Oversigt
`dig` (Domain Information Groper) er et kommandolinjeværktøj, der bruges til at hente DNS-oplysninger om domæner. Det er nyttigt til fejlfinding af DNS-problemer og til at få detaljerede oplysninger om DNS-poster.

## Brug
Den grundlæggende syntaks for `dig`-kommandoen er:

```bash
dig [muligheder] [argumenter]
```

## Almindelige muligheder
- `@server`: Angiver en specifik DNS-server til forespørgslen.
- `-t type`: Angiver hvilken type DNS-post, der skal hentes (f.eks. A, MX, TXT).
- `+short`: Viser kun det mest relevante output i en kortere form.
- `+trace`: Følger DNS-forespørgslerne fra rodservere til den ønskede server.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `dig`:

### Hent A-post for et domæne
```bash
dig example.com A
```

### Hent MX-poster for et domæne
```bash
dig example.com MX
```

### Hent DNS-poster fra en specifik server
```bash
dig @8.8.8.8 example.com
```

### Hent en kort oversigt over A-posten
```bash
dig example.com A +short
```

### Følg DNS-forespørgslerne
```bash
dig example.com +trace
```

## Tips
- Brug `+short` for at få et mere overskueligt output, når du kun har brug for de grundlæggende oplysninger.
- Angiv en specifik DNS-server, hvis du vil teste, hvordan en anden server håndterer forespørgsler.
- `dig` kan være nyttigt til at kontrollere, om DNS-ændringer er blevet opdateret korrekt.