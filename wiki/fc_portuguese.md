# [Linux] Bash fc Uso: Editar e reexecutar comandos anteriores

## Overview
O comando `fc` no Bash é utilizado para listar, editar e reexecutar comandos que foram executados anteriormente no shell. Ele permite que os usuários revisitem e modifiquem comandos passados, facilitando a correção de erros ou a repetição de tarefas.

## Usage
A sintaxe básica do comando `fc` é a seguinte:

```bash
fc [opções] [argumentos]
```

## Common Options
- `-l`: Lista os comandos anteriores.
- `-r`: Reexecuta os comandos na ordem inversa.
- `-s`: Executa o comando sem abrir um editor.
- `-n`: Não exibe números de linha ao listar os comandos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `fc`:

1. **Listar os últimos 10 comandos executados:**
   ```bash
   fc -l -n -10
   ```

2. **Editar o último comando executado:**
   ```bash
   fc
   ```

3. **Reexecutar o último comando sem edição:**
   ```bash
   fc -s
   ```

4. **Listar os últimos 5 comandos e reexecutar o terceiro:**
   ```bash
   fc -l -n -5
   fc -s 3
   ```

5. **Reexecutar todos os comandos em ordem inversa:**
   ```bash
   fc -r
   ```

## Tips
- Utilize `fc` para corrigir rapidamente erros em comandos anteriores sem precisar digitá-los novamente.
- Combine `fc` com outros comandos, como `grep`, para filtrar comandos específicos.
- Lembre-se de que o `fc` abre o editor de texto padrão do seu sistema, então familiarize-se com ele para uma edição eficiente.