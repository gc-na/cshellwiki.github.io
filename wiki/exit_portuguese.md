# [Linux] Bash exit uso: Finaliza um shell ou script

## Overview
O comando `exit` é utilizado para encerrar um shell ou script em Bash. Ele pode ser usado para sair de um terminal interativo ou para finalizar a execução de um script, retornando um código de saída que pode ser utilizado para indicar o sucesso ou falha da operação.

## Usage
A sintaxe básica do comando `exit` é a seguinte:

```bash
exit [opções] [código]
```

## Common Options
O comando `exit` não possui muitas opções, mas aqui estão algumas informações úteis:

- `código`: Um número inteiro que representa o código de saída. Por convenção, um código de saída `0` indica sucesso, enquanto qualquer número diferente de zero indica uma falha ou erro.

## Common Examples

### Exemplo 1: Sair de um terminal
Para sair de um terminal interativo, você pode simplesmente digitar:

```bash
exit
```

### Exemplo 2: Sair de um script com sucesso
Se você estiver em um script e quiser sair com um código de sucesso, use:

```bash
exit 0
```

### Exemplo 3: Sair de um script com erro
Para indicar que ocorreu um erro, você pode usar um código diferente de zero:

```bash
exit 1
```

### Exemplo 4: Sair de um script com um código específico
Você pode usar qualquer número inteiro como código de saída:

```bash
exit 42
```

## Tips
- Sempre utilize um código de saída apropriado em seus scripts para facilitar a depuração e o controle de fluxo.
- O código de saída pode ser verificado imediatamente após a execução de um comando usando `echo $?`, que retorna o último código de saída.
- Em scripts mais complexos, considere usar variáveis para armazenar códigos de saída e facilitar a manutenção do código.