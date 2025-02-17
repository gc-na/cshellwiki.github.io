# [Linux] Bash tcpdump brug: Fange netværkstrafik

## Oversigt
tcpdump er et kommandolinjeværktøj, der bruges til at fange og analysere netværkstrafik, der passerer gennem en netværksgrænseflade. Det er et kraftfuldt værktøj til fejlfinding og overvågning af netværk.

## Brug
Den grundlæggende syntaks for tcpdump er som følger:

```bash
tcpdump [options] [arguments]
```

## Almindelige muligheder
- `-i <interface>`: Angiver den netværksgrænseflade, der skal overvåges.
- `-n`: Deaktiverer navneopslag af værter og porte, hvilket gør output hurtigere.
- `-c <antal>`: Angiver, hvor mange pakker der skal fanges, før tcpdump stopper.
- `-w <fil>`: Skriver de fangede pakker til en fil i stedet for at vise dem på skærmen.
- `-r <fil>`: Læser pakker fra en tidligere gemt fil.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan tcpdump kan bruges:

1. Fange trafik på en specifik netværksgrænseflade:
   ```bash
   tcpdump -i eth0
   ```

2. Fange et bestemt antal pakker:
   ```bash
   tcpdump -i eth0 -c 10
   ```

3. Fange trafik og gemme den i en fil:
   ```bash
   tcpdump -i eth0 -w trafik.pcap
   ```

4. Læse pakker fra en gemt fil:
   ```bash
   tcpdump -r trafik.pcap
   ```

5. Fange trafik fra en bestemt IP-adresse:
   ```bash
   tcpdump -i eth0 host 192.168.1.1
   ```

## Tips
- Brug `-n` for at forbedre hastigheden, især på travle netværk.
- Kombiner `-w` og `-r` for at analysere trafik senere.
- Vær opmærksom på, at tcpdump kræver root-rettigheder for at fange pakker på de fleste systemer.
- Overvej at bruge filtre for at begrænse den trafik, der fanges, hvilket kan gøre analysen lettere.