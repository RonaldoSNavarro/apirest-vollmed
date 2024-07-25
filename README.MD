# Voll.Med API

## Visão Geral

A **Voll.Med API** é uma API RESTful desenvolvida para gerenciar informações e processos relacionados a um sistema de gestão de saúde. A aplicação permite o gerenciamento de pacientes, médicos, agendamentos e outras entidades pertinentes a um sistema de saúde.

## Funcionalidades

- **Gerenciamento de Pacientes:**
  - Cadastro de novos pacientes
  - Atualização de informações de pacientes
  - Exclusão de registros de pacientes
  - Consulta de dados de pacientes

- **Gerenciamento de Médicos:**
  - Cadastro de novos médicos
  - Atualização de informações de médicos
  - Exclusão de registros de médicos
  - Consulta de dados de médicos

- **Gerenciamento de Agendamentos:**
  - Criação de novos agendamentos
  - Atualização de agendamentos existentes
  - Cancelamento de agendamentos
  - Consulta de agendamentos

- **Autenticação e Autorização:**
  - Registro de novos usuários
  - Login de usuários existentes
  - Autorização baseada em roles (paciente, médico, admin)

## Tecnologias Utilizadas

- **Backend:**
  - [Java](https://www.java.com/) com [Spring Boot](https://spring.io/projects/spring-boot)
  - [Spring Data JPA](https://spring.io/projects/spring-data-jpa)
  - [Hibernate](https://hibernate.org/)
  - [Flyway](https://flywaydb.org/)

- **Banco de Dados:**
  - [MySQL](https://www.mysql.com/)

- **Segurança:**
  - [Spring Security](https://spring.io/projects/spring-security) com JWT

- **Documentação da API:**
  - [Springfox Swagger](https://springfox.github.io/springfox/)

## Pré-requisitos

- [Java 11+](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- [Maven](https://maven.apache.org/)
- [MySQL](https://dev.mysql.com/downloads/mysql/)

## Como Executar

1. Clone o repositório:
    ```bash
    git clone https://github.com/seu-usuario/vollmed.api.git
    ```

2. Navegue até o diretório do projeto:
    ```bash
    cd vollmed.api
    ```

3. Configure o banco de dados MySQL com as credenciais adequadas no arquivo `application.properties`:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/vollmed
    spring.datasource.username=seu-usuario
    spring.datasource.password=sua-senha
    spring.jpa.hibernate.ddl-auto=none
    spring.flyway.enabled=true
    ```

4. Execute o projeto usando Maven:
    ```bash
    mvn spring-boot:run
    ```

5. A API estará disponível em:
    ```
    http://localhost:8080
    ```

## Documentação da API

A documentação completa da API pode ser acessada via Swagger em: http://localhost:8080/swagger-ui.html


## Estrutura de Classes

O projeto `med.voll.api` possui a seguinte estrutura de classes:

### Controller
- **AutenticacaoController**: Controlador responsável pela autenticação de usuários.
- **ConsultaController**: Controlador responsável pelas operações relacionadas às consultas médicas.
- **MedicoController**: Controlador responsável pelas operações relacionadas aos médicos.
- **PacienteController**: Controlador responsável pelas operações relacionadas aos pacientes.

### Domain
- **consulta**
  - **validacoes**
    - **AgendaDeConsultas**: Classe responsável pela agenda de consultas.
  - **Consulta**: Entidade que representa uma consulta médica.
  - **ConsultaRepository**: Repositório para gerenciar as consultas no banco de dados.
  - **DadosAgendamentoConsulta**: DTO para os dados de agendamento de consulta.
  - **DadosCancelamentoConsulta**: DTO para os dados de cancelamento de consulta.
  - **DadosDetalhamentoConsulta**: DTO para os detalhes de uma consulta.
  - **DadosListagemConsulta**: DTO para a listagem de consultas.
  - **MotivoCancelamento**: Enum para os motivos de cancelamento de consultas.

- **endereco**
  - **DadosEndereco**: DTO para os dados do endereço.
  - **Endereco**: Entidade que representa um endereço.

- **medico**
  - **DadosAtualizacaoMedico**: DTO para os dados de atualização do médico.
  - **DadosCadastroMedico**: DTO para os dados de cadastro do médico.
  - **DadosDetalhamentoMedico**: DTO para os detalhes de um médico.
  - **DadosListagemMedico**: DTO para a listagem de médicos.
  - **Especialidade**: Enum para as especialidades médicas.
  - **Medico**: Entidade que representa um médico.
  - **MedicoRepository**: Repositório para gerenciar os médicos no banco de dados.

- **paciente**
  - **DadosAtualizacaoPaciente**: DTO para os dados de atualização do paciente.
  - **DadosCadastroPaciente**: DTO para os dados de cadastro do paciente.
  - **DadosListagemPaciente**: DTO para a listagem de pacientes.
  - **Paciente**: Entidade que representa um paciente.
  - **PacienteRepository**: Repositório para gerenciar os pacientes no banco de dados.

- **usuario**
  - **AutenticacaoService**: Serviço para gerenciar a autenticação.
  - **DadosAutenticacao**: DTO para os dados de autenticação.
  - **Usuario**: Entidade que representa um usuário.
  - **UsuarioRepository**: Repositório para gerenciar os usuários no banco de dados.

### Infra
- **exception**
  - **TratadorDeErros**: Classe para tratamento de erros globais na aplicação.

- **security**
  - **DadosTokenJWT**: DTO para os dados do token JWT.
  - **SecurityConfigurations**: Configurações de segurança da aplicação.
  - **SecurityFilter**: Filtro de segurança para interceptar e validar as requisições.
  - **TokenService**: Serviço para manipulação de tokens JWT.

- **springdoc**
  - **SpringDocConfigurations**: Configurações para a documentação da API com SpringDoc.

### Aplicação
- **ApiApplication**: Classe principal da aplicação que contém o método `main`.

### Recursos
- **db.migration**: Diretório contendo os scripts de migração de banco de dados Flyway.
- **application.properties**: Arquivo de propriedades da aplicação para o ambiente padrão.
- **application-prod.properties**: Arquivo de propriedades da aplicação para o ambiente de produção.
- **application-test.properties**: Arquivo de propriedades da aplicação para o ambiente de teste.



# Desenvolvedor

[<img loading="lazy" src="https://avatars.githubusercontent.com/u/134724019?v=4" width=115><br><sub>Ronaldo Navarro</sub>](https://github.com/ronaldosnavarro)
- LinkedIn: https://www.linkedin.com/in/ronaldonavarro

---



