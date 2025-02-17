# [Linux] Bash basename uso equivalente: Extrair o nome de um arquivo

O comando `basename` é utilizado para extrair o nome de um arquivo ou diretório a partir de um caminho completo, removendo a parte do diretório e, opcionalmente, a extensão do arquivo.

## Overview
O `basename` é uma ferramenta útil para simplificar caminhos de arquivos, permitindo que você obtenha apenas o nome do arquivo ou diretório sem a parte do caminho. Isso é especialmente útil em scripts e automações.

## Usage
A sintaxe básica do comando `basename` é a seguinte:

```bash
basename [opções] [argumentos]
```

## Common Options
- `-a`: Aceita múltiplos argumentos e retorna o nome base para cada um deles.
- `-s SUFIX`: Remove a sufixo especificado do nome do arquivo, se presente.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `basename`:

1. **Extrair o nome de um arquivo a partir de um caminho completo:**

```bash
basename /home/usuario/documentos/relatorio.txt
```
Saída:
```
relatorio.txt
```

2. **Extrair apenas o nome do arquivo sem a extensão:**

```bash
basename /home/usuario/documentos/relatorio.txt .txt
```
Saída:
```
relatorio
```

3. **Usar com múltiplos arquivos:**

```bash
basename -a /home/usuario/documentos/relatorio.txt /home/usuario/imagens/foto.jpg
```
Saída:
```
relatorio.txt
foto.jpg
```

4. **Remover um sufixo específico:**

```bash
basename /home/usuario/documentos/relatorio.txt .txt
```
Saída:
```
relatorio
```

## Tips
- Utilize `basename` em scripts para facilitar a manipulação de arquivos e diretórios.
- Combine `basename` com outros comandos, como `find`, para processar múltiplos arquivos de forma eficiente.
- Lembre-se de que o `basename` não altera os arquivos, apenas retorna o nome base, tornando-o seguro para uso em scripts.