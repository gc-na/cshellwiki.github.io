# [Linux] Bash cal <Uso equivalente em português>: Exibir um calendário

## Overview
O comando `cal` é utilizado para exibir um calendário no terminal. Ele pode mostrar o calendário do mês atual, de meses específicos ou até mesmo de anos inteiros, facilitando a visualização de datas.

## Usage
A sintaxe básica do comando `cal` é a seguinte:

```bash
cal [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o comando `cal`:

- `-m`: Exibe o calendário começando pela segunda-feira.
- `-y`: Mostra o calendário do ano atual.
- `-3`: Exibe o mês atual e os meses anterior e posterior.
- `-j`: Mostra os dias do ano (número do dia do ano).
- `-w`: Exibe o calendário com semanas começando na segunda-feira.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `cal`:

1. **Exibir o calendário do mês atual:**
   ```bash
   cal
   ```

2. **Exibir o calendário de um mês específico (por exemplo, março de 2023):**
   ```bash
   cal 03 2023
   ```

3. **Exibir o calendário do ano atual:**
   ```bash
   cal -y
   ```

4. **Exibir o calendário de três meses (mês atual, anterior e posterior):**
   ```bash
   cal -3
   ```

5. **Exibir o calendário de um ano específico (por exemplo, 2025):**
   ```bash
   cal 2025
   ```

## Tips
- Utilize a opção `-m` se preferir que a semana comece na segunda-feira, que é o padrão em muitos países.
- Combine opções para personalizar a visualização do calendário, como `cal -3 -m` para mostrar três meses começando pela segunda-feira.
- O comando `cal` é uma ferramenta leve e rápida, ideal para verificar datas sem sair do terminal.