
# 🏥 Projeto API Médica - Spring Boot

Este é um projeto backend de uma API RESTful desenvolvida com **Spring Boot**, voltada para o gerenciamento de médicos. Ele permite o cadastro, listagem, atualização e exclusão lógica de médicos, com integração a banco de dados usando **JPA/Hibernate** e **Flyway** para versionamento de schema.

## 🚀 Tecnologias Utilizadas

- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA
- Flyway (Migrations)
- H2 Database (ambiente de dev)
- Maven
- Lombok

## 📁 Estrutura do Projeto

```
src/
└── main
    ├── java
    │   └── med.voll.api
    │       ├── ApiApplication.java         # Classe principal
    │       ├── controller/
    │       │   ├── HelloController.java
    │       │   └── MedicoController.java   # Endpoints da API
    │       ├── endereco/
    │       │   ├── DadosEndereco.java
    │       │   └── Endereco.java
    │       └── medico/
    │           ├── DadosCadastroMedico.java
    │           ├── DadosAtualizacaoMedico.java
    │           ├── DadosListagemMedico.java
    │           ├── Especialidade.java
    │           ├── Medico.java
    │           └── MedicoRepository.java
    └── resources
        ├── application.properties          # Configurações do Spring
        └── db/migration/                   # Scripts Flyway
            ├── V1__create-table-medicos.sql
            └── V2__alter-table-medicos-add-column-telefone.sql
```

## 🧪 Endpoints Disponíveis

- `GET /hello`: **Teste de conexão (Hello World)**
- `POST /medicos`: **Cadastrar médico**
- `GET /medicos`: **Listar médicos ativos (com paginação)**
- `PUT /medicos`: **Atualizar dados do médico**
- `DELETE /medicos/{id}`: **Exclusão lógica (não remove do banco)**

## 🛠️ Como Rodar Localmente

**1. Clone o repositório:**

```bash
git clone https://github.com/iamyago/VollMed_api.git
cd VollMed_api
```

**2. Compile o projeto:**

```bash
./mvnw clean install
```

**3. Rode o projeto:**

```bash
./mvnw spring-boot:run
```

**4. Acesse a aplicação:**

- **API**: [http://localhost:8080](http://localhost:8080)  
- **H2 Console** (se habilitado): [http://localhost:8080/h2-console](http://localhost:8080/h2-console)

## 📝 Observações

- O projeto está configurado para criar as tabelas automaticamente e aplicar as **migrations Flyway** ao iniciar.
- A exclusão de médicos é **lógica**, ou seja, o médico permanece no banco mas é marcado como inativo.

---

📌 Este projeto é parte do aprendizado do curso **"Spring Boot 3 - Alura"**.
