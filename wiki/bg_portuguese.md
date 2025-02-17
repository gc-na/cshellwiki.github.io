# [Linux] Bash bg Uso equivalente: Colocar processos em segundo plano

## Overview
O comando `bg` é utilizado no Bash para retomar a execução de um processo que foi interrompido, colocando-o em segundo plano. Isso permite que o usuário continue utilizando o terminal enquanto o processo ainda está em execução.

## Usage
A sintaxe básica do comando `bg` é a seguinte:

```bash
bg [opções] [jobspec]
```

## Common Options
- `jobspec`: Especifica o trabalho que você deseja colocar em segundo plano. Pode ser o número do trabalho ou o nome do processo.
- `-n`: Não notifica o usuário quando o trabalho é colocado em segundo plano.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `bg`:

1. **Colocar o último trabalho interrompido em segundo plano:**
   ```bash
   bg
   ```

2. **Colocar um trabalho específico em segundo plano:**
   Primeiro, você pode interromper um trabalho usando `Ctrl + Z`, e depois usar:
   ```bash
   bg %1
   ```
   Aqui, `%1` refere-se ao primeiro trabalho na lista de trabalhos.

3. **Colocar um trabalho em segundo plano sem notificações:**
   ```bash
   bg -n %2
   ```

## Tips
- Sempre verifique a lista de trabalhos em execução com o comando `jobs` antes de usar `bg`, para saber quais processos estão disponíveis para serem colocados em segundo plano.
- Utilize `fg` para trazer um trabalho de volta para o primeiro plano, caso você precise interagir com ele novamente.
- Lembre-se de que processos em segundo plano podem continuar a gerar saída no terminal, então é uma boa prática redirecionar a saída se necessário.