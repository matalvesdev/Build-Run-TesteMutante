# Build-Run-TesteMutante

## 📋 Sobre o Projeto

Projeto Maven focado em testes unitários e testes de mutação utilizando JUnit 5, Mockito e PITest. Este repositório demonstra boas práticas de desenvolvimento de software com ênfase em qualidade de código através de testes robustos.

## 🚀 Tecnologias

Este projeto utiliza as seguintes tecnologias e frameworks, conforme definido no `pom.xml`:

### Linguagem e Build
- **Java**: 21
- **Maven**: Build automation tool
- **Encoding**: UTF-8

### Frameworks de Teste
- **JUnit Jupiter**: 5.11.4
  - `junit-jupiter-api`: API para escrever testes
  - `junit-jupiter-engine`: Engine para executar testes
  - `junit-jupiter-params`: Suporte para testes parametrizados

### Mocking
- **Mockito**: 5.15.2
  - `mockito-core`: Framework de mocking
  - `mockito-junit-jupiter`: Integração Mockito com JUnit 5

### Teste de Mutação
- **PITest Maven Plugin**: 1.18.1
  - `pitest-junit5-plugin`: 1.2.1
  - Configurado para usar todos os mutadores disponíveis
  - Execução com 4 threads
  - Saída em formato HTML

## 📦 Informações do Projeto

- **Group ID**: `tech.buildrun`
- **Artifact ID**: `unittest`
- **Version**: `1.0-SNAPSHOT`

## 🎯 Estrutura do Projeto

O projeto está organizado nos seguintes módulos:

- **authms**: Sistema de autenticação com gestão de usuários
- **bankguard**: Validador de transações bancárias
- **ecommerce**: Serviço de pedidos (orders)
- **mockito**: Exemplos de uso do Mockito

## 🔧 Pré-requisitos

- Java 21 ou superior
- Maven 3.6 ou superior

## 🏗️ Como Compilar

Para compilar o projeto, execute:

```bash
mvn clean compile
```

## 🧪 Como Executar os Testes

### Executar todos os testes unitários:

```bash
mvn test
```

### Executar testes de mutação com PITest:

```bash
mvn test-compile org.pitest:pitest-maven:mutationCoverage
```

O relatório HTML será gerado no diretório `target/pit-reports/`.

## 📊 Configuração do PITest

O PITest está configurado com:
- **Threads**: 4 (execução paralela)
- **Mutadores**: ALL (todos os mutadores disponíveis)
- **Classes alvo**: `tech.buildrun.*`
- **Testes alvo**: `tech.buildrun.*Test`
- **Formato de saída**: HTML

## 📝 Dependências

Todas as dependências de teste estão no escopo `test`:

| Dependência | Versão | Finalidade |
|------------|--------|-----------|
| junit-jupiter-api | 5.11.4 | API do JUnit 5 |
| junit-jupiter-engine | 5.11.4 | Engine de execução do JUnit 5 |
| junit-jupiter-params | 5.11.4 | Testes parametrizados |
| mockito-core | 5.15.2 | Framework de mocking |
| mockito-junit-jupiter | 5.15.2 | Integração Mockito + JUnit 5 |

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## 📄 Licença

Este projeto é de código aberto e está disponível sob os termos descritos no repositório.