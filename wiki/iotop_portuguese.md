# [Linux] Bash iotop Uso: Monitora o uso de I/O por processos

## Overview
O comando `iotop` é uma ferramenta útil para monitorar o uso de entrada e saída (I/O) de disco em sistemas Linux. Ele exibe uma lista de processos que estão consumindo I/O, permitindo que os administradores identifiquem quais aplicações estão utilizando mais recursos de disco.

## Usage
A sintaxe básica do comando `iotop` é a seguinte:

```bash
iotop [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `iotop`:

- `-o`, `--only`: Mostra apenas os processos que estão fazendo uso de I/O.
- `-b`, `--batch`: Executa o `iotop` em modo batch, útil para redirecionar a saída para um arquivo.
- `-d`, `--delay`: Define o intervalo de atualização em segundos (padrão é 1 segundo).
- `-p`, `--pid`: Monitora apenas o processo com o ID especificado.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `iotop`:

1. **Executar o iotop em modo interativo:**
   ```bash
   iotop
   ```

2. **Mostrar apenas processos que estão utilizando I/O:**
   ```bash
   iotop -o
   ```

3. **Executar o iotop em modo batch e salvar a saída em um arquivo:**
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. **Definir um intervalo de atualização de 2 segundos:**
   ```bash
   iotop -d 2
   ```

5. **Monitorar um processo específico pelo seu PID:**
   ```bash
   iotop -p 1234
   ```

## Tips
- Utilize o modo batch para registrar o uso de I/O ao longo do tempo, o que pode ser útil para análise posterior.
- Combine o `iotop` com outras ferramentas como `grep` para filtrar resultados específicos.
- Lembre-se de que o `iotop` requer permissões de superusuário para monitorar todos os processos. Use `sudo` se necessário.