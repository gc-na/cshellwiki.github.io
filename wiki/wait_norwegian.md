# [Linux] Bash wait bruk: Vent på prosesser

## Oversikt
`wait`-kommandoen i Bash brukes til å vente på at en eller flere bakgrunnsprosesser skal fullføre. Dette er nyttig når du ønsker å synkronisere skriptet ditt med prosesser som kjører parallelt.

## Bruk
Den grunnleggende syntaksen for `wait`-kommandoen er som følger:

```bash
wait [alternativer] [argumenter]
```

## Vanlige alternativer
- `PID`: Angi prosess-ID-en til prosessen du vil vente på. Hvis ingen PID er spesifisert, venter `wait` på alle bakgrunnsprosesser.
- `-n`: Vent på den første fullførte bakgrunnsprosessen.

## Vanlige eksempler

### Vente på en spesifikk prosess
For å vente på en spesifikk prosess med PID 1234:

```bash
wait 1234
```

### Vente på alle bakgrunnsprosesser
For å starte flere prosesser i bakgrunnen og vente på at de alle skal fullføre:

```bash
sleep 5 &
sleep 3 &
wait
echo "Alle prosesser er fullført."
```

### Vente på den første fullførte prosessen
For å vente på den første bakgrunnsprosessen som fullfører:

```bash
sleep 5 &
sleep 3 &
wait -n
echo "Den første prosessen er fullført."
```

## Tips
- Bruk `wait` i skript der du har flere bakgrunnsprosesser for å sikre at skriptet ikke avsluttes før alle prosessene er fullført.
- Vær oppmerksom på at `wait` returnerer statuskoden til den prosessen som fullførte. Du kan bruke denne koden for feilhåndtering i skriptene dine.
- Kombiner `wait` med `&` for å kjøre flere prosesser parallelt og deretter vente på at de skal fullføre.