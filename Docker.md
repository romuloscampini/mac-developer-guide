# Informações de Docker

##Link Úteis

###Download e Instalação
https://docs.docker.com/docker-for-mac/

###Imagens públicas
https://hub.docker.com/explore/

##Containers
###Postgres:

Executa o container do postgres com
- Nome: postgresdb
- Porta: 15432 (Host Físico)
- Senha: 123456
```
docker run --name postgresdb -e POSTGRES_PASSWORD=123456 -p 15432:5432 -d postgres:9.4
```

Criar container com acesso a volume externo 
(Parametro -v -> PastaHostFisico:PastaContainer)
```
docker run --name dbExterno -e POSTGRES_PASSWORD=123456 -p 12451:5432 -v /Users/romuloscampini/Development/Touch/docker-share:/tmp/ -d postgres:9.4
```

List o container em execução
```
docker ps
```

Para o container ou Inicia
```
docker stop NomeContainer
docker start NomeContainer
```
