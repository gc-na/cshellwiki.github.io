# [Linux] Bash foreach brug: Udfør kommandoer på hver post i en liste

## Oversigt
`foreach`-kommandoen bruges til at udføre en specifik kommando for hver post i en liste. Det er en praktisk måde at automatisere gentagne opgaver på, især når man arbejder med mange filer eller data.

## Brug
Den grundlæggende syntaks for `foreach`-kommandoen er som følger:

```bash
foreach [options] [arguments]
```

## Almindelige muligheder
- `-n`: Udfør kommandoen uden at vise output.
- `-p`: Spørg brugeren om bekræftelse, før hver kommando udføres.
- `-v`: Vis de kommandoer, der bliver udført.

## Almindelige eksempler

### Eksempel 1: Udfør en kommando på en liste af filer
```bash
foreach file (*.txt) {
    echo "Behandler $file"
}
```
I dette eksempel vil `foreach`-kommandoen iterere over alle `.txt`-filer i den aktuelle mappe og udskrive en besked for hver fil.

### Eksempel 2: Sletning af midlertidige filer
```bash
foreach file (*.tmp) {
    rm $file
}
```
Her vil `foreach`-kommandoen slette alle midlertidige filer i den aktuelle mappe.

### Eksempel 3: Komprimering af billeder
```bash
foreach img (*.jpg) {
    convert $img -quality 80 compressed/$img
}
```
I dette eksempel komprimeres alle `.jpg`-billeder og gemmes i en undermappe kaldet `compressed`.

## Tips
- Sørg for at teste dine kommandoer med en lille liste, inden du anvender dem på mange filer for at undgå utilsigtede ændringer.
- Brug `-n`-muligheden, hvis du vil køre kommandoer uden at se output, hvilket kan være nyttigt i scripts.
- Overvej at bruge `-p` for at få bekræftelse, når du udfører destruktive handlinger som sletning.