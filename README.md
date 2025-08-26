# 🎮 DSList - API de Lista de Jogos

Projeto desenvolvido durante o **Intensivão Java Spring** da [DevSuperior](https://devsuperior.com.br), com foco em arquitetura de software, API REST, boas práticas com Spring Boot e persistência de dados com JPA.

---

## 📌 Sobre o Projeto
O **DSList** é uma API REST que permite:
- Listar jogos cadastrados no sistema;
- Organizar jogos em listas;
- Reordenar a posição de jogos dentro de uma lista.

Este projeto foi criado com **Java + Spring Boot** e segue o padrão de **arquitetura em camadas** (`controllers → services → repositories → entities → dtos`).

---

## 🚀 Tecnologias Utilizadas
- **Java 17+**
- **Spring Boot**
- **Spring Data JPA**
- **H2 Database** (perfil de teste)
- **PostgreSQL** (perfil de produção)
- **Maven**
- **Docker** (opcional para banco em produção)
- **GitHub Actions** (CI/CD)

---

## 📂 Estrutura do Projeto
src/

├── main/

│ ├── java/com/devsuperior/dslist/

│ │ ├── controllers/ → Endpoints da API

│ │ ├── services/ → Regras de negócio

│ │ ├── repositories/ → Acesso ao banco

│ │ ├── entities/ → Entidades JPA

│ │ └── dtos/ → Objetos de transferência

│ └── resources/
│
│ ├── application.properties → Configurações

│ └── import.sql → Seed de dados

└── test/ → Testes automatizados

---

## ⚙️ Como Executar o Projeto

### Pré-requisitos
- Java 17 ou superior instalado
- Maven (ou usar o **Maven Wrapper** incluso no projeto)
- Docker (opcional, se quiser rodar PostgreSQL localmente)

### Passo a passo
1. Clone o repositório:
   ```bash
   git clone https://github.com/Rubem-Alcantara/dslist.git
   
   Caso prefira clonar o repositório original:
   git clone https://github.com/devsuperior/dslist-backend.git
   
   cd dslist

2. Execute o projeto de uma das seguintes formas:

▶️ Usando o Spring Tool Suite (STS):

- Abra o STS e importe o projeto como Maven Project.
- Aguarde o download das dependências.

3. Teste a API utilizando o Postman (ou outra ferramenta similar).

- Abra o Postman
- Crie uma nova requisição apontando para: http://localhost:8080
- Utilize os endpoints disponíveis (ex.: GET /games, GET /lists, etc.) para validar as respostas.

--------

📡 Endpoints Principais

🔹 Listar todos os jogos: GET /games
<img width="1153" height="237" alt="image" src="https://github.com/user-attachments/assets/06917022-08d5-4ebf-9e36-eb4e2fc43c1a" />

🔹 Listar todas as listas: GET /lists

<img width="411" height="164" alt="image" src="https://github.com/user-attachments/assets/3f3741b9-9a0e-4d70-a359-74b9c078ab47" />

🔹 Listar jogos de uma lista específica: GET /lists/{listId}/games
<img width="1157" height="240" alt="image" src="https://github.com/user-attachments/assets/f1aeea91-7d9c-43ec-9eea-f692e33810c5" />

🔹 Reordenar jogos em uma lista

Requisição sendo realizada no Postman:
<img width="740" height="232" alt="image" src="https://github.com/user-attachments/assets/d1a596c7-8e19-4b74-a6c0-1036da78bf47" />

Antes de executar:

<img width="365" height="147" alt="image" src="https://github.com/user-attachments/assets/74aa200b-4820-4579-9c7b-219e70efd3fc" />

Depois de executar:

<img width="367" height="169" alt="image" src="https://github.com/user-attachments/assets/b6b2aa54-08c4-4064-9cc3-bb3e50db3770" />


🗄️ Banco de Dados

- Perfil test: usa banco H2 em memória (configuração padrão).
- Perfil dev/prod: usa PostgreSQL.
- Arquivo de configuração: src/main/resources/application.properties
- Arquivo de seed: src/main/resources/import.sql

✅ Próximos Passos e Melhorias

{Em desenvolvimento...}

👨‍💻 Autor

Projeto desenvolvido por Rubem Alcantara durante o Intensivão Java Spring da DevSuperior.
