# [Linux] Bash continue användning: Fortsätter en loop

## Översikt
`continue`-kommandot används i Bash-skript för att hoppa över den återstående delen av en loop och gå vidare till nästa iteration. Detta är användbart när du vill ignorera vissa villkor inom en loop utan att avsluta hela loopen.

## Användning
Den grundläggande syntaxen för `continue`-kommandot är:

```bash
continue [n]
```

Där `n` är ett valfritt argument som anger hur många nivåer av loopar som ska fortsätta. Om inget argument anges, fortsätter den den innersta loopen.

## Vanliga alternativ
- `n`: Anger hur många nivåer av loopar som ska fortsätta. Om `n` är 1, fortsätter den innersta loopen; om `n` är 2, fortsätter den näst innersta, och så vidare.

## Vanliga exempel

### Exempel 1: Enkel användning av continue
I detta exempel hoppar vi över udda tal i en for-loop.

```bash
for i in {1..10}; do
    if (( i % 2 != 0 )); then
        continue
    fi
    echo "$i"
done
```
Detta skript skriver ut jämna tal från 1 till 10.

### Exempel 2: Använda continue med en while-loop
Här hoppar vi över negativa tal i en while-loop.

```bash
count=0
while [ $count -lt 5 ]; do
    count=$((count - 1))
    if [ $count -lt 0 ]; then
        continue
    fi
    echo "$count"
done
```
Detta skript kommer inte att skriva ut negativa tal.

### Exempel 3: Fortsätta en specifik nivå av loopar
I detta exempel använder vi `continue` för att hoppa över en iteration i en nästlad loop.

```bash
for i in {1..3}; do
    for j in {1..3}; do
        if [ $j -eq 2 ]; then
            continue 2
        fi
        echo "i: $i, j: $j"
    done
done
```
Detta skript kommer att hoppa över alla iterationer där `j` är 2.

## Tips
- Använd `continue` för att förbättra läsbarheten i dina skript genom att undvika djupa nästlade if-satser.
- Tänk på att `continue` endast påverkar den aktuella loopen, så se till att du använder det på rätt nivå.
- Testa alltid dina skript noggrant för att säkerställa att `continue` används som avsett och inte oavsiktligt hoppar över viktiga delar av din kod.