# [Linux] Bash default comando: [executar comandos no terminal]

## Overview
O comando `default` no contexto do Bash não é um comando padrão. No entanto, se você estiver se referindo ao comando `bash`, ele é usado para iniciar uma nova sessão do shell Bash. O Bash é um interpretador de comandos que permite aos usuários interagir com o sistema operacional através de uma interface de linha de comando.

## Usage
A sintaxe básica do comando `bash` é a seguinte:

```bash
bash [opções] [arquivo]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `bash`:

- `-c`: Executa um comando passado como string.
- `-i`: Inicia uma sessão interativa.
- `--version`: Exibe a versão do Bash instalado.
- `-l`: Inicia uma sessão de login.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `bash`:

1. **Iniciar uma nova sessão do Bash:**
   ```bash
   bash
   ```

2. **Executar um comando específico:**
   ```bash
   bash -c "echo 'Olá, mundo!'"
   ```

3. **Iniciar uma sessão interativa:**
   ```bash
   bash -i
   ```

4. **Verificar a versão do Bash:**
   ```bash
   bash --version
   ```

5. **Iniciar uma sessão de login:**
   ```bash
   bash -l
   ```

## Tips
- Utilize `bash -c` para executar scripts ou comandos de forma rápida sem precisar criar um arquivo separado.
- Para scripts mais complexos, considere criar um arquivo `.sh` e executá-lo com `bash nome_do_arquivo.sh`.
- Sempre verifique a versão do Bash para garantir que você está utilizando recursos compatíveis com seu sistema.