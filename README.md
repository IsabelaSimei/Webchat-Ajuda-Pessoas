### **Descrição do Projeto: Webchat-Ajuda-Pessoas**
O projeto **Webchat-Ajuda-Pessoas** é uma plataforma web desenvolvida para conectar usuários e permitir a comunicação interativa em tempo real para prestação de ajuda e suporte.

---

### **Estrutura e Arquitetura do Sistema**
A aplicação é dividida em três módulos principais:

* **Backend Principal (`backend/`)**:
* Desenvolvido em **Node.js** com **TypeScript** e framework **Express**.
* Utiliza **TypeORM** para mapeamento objeto-relacional e gerenciamento de banco de dados via migrações.
* Implementa segurança através de criptografia de senhas com **BCrypt** (`BCryptHashProvider`) e middleware de verificação de autenticação (`ensureAuthenticated`).
* Organizado na estrutura de rotas, controllers e serviços (`CreateUserService`, `AuthenticateUserService`, `ShowProfileService`, `UpdateProfileService`, `DeleteProvileService`).

* **Servidor de Chat em Tempo Real (`chat/backend/`)**:
* Módulo isolado focado no gerenciamento do servidor de bate-papo (`ChatServer.ts`).
* Desenvolvido em **Node.js** e **TypeScript**.

* **Cliente de Chat (`chat/client/`)**:
* Aplicação desenvolvida em **React** com **TypeScript** voltada para a interface do chat.
* Utiliza **Context API** (`ChatContext.ts`) e integração com WebSockets (`SocketService.ts`) para troca instantânea de mensagens.

* **Frontend Principal (`frontend/`)**:
* Interface web em **React** para o sistema principal de navegação.

---

### **Principais Funcionalidades**
* **Autenticação e Controle de Acesso**: Registro de usuários, gerenciamento de sessões e rotas protegidas.
* **Gestão de Perfil**: Consulta, edição e exclusão de informações do perfil.
* **Lista de Contatos**: Módulo para busca e listagem de contatos e conexões entre pessoas (`ListUsersContactsService`, `users_contacts.routes.ts`).
* **Bate-papo em Tempo Real**: Envio e recebimento de mensagens instantâneas via WebSockets.
