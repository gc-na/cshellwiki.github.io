# [Linux] Bash curl brug: Hent data fra internettet

## Oversigt
`curl` er et kommandolinjeværktøj, der bruges til at overføre data til eller fra en server ved hjælp af forskellige protokoller, herunder HTTP, HTTPS, FTP og mange flere. Det er et kraftfuldt værktøj til at hente indhold fra internettet eller sende data til en server.

## Brug
Den grundlæggende syntaks for `curl`-kommandoen er som følger:

```bash
curl [muligheder] [argumenter]
```

## Almindelige muligheder
- `-X`: Angiv HTTP-metoden (f.eks. GET, POST).
- `-d`: Send data i en POST-anmodning.
- `-H`: Angiv en brugerdefineret header.
- `-o`: Gem output til en fil.
- `-I`: Hent kun HTTP-headerne.
- `-L`: Følg omdirigeringer.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `curl`:

### Hent en webside
```bash
curl https://www.example.com
```

### Gem output til en fil
```bash
curl -o filnavn.html https://www.example.com
```

### Send en POST-anmodning med data
```bash
curl -X POST -d "navn=John&alder=30" https://www.example.com/api
```

### Hent kun HTTP-headerne
```bash
curl -I https://www.example.com
```

### Følg omdirigeringer
```bash
curl -L https://www.example.com
```

## Tips
- Brug `-v` (verbose) for at se detaljer om anmodningen og svaret, hvilket kan være nyttigt til fejlfinding.
- Hvis du arbejder med API'er, kan det være nyttigt at gemme dine anmodninger i et script for at automatisere processen.
- Vær opmærksom på, at nogle servere kan kræve autentificering; brug `-u` til at angive brugernavn og adgangskode.