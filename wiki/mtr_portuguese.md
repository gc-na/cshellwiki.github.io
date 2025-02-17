# [Linux] Bash mtr Uso: Ferramenta de diagnóstico de rede

## Overview
O comando `mtr` (My Traceroute) combina as funcionalidades dos comandos `ping` e `traceroute` para fornecer uma análise em tempo real da rota que os pacotes de dados seguem até um destino específico. Ele é útil para diagnosticar problemas de rede, permitindo que os usuários vejam a latência e a perda de pacotes em cada salto da rota.

## Usage
A sintaxe básica do comando `mtr` é a seguinte:

```bash
mtr [opções] [destino]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `mtr`:

- `-r`: Executa o mtr em modo relatório, exibindo a saída de forma mais compacta.
- `-c [n]`: Define o número de pacotes a serem enviados (substitua `[n]` pelo número desejado).
- `-i [n]`: Define o intervalo entre os pacotes enviados (substitua `[n]` pelo valor em segundos).
- `-p`: Exibe o número da porta de cada salto.
- `-w`: Exibe a saída em um formato mais legível para humanos (modo "wide").

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `mtr`:

1. **Executar um mtr básico para um domínio:**
   ```bash
   mtr google.com
   ```

2. **Executar mtr em modo relatório para um IP específico:**
   ```bash
   mtr -r 8.8.8.8
   ```

3. **Definir o número de pacotes a serem enviados:**
   ```bash
   mtr -c 10 example.com
   ```

4. **Usar um intervalo de 2 segundos entre os pacotes:**
   ```bash
   mtr -i 2 example.com
   ```

5. **Exibir a saída em formato legível:**
   ```bash
   mtr -w google.com
   ```

## Tips
- Sempre execute o `mtr` com permissões de superusuário (usando `sudo`) para obter informações mais detalhadas sobre a rede.
- Combine as opções para personalizar a saída de acordo com suas necessidades, como o uso de `-r` e `-c` juntos para relatórios rápidos.
- Utilize o `mtr` regularmente para monitorar a saúde da sua conexão de rede e identificar possíveis problemas antes que se tornem críticos.