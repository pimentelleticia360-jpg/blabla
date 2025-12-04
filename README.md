# 📘 Helpdesk Full Stack (Spring Boot + Angular)

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![Postgres](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)

Sistema completo para gestão de chamados de suporte técnico (Helpdesk), desenvolvido como projeto acadêmico de Desenvolvimento Web Full Stack. O sistema utiliza uma arquitetura moderna separando **API RESTful** e **Cliente SPA**.

---

## 💻 Sobre o Projeto

O objetivo do sistema é gerenciar o ciclo de vida de atendimentos de TI, controlando **Técnicos**, **Clientes** e **Chamados**. O sistema implementa regras de negócio robustas, controle de acesso (RBAC) e validações de integridade de dados.

### Principais Funcionalidades

* **Autenticação JWT:** Login seguro com token e sessão expirável.
* **Dashboard:** Visão geral com estatísticas de chamados em tempo real.
* **Gestão de Técnicos:** CRUD completo com perfil de Administrador.
* **Gestão de Clientes:** Cadastro e manutenção da base de clientes.
* **Gestão de Chamados:**
    * Abertura de tickets com prioridade (Baixa, Média, Alta) e status.
    * Histórico de observações.
    * Regras de encerramento automáticas.
* **Controle de Acesso (RBAC):**
    * **ADMIN:** Acesso total ao sistema.
    * **TÉCNICO:** Acesso operacional (com restrições para excluir dados sensíveis ou gerenciar outros técnicos).

---

## 🛠 Tecnologias Utilizadas

### Backend (API REST)
* **Linguagem:** Java 11+
* **Framework:** Spring Boot 2.x
* **Segurança:** Spring Security + JWT (Autenticação/Autorização)
* **ORM:** Spring Data JPA + Hibernate
* **Banco de Dados:** H2 (Ambiente de Teste/Memória)
* **Build:** Maven
* **Validação:** Bean Validation

### Frontend (SPA)
* **Framework:** Angular 12+
* **Linguagem:** TypeScript
* **UI/UX:** Angular Material
* **Reatividade:** RxJS
* **Segurança Front:** Interceptor (Tratamento de erros e Tokens) & AuthGuard

---

## ⚙️ Regras de Negócio e Segurança

O sistema possui travas de segurança tanto no Frontend quanto no Backend:

1.  **Proteção de Rotas:** Usuários não logados são redirecionados automaticamente para o Login.
2.  **Sessão Zumbi:** Se o token expirar ou for inválido, o sistema encerra a sessão via Interceptor.
3.  **Integridade de Dados:** Não é possível excluir Clientes ou Técnicos que possuem chamados vinculados (*Foreign Key Constraint*), garantindo a integridade do histórico.
4.  **Hierarquia de Permissões:**
    * Técnicos comuns **não podem** criar, editar ou excluir outros Técnicos.
    * Técnicos comuns podem gerenciar Clientes e Chamados livremente.

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
* Java JDK 11 ou superior.
* Node.js e NPM.
* Angular CLI (`npm install -g @angular/cli`).

### 1️⃣ Rodando o Backend

1.  Clone este repositório.
2.  Abra a pasta do projeto `backend` (ou raiz) na sua IDE favorita (IntelliJ, Eclipse, VS Code).
3.  Aguarde o Maven baixar as dependências.
4.  Execute a classe principal `HelpdeskApplication.java`.

O servidor iniciará na porta **8080**.
> **Banco de Dados H2 Console:** [http://localhost:8080/h2-console](http://localhost:8080/h2-console)

### 2️⃣ Rodando o Frontend

1.  Abra o terminal na pasta do projeto `frontend`.
2.  Instale as dependências:
    ```bash
    npm install
    ```
3.  Execute o servidor de desenvolvimento:
    ```bash
    ng serve
    ```
4.  Acesse o sistema no navegador em: `http://localhost:4200`

---

## 📝 Licença

Este projeto foi desenvolvido para fins acadêmicos. Sinta-se à vontade para utilizar para estudos.
