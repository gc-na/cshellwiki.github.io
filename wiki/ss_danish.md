# [Linux] Bash ss brug: Visning af netværksforbindelser

## Oversigt
`ss` er et værktøj til at vise socket-statistikker og netværksforbindelser på Linux-systemer. Det kan bruges til at overvåge og diagnosticere netværksproblemer ved at give detaljerede oplysninger om aktive forbindelser, lytte sockets og meget mere.

## Brug
Den grundlæggende syntaks for `ss`-kommandoen er som følger:

```bash
ss [muligheder] [argumenter]
```

## Almindelige muligheder
- `-t`: Vis kun TCP-forbindelser.
- `-u`: Vis kun UDP-forbindelser.
- `-l`: Vis kun lytte sockets.
- `-p`: Vis processer, der ejer sockets.
- `-n`: Vis numeriske adresser i stedet for at forsøge at opløse dem til navne.

## Almindelige eksempler

1. **Vis alle aktive forbindelser:**
   ```bash
   ss
   ```

2. **Vis kun TCP-forbindelser:**
   ```bash
   ss -t
   ```

3. **Vis lytte sockets:**
   ```bash
   ss -l
   ```

4. **Vis UDP-forbindelser:**
   ```bash
   ss -u
   ```

5. **Vis detaljer om processer, der ejer sockets:**
   ```bash
   ss -p
   ```

6. **Vis alle forbindelser med numeriske adresser:**
   ```bash
   ss -n
   ```

## Tips
- Brug `ss -t -l` for hurtigt at finde ud af, hvilke TCP-porte der er åbne og lytter.
- Kombiner mulighederne for at få mere specifik information, f.eks. `ss -tunlp` for at se både TCP og UDP med procesinformation.
- `ss` er generelt hurtigere og mere effektivt end det ældre `netstat`-værktøj, så det anbefales at bruge `ss` til netværksdiagnose.