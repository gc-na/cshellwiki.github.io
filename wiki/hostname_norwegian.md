# [Linux] Bash hostname bruk: Hente og sette vertsnavn

## Oversikt
`hostname`-kommandoen brukes til å vise eller sette vertsnavnet til systemet. Vertsnavnet er det navnet som identifiserer en datamaskin i et nettverk.

## Bruk
Den grunnleggende syntaksen for `hostname`-kommandoen er:

```
hostname [alternativer] [argumenter]
```

## Vanlige alternativer
- `-s`: Viser bare vertsnavnet (kort form).
- `-f`: Viser det fullstendige vertsnavnet (inkludert domenenavn).
- `-i`: Viser IP-adressen til vertsnavnet.
- `-A`: Viser alle aliaser for vertsnavnet.

## Vanlige eksempler
For å vise det nåværende vertsnavnet:

```bash
hostname
```

For å vise det korte vertsnavnet:

```bash
hostname -s
```

For å vise det fullstendige vertsnavnet:

```bash
hostname -f
```

For å vise IP-adressen til vertsnavnet:

```bash
hostname -i
```

For å sette et nytt vertsnavn:

```bash
sudo hostname nytt-vertsnavn
```

## Tips
- Husk at endring av vertsnavn kan kreve en omstart av systemet for å tre i kraft fullt ut.
- Bruk `hostnamectl` for mer avanserte funksjoner og for å sette vertsnavn på systemer som bruker systemd.
- Kontroller alltid at det nye vertsnavnet er unikt i nettverket for å unngå konflikter.