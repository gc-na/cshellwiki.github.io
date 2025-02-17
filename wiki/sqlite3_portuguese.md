# [Linux] Bash sqlite3 Uso: Interagir com bancos de dados SQLite

## Overview
O comando `sqlite3` é uma ferramenta de linha de comando para interagir com bancos de dados SQLite. Ele permite que os usuários executem consultas SQL, criem e modifiquem bancos de dados, além de gerenciar dados de forma eficiente.

## Usage
A sintaxe básica do comando `sqlite3` é a seguinte:

```bash
sqlite3 [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `sqlite3`:

- `-help`: Exibe a ajuda e as opções disponíveis.
- `-version`: Mostra a versão do SQLite.
- `-init <arquivo>`: Executa comandos SQL de um arquivo ao iniciar o sqlite3.
- `-batch`: Executa em modo batch, sem interação do usuário.
- `-cmd <comando>`: Executa um comando SQL antes de entrar no shell interativo.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o comando `sqlite3`:

1. **Criar um novo banco de dados:**
   ```bash
   sqlite3 meu_banco_de_dados.db
   ```

2. **Criar uma tabela:**
   ```bash
   sqlite3 meu_banco_de_dados.db "CREATE TABLE usuarios (id INTEGER PRIMARY KEY, nome TEXT);"
   ```

3. **Inserir dados na tabela:**
   ```bash
   sqlite3 meu_banco_de_dados.db "INSERT INTO usuarios (nome) VALUES ('João');"
   ```

4. **Consultar dados:**
   ```bash
   sqlite3 meu_banco_de_dados.db "SELECT * FROM usuarios;"
   ```

5. **Exportar dados para um arquivo CSV:**
   ```bash
   sqlite3 -header -csv meu_banco_de_dados.db "SELECT * FROM usuarios;" > usuarios.csv
   ```

## Tips
- Sempre faça backup do seu banco de dados antes de realizar operações destrutivas.
- Utilize o modo `-batch` para executar scripts SQL automaticamente sem interação.
- Explore a opção `-init` para carregar configurações ou comandos padrão ao iniciar o sqlite3.
- Para facilitar a leitura, use `-header` ao consultar dados, assim os nomes das colunas serão exibidos.