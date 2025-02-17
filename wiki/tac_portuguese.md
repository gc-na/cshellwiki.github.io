# [Linux] Bash tac Uso: Inverter a ordem das linhas de um arquivo

## Overview
O comando `tac` é utilizado para inverter a ordem das linhas de um arquivo. Ao contrário do comando `cat`, que exibe as linhas na ordem em que aparecem, o `tac` apresenta as linhas do final para o início, permitindo uma visualização reversa do conteúdo.

## Usage
A sintaxe básica do comando `tac` é a seguinte:

```bash
tac [opções] [argumentos]
```

## Common Options
- `-b`, `--before`: Coloca a linha de separação antes da linha.
- `-r`, `--regex`: Trata a expressão como uma expressão regular.
- `-s`, `--separator`: Define um separador diferente para inverter as linhas.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `tac`:

1. **Inverter as linhas de um arquivo**:
   ```bash
   tac arquivo.txt
   ```

2. **Inverter as linhas e salvar a saída em um novo arquivo**:
   ```bash
   tac arquivo.txt > arquivo_invertido.txt
   ```

3. **Usar um separador específico**:
   ```bash
   tac -s ',' arquivo.csv
   ```

4. **Inverter a saída de um comando**:
   ```bash
   ls -l | tac
   ```

## Tips
- Utilize `tac` em combinação com outros comandos para manipular e visualizar dados de forma mais eficiente.
- Lembre-se de que `tac` lê o arquivo inteiro na memória, portanto, para arquivos muito grandes, considere o impacto no desempenho.
- Experimente usar `tac` com opções de separador para manipular arquivos de dados estruturados, como CSV.