📘 Helpdesk Full Stack (Spring Boot + Angular)

Sistema completo para gestão de chamados de suporte técnico (Helpdesk), desenvolvido como projeto acadêmico de Desenvolvimento Web Full Stack. O sistema utiliza uma arquitetura moderna separando API RESTful e Cliente SPA.

💻 Sobre o Projeto

O objetivo do sistema é gerenciar o ciclo de vida de atendimentos de TI, controlando Técnicos, Clientes e Chamados. O sistema implementa regras de negócio robustas, controle de acesso (RBAC) e validações de integridade.

Principais Funcionalidades

Autenticação JWT: Login seguro com token e sessão expirável.

Dashboard: Visão geral com estatísticas de chamados em tempo real.

Gestão de Técnicos: CRUD completo com perfil de Administrador.

Gestão de Clientes: Cadastro e manutenção da base de clientes.

Gestão de Chamados:

Abertura de tickets com prioridade e status.

Histórico de observações.

Regras de encerramento.

Controle de Acesso:

ADMIN: Acesso total ao sistema.

TÉCNICO: Acesso operacional (não pode excluir colegas ou alterar configurações sensíveis).

🛠 Tecnologias Utilizadas

Backend (API REST)

Java 11+ com Spring Boot 2.x

Spring Security + JWT (Autenticação/Autorização)

Spring Data JPA + Hibernate

Banco de Dados H2 (Ambiente de Teste/Memória)

Maven (Gerenciador de dependências)

Bean Validation (Validação de dados)

Frontend (SPA)

Angular 12+

TypeScript

Angular Material (Interface e Componentes)

RxJS (Programação Reativa)

Interceptor (Tratamento de erros e Tokens)

AuthGuard (Proteção de Rotas)

⚙️ Regras de Negócio e Segurança

O sistema possui travas de segurança tanto no Frontend quanto no Backend:

Proteção de Rotas: Usuários não logados são redirecionados para o Login.

Sessão Zumbi: Se o token expirar, o sistema encerra a sessão automaticamente.

Integridade de Dados: Não é possível excluir Clientes ou Técnicos que possuem chamados vinculados.

Hierarquia:

Técnicos comuns não podem criar/editar/excluir outros Técnicos.

Técnicos comuns podem gerenciar Clientes e Chamados livremente.

🚀 Como Executar o Projeto

Pré-requisitos

Java JDK 11 ou superior

Node.js e NPM

Angular CLI (npm install -g @angular/cli)

1️⃣ Rodando o Backend

Clone este repositório.

Abra a pasta do projeto backend na sua IDE (IntelliJ/Eclipse/VS Code).

Aguarde o Maven baixar as dependências.

Execute a classe principal HelpdeskApplication.java.

O servidor iniciará na porta 8080.

Banco de Dados H2 Console: http://localhost:8080/h2-console

2️⃣ Rodando o Frontend

Abra o terminal na pasta do projeto frontend.

Instale as dependências:

npm install


Execute o servidor:

ng serve


Acesse pelo navegador: http://localhost:4200

🧪 Credenciais de Teste

O banco de dados H2 é recriado a cada execução. Utilize os usuários padrão (se configurados no DBService) ou crie novos via banco:

Perfil

E-mail

Senha Padrão

Administrador

admin@mail.com

123

Técnico

tecnico@mail.com

123

🎨 Layout e Telas

O sistema utiliza o Angular Material para garantir responsividade e usabilidade.

Login: Interface limpa para autenticação.

Listagens: Tabelas com paginação e indicadores visuais (Badges coloridos para Status e Prioridade).

Formulários: Validação em tempo real (campos obrigatórios, e-mail válido, CPF).

Alertas: Feedback visual (Snackbars/Alerts) para sucesso ou erro (ex: "Acesso Negado").

📝 Licença

Este projeto foi desenvolvido para fins acadêmicos. Sinta-se à vontade para usar como base para estudos.

Feito com ☕ e código.