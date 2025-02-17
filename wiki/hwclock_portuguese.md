# [Linux] Bash hwclock uso: Sincroniza o relógio do sistema com o relógio de hardware

## Overview
O comando `hwclock` é utilizado para acessar e manipular o relógio de hardware do sistema. Ele permite que os usuários leiam e ajustem o tempo do relógio de hardware, que é independente do sistema operacional e continua funcionando mesmo quando o computador está desligado.

## Usage
A sintaxe básica do comando `hwclock` é a seguinte:

```bash
hwclock [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `hwclock`:

- `--hctosys`: Sincroniza o relógio do sistema com o relógio de hardware.
- `--systohc`: Sincroniza o relógio de hardware com o relógio do sistema.
- `--show`: Exibe a hora atual do relógio de hardware.
- `--set`: Define a hora do relógio de hardware.
- `--utc`: Indica que o relógio de hardware está configurado para o tempo UTC.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `hwclock`:

1. **Sincronizar o relógio do sistema com o relógio de hardware:**
   ```bash
   hwclock --hctosys
   ```

2. **Sincronizar o relógio de hardware com o relógio do sistema:**
   ```bash
   hwclock --systohc
   ```

3. **Exibir a hora atual do relógio de hardware:**
   ```bash
   hwclock --show
   ```

4. **Definir uma nova hora para o relógio de hardware:**
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

5. **Definir o relógio de hardware para UTC:**
   ```bash
   hwclock --systohc --utc
   ```

## Tips
- Sempre verifique a hora do relógio de hardware após fazer ajustes, usando `hwclock --show`.
- É uma boa prática sincronizar o relógio de hardware com o relógio do sistema após instalar ou atualizar o sistema operacional.
- Se você estiver em um ambiente de múltiplos fusos horários, considere usar a opção `--utc` para evitar confusões com o horário local.