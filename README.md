# Sumário
 
 - [Introdução](#maslow)
 - [Mobile](#app-react-native)
 - [Página Institucional](#pag-institucional)
 - [Aplicação](#maslow-app)
 - [API](#maslow-api)
 - [Integrantes](#integrantes)
 
# Maslow

A saúde mental desempenha um papel crucial no bem-estar geral das pessoas, e sua importância tem sido cada vez mais reconhecida em um mundo marcado por desafios únicos, como o impacto das redes sociais e o sedentarismo. Diante desse cenário, é fundamental a existência de uma aplicação que não apenas reconheça, mas também aborde ativamente esses desafios, capacitando os usuários no gerenciamento e promoção eficaz de seu bem-estar emocional.

O Maslow é projetado como uma ferramenta integral para enfrentar os desequilíbrios emocionais causados por fatores modernos, como a constante exposição às redes sociais. Ao invés de apenas reconhecer os problemas, nosso aplicativo busca oferecer soluções práticas e personalizadas, alinhadas com as necessidades individuais de cada usuário.

Nossa aplicação não só acompanha o estado emocional diário dos usuários, mas também fornece recursos ativos para contrabalançar os impactos negativos. Desde exercícios de meditação guiada até estratégias específicas para lidar com o estresse digital visando ser um guia compassivo no caminho do equilíbrio emocional.

Além disso, reconhecendo o papel essencial da atividade física na saúde mental, o aplicativo incentiva a integração de hábitos saudáveis na rotina diária, promovendo assim uma abordagem completa para o bem-estar.

Por meio de uma interface intuitiva e acessível, o Maslow se torna uma aliada diária, oferecendo não apenas rastreamento e monitoramento, mas também recursos educativos, acesso a profissionais de saúde mental e a criação de uma comunidade de apoio.

Em um mundo cada vez mais digital buscamos não apenas prevenir e gerenciar desequilíbrios emocionais, mas também fornecer um espaço seguro e eficaz para os usuários fortalecerem sua resiliência emocional e alcançarem um estado de bem-estar duradouro. 
 
# Estrutura de pastas
## /app-react-native
Contém os arquivos necessários para rodar o projeto em react native da aplicação mobile
 
### Iniciar aplicação
 - Abra a pasta em um Ambiente de Desenvolvimento (ex: Visual Studio Code)
 - Certifique-se de que tenha o [Node.js](https://www.alura.com.br/artigos/como-instalar-node-js-windows-linux-macos?gclid=CjwKCAjw1YCkBhAOEiwA5aN4ASAemF6qwJklrTyYnpgA0IoEU_05CItBNrJP2DFtOd5e-DQkbcME3RoC3DEQAvD_BwE) e o [Expo](https://docs.expo.dev/get-started/installation/) instalados
 - Abra o terminal e siga os passos a seguir:
 
 ````
 cd (caminho até a pasta do projeto)
 ````
 ````
 npm install
 ````
 ````
 expo start
 ````
 
## /pag-institucional
Contém os arquivos necessários para abrir o projeto em HTML e Bootstrap da página institucional
 
### Iniciar aplicação
- Abra o arquivo `index.html` no seu navegador
- Contém os conteiners Docker com o backend do projeto em PHP e MySQL, alimentando uma API REST.
 
### Iniciar aplicação
- Abra a pasta em um Ambiente de Desenvolvimento (ex: Visual Studio Code)
 
- ### Iniciando pelo servidor Apache:
  - Certifique-se de que tenha o [Xampp](https://www.apachefriends.org/pt_br/download.html) instalado.
  - Abra o Xampp Control Painel e inicie o serviço Apache e MySQL
  - Transfira a pasta `/pag-institucional` para a pasta `C:\xampp\htdocs\`
 
  - #### Criando o banco
    - Acesse esse [link](http://localhost/phpmyadmin/) em seu navegador
    - Acesse a opção "Importar" no menu e suba o arquivo `db.sql` que está na pasta `/src`
   
  - #### Acessando o sistema
    - Acesse esse [link](http://localhost/pag-institucional/src/) em seu navegador 
    - Se cadastre e após isso efetue o login ou efetue o login com as credenciais: email: `admin@fiap` e senha: `admin` 
 
- ### Iniciando pelo Docker:
[Link](https://hub.docker.com/r/rafaelaurichi/php-apache) para o repositório da imagem no `Docker Hub` 
 
  - Certifique-se de que tenha o [Docker](https://www.docker.com/products/docker-desktop/) instalado.
  - Abra o Docker Desktop e inicie o serviço
  - Abra o terminal e siga os passos a seguir:
   
  ````
  cd (caminho até a pasta do projeto)
  ````
  ````
  docker-compose up
  ````
 
  - #### Criando o banco
    - Acesse esse [link](http://localhost:8080) em seu navegador
    - Efetue o login no PHPMyAdmin
    - Acesse a opção "Importar" no menu e suba o arquivo `db.sql` que está na pasta `/src`
 
  - #### Acessando o sistema
    - Acesse esse [link](http://localhost) em seu navegador
    - Se cadastre e após isso efetue o login ou efetue o login com as credenciais: email: `admin@fiap` e senha: `admin` 
 
### API de autenticação
Para receber um retorno de autenticação de algum usuário é necessário que esteja com o projeto da pasta `/backend` rodando e realizar uma requisição do método `POST` para essa [URL](http://localhost/backend/src/api/usuario-existente.php) (caso esteja usando Xampp) ou para esta [URL](http://localhost/api/usuario-existente.php) (caso esteja usando Docker) e passar as seguintes informações:
 
````json
{
    "email": "(email do usuário)",
    "senha": "(senha do usuário)"
}
````
 
O retorno deve ser:
 
````json
{
    "id": " ",
    "nome": " ",
    "email": " ",
    "senha": " ",
    "telefone": " ",
    "sexo": " ",
    "data_nasc": " ",
    "cidade": " ",
    "estado": " ",
    "endereco": " "
}
````
 
## /maslow-app
(o que contém na pasta)
 
### Iniciar aplicação
- Abra a pasta em um Ambiente de Desenvolvimento (ex: Visual Studio Code)
 
- ### Iniciando pelo servidor Apache:
  - Certifique-se de que tenha o [Xampp](https://www.apachefriends.org/pt_br/download.html) instalado.
  - Abra o Xampp Control Painel e inicie o serviço Apache e MySQL
  - Transfira a pasta `/pag-institucional` para a pasta `C:\xampp\htdocs\`
 
  - #### Criando o banco
    - Acesse esse [link](http://localhost/phpmyadmin/) em seu navegador
    - Acesse a opção "Importar" no menu e suba o arquivo `db.sql` que está na pasta `/src`
   
  - #### Acessando o sistema
    - Acesse esse [link](http://localhost/pag-institucional/src/) em seu navegador 
    - Se cadastre e após isso efetue o login ou efetue o login com as credenciais: email: `admin@fiap` e senha: `admin` 
 
- ### Iniciando pelo Docker:
[Link](https://hub.docker.com/r/rafaelaurichi/php-apache) para o repositório da imagem no `Docker Hub` 
 
  - Certifique-se de que tenha o [Docker](https://www.docker.com/products/docker-desktop/) instalado.
  - Abra o Docker Desktop e inicie o serviço
  - Abra o terminal e siga os passos a seguir:
   
  ````
  cd (caminho até a pasta do projeto)
  ````
  ````
  docker-compose up
  ````
 
  - #### Criando o banco
    - Acesse esse [link](http://localhost:8080) em seu navegador
    - Efetue o login no PHPMyAdmin
    - Acesse a opção "Importar" no menu e suba o arquivo `db.sql` que está na pasta `/src`
 
  - #### Acessando o sistema
    - Acesse esse [link](http://localhost) em seu navegador
    - Se cadastre e após isso efetue o login ou efetue o login com as credenciais: email: `admin@fiap` e senha: `admin` 
 
### API de autenticação
Para receber um retorno de autenticação de algum usuário é necessário que esteja com o projeto da pasta `/backend` rodando e realizar uma requisição do método `POST` para essa [URL](http://localhost/backend/src/api/usuario-existente.php) (caso esteja usando Xampp) ou para esta [URL](http://localhost/api/usuario-existente.php) (caso esteja usando Docker) e passar as seguintes informações:
 
````json
{
    "email": "(email do usuário)",
    "senha": "(senha do usuário)"
}
````
 
O retorno deve ser:
 
````json
{
    "id": " ",
    "nome": " ",
    "email": " ",
    "senha": " ",
    "telefone": " ",
    "sexo": " ",
    "data_nasc": " ",
    "cidade": " ",
    "estado": " ",
    "endereco": " "
}
````

## /maslow-api
 
# Integrantes
 
 - Rafael Dias Aurichi 96169
 - Bruno Roberto 95757
 - David Almeida 96033

