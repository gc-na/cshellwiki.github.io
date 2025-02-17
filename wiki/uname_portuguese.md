# [Linux] Bash uname Uso: Exibir informações do sistema

## Overview
O comando `uname` é utilizado para exibir informações sobre o sistema operacional em que você está trabalhando. Ele pode fornecer detalhes como o nome do kernel, a versão e o tipo de máquina.

## Usage
A sintaxe básica do comando `uname` é a seguinte:

```bash
uname [opções]
```

## Common Options
Aqui estão algumas opções comuns do comando `uname`:

- `-a`: Exibe todas as informações disponíveis sobre o sistema.
- `-s`: Mostra o nome do kernel.
- `-n`: Exibe o nome do host da máquina.
- `-r`: Mostra a versão do kernel.
- `-v`: Exibe a data e hora da versão do kernel.
- `-m`: Mostra o tipo de máquina (arquitetura).
- `-p`: Exibe o tipo de processador.
- `-i`: Mostra a plataforma do hardware.
- `-o`: Exibe o sistema operacional.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `uname`:

1. **Exibir todas as informações do sistema:**
   ```bash
   uname -a
   ```

2. **Mostrar apenas o nome do kernel:**
   ```bash
   uname -s
   ```

3. **Ver a versão do kernel:**
   ```bash
   uname -r
   ```

4. **Exibir o nome do host da máquina:**
   ```bash
   uname -n
   ```

5. **Mostrar o tipo de máquina:**
   ```bash
   uname -m
   ```

## Tips
- Utilize `uname -a` para obter uma visão geral completa do sistema em uma única linha.
- Combine `uname` com outros comandos, como `grep`, para filtrar informações específicas.
- Lembre-se de que algumas opções podem não estar disponíveis em todos os sistemas, então verifique a documentação do seu sistema operacional se necessário.