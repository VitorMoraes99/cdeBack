📦 Controle de Estoque - Backend O backend desta aplicação fornece APIs para gerenciamento de estoque, autenticação e segurança. Ele foi desenvolvido para complementar o frontend disponível no repositório estoqueFront.

🚀 Tecnologias Utilizadas Node.js Express Banco de Dados: MySQL JWT para autenticação e segurança Bcrypt para criptografia de senhas 🌟 Funcionalidades 🔒 Autenticação segura com JWT e senhas criptografadas 🆕 API para CRUD de produtos (criar, editar, excluir, listar) 📦 Gestão eficiente do estoque com suporte para múltiplos produtos 🔧 Instalação e Execução

Clone o repositório: bash Copiar código git clone (https://github.com/VitorMoraes99/cdeBack)

Navegue até o diretório do projeto: bash Copiar código cd estoqueBack

Instale as dependências: bash Copiar código npm install

Configure as variáveis de ambiente no arquivo .env: env Copiar código DB_HOST=localhost DB_USER=seu_usuario DB_PASS=sua_senha DB_NAME=estoque JWT_SECRET=sua_chave_secreta

Inicie o servidor: bash Copiar código npm start 🐳 Usando Docker

Configure o arquivo .env Certifique-se de que as variáveis de ambiente estão devidamente configuradas no arquivo .env, como mostrado acima.

Crie um arquivo docker-compose.yml: yaml Copiar código version: "3.8" services: app: build: . ports:

"3000:3000" env_file:
.env depends_on:
db db: image: mysql:8 restart: always environment: MYSQL_ROOT_PASSWORD: root_password MYSQL_DATABASE: estoque MYSQL_USER: seu_usuario MYSQL_PASSWORD: sua_senha ports:
"3306:3306" volumes:
db_data:/var/lib/mysql volumes: db_data:
Inicie os serviços com Docker Compose: Execute o seguinte comando na raiz do projeto, onde o arquivo docker-compose.yml está localizado:

bash Copiar código docker-compose up --build 4. Acessar a aplicação: O backend estará disponível em http://localhost:3000. O banco de dados MySQL estará acessível na porta 3306.
