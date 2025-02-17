# [Linux] Bash mkdir Uso: Criação de diretórios

## Overview
O comando `mkdir` é utilizado para criar novos diretórios no sistema de arquivos. Ele permite que os usuários organizem seus arquivos em pastas, facilitando a gestão e o acesso a eles.

## Usage
A sintaxe básica do comando `mkdir` é a seguinte:

```bash
mkdir [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `mkdir`:

- `-p`: Cria diretórios pai conforme necessário. Se os diretórios intermediários não existirem, eles serão criados.
- `-v`: Exibe uma mensagem para cada diretório que é criado, útil para verificar se o comando foi executado corretamente.
- `-m`: Define as permissões do diretório criado, utilizando a notação octal.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `mkdir`:

1. **Criar um único diretório:**
   ```bash
   mkdir meu_diretorio
   ```

2. **Criar múltiplos diretórios ao mesmo tempo:**
   ```bash
   mkdir dir1 dir2 dir3
   ```

3. **Criar um diretório e seus diretórios pai:**
   ```bash
   mkdir -p /caminho/para/meu_diretorio/novo_diretorio
   ```

4. **Criar um diretório e exibir uma mensagem:**
   ```bash
   mkdir -v meu_diretorio
   ```

5. **Criar um diretório com permissões específicas:**
   ```bash
   mkdir -m 755 meu_diretorio
   ```

## Tips
- Sempre verifique se o diretório que você está tentando criar já existe para evitar erros.
- Utilize a opção `-p` ao criar diretórios aninhados para garantir que todos os diretórios necessários sejam criados.
- Combine o `mkdir` com outros comandos, como `cd`, para facilitar a navegação após a criação de diretórios.