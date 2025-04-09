# 🛒 EShop - E-commerce com Arquitetura de Microsserviços

Este projeto é uma aplicação de e-commerce desenvolvida com foco em **arquitetura de microsserviços**, utilizando as tecnologias mais recentes do ecossistema **.NET 8** e aplicando **boas práticas de engenharia de software**, como **DDD**, **CQRS**, **Clean Architecture**, entre outras.

## 🧠 Principais Conceitos e Tecnologias Aplicadas

- ASP.NET Core 8 Web API com Minimal APIs e C# 12
- Vertical Slice Architecture com Feature Folders
- CQRS com MediatR e validações com FluentValidation
- Marten (PostgreSQL) e Entity Framework Core (SQL Server)
- Redis como cache distribuído
- Comunicação entre serviços com gRPC e RabbitMQ
- MassTransit para abstração da mensageria
- API Gateway com YARP + Rate Limiting
- Design Patterns: Proxy, Decorator, Cache-aside
- Docker, Logging, Health Checks, Exception Handling

## 📦 Microsserviços

- `Catalog.API`
- `Basket.API`
- `Discount.gRPC`
- `Ordering.API`
- `ApiGateway.Yarp`

## 🚀 Como Executar

Certifique-se de ter o [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0), [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/) instalados.\
Seria bem útil possuir também o [Docker Desktop](https://www.docker.com/products/docker-desktop/) para facilitar as interações com os contêineres.

Na raiz do projeto, execute:

```bash
docker-compose up --build
```

Acesse os serviços via API Gateway com base nas rotas do YARP.

📬 Teste das APIs com Postman
Este projeto inclui uma collection pronta para facilitar o teste dos endpoints com o Postman.

✅ Como importar:
Baixe o arquivo [EShop Microservices.postman_collection.json](./postman/EShop%20Microservices.postman_collection.json) incluído neste repositório.

Abra o Postman.

Vá em File > Import e selecione a collection.

Configure as variáveis de ambiente no Postman:

```bash
(Docker) 
catalog_url = https://localhost:6060
basket_url = http://localhost:6061
ordering_url = http://localhost:6063
yarp_url = http://localhost:6064

(Localhost)
catalog_url = https://localhost:5050
basket_url = http://localhost:5051
ordering_url = http://localhost:5053
yarp_url = http://localhost:5054
```

Agora você pode testar os endpoints das APIs de forma rápida e prática! 🧪

📚 Aprendizados
Este projeto consolida conhecimentos em .NET moderno, microsserviços, mensageria, arquitetura limpa, práticas de DDD, comunicação eficiente entre serviços e uso profissional de ferramentas como o Docker.
