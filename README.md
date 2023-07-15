# Fullcycle-gRPC

## Preparando o ambiente

### Instalando gRPC usando Golang 

- [Instalação gRPC GoLang](https://grpc.io/docs/languages/go/quickstart/)

### Conectando no banco de dados (SQLite3)

```bash
sqlite3 db.sqlite 
```
## Como rodar essa aplicação ?

```go
go run cmd/grpcServer/main.go
```

## Alterando um arquivo Proto

Se você alterar um arquivo da pasta proto (course_category.proto), você previsa gerar os métodos rpc através do seguinte comando abaixo:

```bash
protoc --go_out=. --go-grpc_out=. proto/course_category.proto
```

## Usando o Evans (Client gRPC) para chamar seus procedimentos gRPC

[Evans](https://github.com/ktr0731/evans)

### Executando Evans

```bash
evans -r repl
```

### Chamando procedimento gRPC

```bash
call nomeDoSeuProcedimento
```

Exemplo:

```bash
call CreateCategoryStreamBidirectional
```


