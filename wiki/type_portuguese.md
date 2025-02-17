# [Linux] Bash tipo equivalente de uso: [verifica o tipo de comando]

## Overview
O comando `type` no Bash é utilizado para identificar o tipo de um comando específico. Ele informa se o comando é um alias, uma função, um built-in do shell ou um executável localizado em um diretório do sistema.

## Usage
A sintaxe básica do comando `type` é a seguinte:

```bash
type [opções] [argumentos]
```

## Common Options
- `-t`: Exibe apenas o tipo do comando, sem informações adicionais.
- `-a`: Mostra todas as localizações do comando, incluindo aliases e funções.
- `-p`: Exibe o caminho completo do executável se o comando for um executável.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `type`:

1. **Verificar o tipo de um comando**:
   ```bash
   type ls
   ```

2. **Verificar o tipo de um alias**:
   ```bash
   alias ll='ls -la'
   type ll
   ```

3. **Mostrar todas as localizações de um comando**:
   ```bash
   type -a echo
   ```

4. **Exibir apenas o tipo de um comando**:
   ```bash
   type -t cd
   ```

5. **Verificar o caminho de um executável**:
   ```bash
   type -p python
   ```

## Tips
- Utilize `type` para diagnosticar problemas com comandos que não estão funcionando como esperado, ajudando a identificar se você está chamando um alias ou uma função.
- Combine `type` com outros comandos, como `which`, para obter informações mais detalhadas sobre a localização de executáveis.
- Lembre-se de que `type` é uma built-in do Bash, portanto, não requer instalação adicional e está sempre disponível no seu terminal.