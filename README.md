# DIO FORMAÇÃO DOCKER

## O QUE É CONTAINER

Tecnologia usada para reunir um app e todos os seus arquivos em um ambiente de tempo de execução. Um container pode ser movido e executado em qualquer sistema operacional e contexto Oferece flexibilidade para criar, implantar, copiar e migrar um container de um ambiente a outro.

## O QUE É DOCKER

Software que permite trabalhar com containers como se fossem "Máquinas virtuais" modulares e leves.

## DOCKER

### Primeiros passos

**1. Verificar as imagens baixadas**

```bash
docker images
```

**2. Baixando primeira imagem**

```bash
docker pull hello-world
```

**3. Executando primeira imagem**

```bash
docker run hello-world
```

**4. Status do que ocorreu recentemente**

```bash
docker ps -a
```

ou 

```bash
docker container ls
```

**5. Apresentar containers em execução**

```bash
docker ps
```

**6. Executar containers por x segundos**

```bash
docker run hello-world sleep 10
```

**6. Executar containers em modo interativo**

```bash
docker run -it ubuntu
```

ou 

```bash
docker container run
```

OBS: Para sair do container com ubuntu, basta digitar:

```bash
exit
```

**7. Visualizar a ajuda**

```bash
docker help
```

ou 

```bash
docker container help
```

## RODANDO UBUNTU NUM CONTAINER

```bash
docker pull ubuntu
```

### Rodando o nano

```bash
docker run -dti ubuntu
docker exec -it [id do container] /bin/bash
apt update
apt upgrade
apt install nano
```
### Fechando o container

```bash
docker stop [id do container]
```

### Excluindo o container

```bash
docker rm [id do container]
```

### Verificando imagens

```bash
docker images
```

### Excluindo a imagem

```bash
docker rmi hello-world
```

obs: Só pode excluir a imagem se o docker for excluído antes

### Nomeando o container

Note que "ubuntu" é a imagem

```bash
docker run -dti --name [Nome que você deseja para o container] ubuntu
```

