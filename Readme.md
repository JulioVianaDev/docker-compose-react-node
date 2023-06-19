# Projeto de um fullStack app (nodejs,mongodb,react) dockerizado

### O projeto consiste em um simples crud usando a rede interna do docker-compose para conectar e dockerizar todo o setup de aplicação, para este projeto são criadas variaveis .env que deixei abertas apenas para fins educativos.

## Pré-requisitos

Certifique-se de ter os seguintes requisitos instalados em sua máquina:

- Docker
- Node.js (se você planeja desenvolver ou modificar o código da API)

## Configuração

1. Clone este repositório para o seu ambiente local.

2. Navegue até o diretório do projeto.

3. Crie um arquivo chamado `mongo.env` no diretório `env` e defina as variáveis de ambiente necessárias para o MongoDB. Por exemplo:

MONGO_INITDB_ROOT_USERNAME=max
MONGO_INITDB_ROOT_PASSWORD=secretpassword


4. Crie um arquivo chamado `backend.env` no diretório `env` e defina as variáveis de ambiente necessárias para a API Node.js. Por exemplo:

DB_HOST=mongodb
DB_PORT=27017
DB_NAME=mydatabase


Certifique-se de que o valor de `DB_HOST` seja definido como `mongodb`, pois esse é o nome do serviço do banco de dados no arquivo `docker-compose.yml`.

## Executando o Projeto

1. Abra um terminal e navegue até o diretório raiz do projeto.

2. Execute o seguinte comando para iniciar os contêineres do Docker:

docker-compose up


Este comando irá baixar as imagens necessárias, criar e iniciar os contêineres do MongoDB, da API Node.js e do frontend.

3. Após a inicialização bem-sucedida, você pode acessar a API Node.js em `http://localhost:80` e o frontend em `http://localhost:3000` no seu navegador.

## Estrutura do Projeto

- `docker-compose.yml`: O arquivo de configuração do Docker Compose que define os serviços do MongoDB, API Node.js e frontend, bem como suas dependências e volumes.

- `backend/`: O diretório contendo o código-fonte da API Node.js.

- `frontend/`: O diretório contendo o código-fonte do frontend.

- `env/mongo.env`: O arquivo que contém as variáveis de ambiente necessárias para o MongoDB.

- `env/backend.env`: O arquivo que contém as variáveis de ambiente necessárias para a API Node.js.

## Considerações Finais

Este projeto fornece um ambiente Dockerizado com MongoDB e uma API Node.js pronta para uso. Você pode modificar o código da API ou do frontend de acordo com suas necessidades.

Divirta-se usando o projeto! Se você tiver alguma dúvida ou problema, sinta-se à vontade para entrar em contato.
