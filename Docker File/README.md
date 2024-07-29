# COMO CRIAR UM DOCKER FILE

## BAIXANDO IMAGEM DO UBUNTU

docker pull ubuntu
docker run -dti --name ubuntu-python ubuntu
docker exec -ti ubuntu-python bash
apt update
apt install -y python3 nano
apt clean
nano app.py
nome = input("Qual seu nome?")
print(nome)

ctrl+x
y
enter

python3 app.py

docker exit

docker exec -ti ubuntu-python python3 app.py

docker stop [id do container]

docker rm [id do container]

## CRIANDO O DOCKER FILE

Crie um arquivo chamado **dockerfile** igual como o presente nesta pasta

docker build . -t ubuntu-python
docker run -ti --name meu-app ubuntu-python 