# Catalog Admin

Microsserviço de administração de catálogo de vídeos, desenvolvido durante o Full Cycle 3.0.

Responsável por gerenciar entidades do domínio de streaming — categorias, gêneros e vídeos — com foco em qualidade de design e separação de responsabilidades.

## Arquitetura

O projeto segue Clean Architecture com separação explícita em camadas:

```
src/
├── domain/          # Entidades, Value Objects, interfaces de repositório
├── application/     # Use cases, DTOs, regras de aplicação
└── infrastructure/  # Persistência, controllers, configuração Spring
```

A camada de domínio não possui dependência de frameworks — as regras de negócio são isoladas e testáveis independentemente da infraestrutura.

## Funcionalidades

- CRUD de categorias, gêneros e vídeos
- Relacionamento entre entidades do domínio
- Validações no nível de domínio
- Exposição via API REST

## Stack

- Java 17
- Spring Boot
- Hibernate / JPA
- Gradle
- Docker

## Como executar

```bash
docker-compose up -d
./gradlew bootRun
```

## Aprendizados

Este projeto foi o ponto de entrada prático em Clean Architecture com Java. A separação entre domínio e infraestrutura que parece custosa no início se justifica quando os use cases crescem e a necessidade de trocar implementações surge sem impacto no núcleo do negócio.
