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
* **Framework:** Spring Boot
