# Board - Sistema de Gerenciamento de Quadros

Este projeto é uma aplicação Java para gerenciamento de quadros (boards) no estilo Kanban, desenvolvida como estudo de estruturação de dados e separação em camadas com persistência em banco de dados. O sistema permite a organização de cartões em colunas de um quadro, suportando funcionalidades como migração de banco de dados, controle de cartões e interação via console.

## Funcionalidades

- Execução de migração de banco de dados com **Liquibase**
- Interface de console com menu principal
- Criação e manipulação de quadros, colunas e cartões
- Tratamento de exceções como cartões bloqueados, finalizados e entidades inexistentes
- Estrutura DTO para transferência de dados
- Conexão com banco de dados MySQL

## Tecnologias Utilizadas

- **Java**
- **Gradle Kotlin DSL**
- **Liquibase** (migração de banco de dados)
- **MySQL** (persistência)
- **Lombok** (para reduzir boilerplate de código)
- **JUnit Platform** (para testes)

## Estrutura do Projeto

board-master/

```bash
├── src/
│ ├── main/
│ │ ├── java/br/com/dio/
│ │ │ ├── dto/ # Data Transfer Objects
│ │ │ ├── exception/ # Exceções customizadas
│ │ │ ├── persistence/ # Configurações e acesso ao banco
│ │ │ ├── ui/ # Interface via terminal
│ │ │ └── Main.java # Classe principal
├── build.gradle.kts # Script de build (Gradle Kotlin DSL)
├── settings.gradle.kts # Configuração do projeto
└── liquibase.log # Log da última migração
```

## Requisitos

- Java 11 ou superior
- MySQL
- Gradle (ou utilize o wrapper incluído)

## Como Executar

1. Clone o repositório:
    ```bash
    git clone https://github.com/seuusuario/board.git
    cd board
    ```

    Configure o banco de dados MySQL e credenciais no arquivo de configuração (ex: ConnectionConfig.java).

    Execute a aplicação: ./gradlew run

## Licença

Este projeto é licenciado sob a licença MIT.
