# [Linux] Bash docker uso: Gerenciar contêineres e imagens

## Overview
O comando `docker` é uma ferramenta poderosa que permite gerenciar contêineres e imagens no ambiente Docker. Ele facilita a criação, execução e gerenciamento de aplicativos em contêineres, proporcionando um ambiente isolado e consistente para o desenvolvimento e a produção.

## Usage
A sintaxe básica do comando `docker` é a seguinte:

```bash
docker [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `docker`:

- `run`: Cria e inicia um novo contêiner a partir de uma imagem.
- `ps`: Lista todos os contêineres em execução.
- `images`: Lista todas as imagens disponíveis no sistema.
- `rm`: Remove um ou mais contêineres.
- `rmi`: Remove uma ou mais imagens.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `docker`:

1. **Executar um contêiner simples**:
   ```bash
   docker run hello-world
   ```

2. **Listar contêineres em execução**:
   ```bash
   docker ps
   ```

3. **Listar todas as imagens disponíveis**:
   ```bash
   docker images
   ```

4. **Remover um contêiner específico**:
   ```bash
   docker rm nome_do_container
   ```

5. **Remover uma imagem específica**:
   ```bash
   docker rmi nome_da_imagem
   ```

## Tips
- Sempre verifique se o Docker está em execução antes de usar os comandos.
- Utilize `docker ps -a` para listar todos os contêineres, incluindo os que não estão em execução.
- Mantenha suas imagens e contêineres organizados, removendo aqueles que não são mais necessários para economizar espaço em disco.
- Explore a documentação oficial do Docker para aprender sobre opções e comandos avançados.