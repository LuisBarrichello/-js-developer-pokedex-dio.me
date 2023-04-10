# API, REST e RESTFUL

## API
Acronimo de Application Programming Interface (Interface de
Programação de Aplicações) é basicamente um conjunto de
rotinas e padrões estabelecidos por uma aplicação, para que
outras aplicações possam utilizar as funcionalidades desta
aplicação.
No contexto de APIs, a palavra Aplicação refere-se a qualquer software com uma função distinta. A interface pode ser pensada como um contrato de serviço entre duas aplicações.
• Responsável por estabelecer comunicação entre diferentes serviços.
• Meio de campo entre as tecnologias.
• Intermediador para troca de informações.


## REST
Um acrônimo para Representational State Transfer (
Transferência de Estado Representativo).

Será feita a transferência de dados de uma maneira simbólica,
figurativa, representativa, de maneira didática.

A transferência de dados, geralmemte, usando o protocolo HTTP.

O Rest, delimita algumas obrigações nessas transferências de dados.

Resources seria então, uma entidade, um objeto.

trata-se de um conjunto de princípios e definições necessário para a criação de um projeto com interfaces bem definidas.

É, na verdade, uma abstração da arquitetura da Web

A arquitetura Rest permite a comunicação entre aplicações.

##### Diferença entre Rest e Restful
Rest: é um conjunto de princípios de arquitetura.
Restful: é uma condição única de aplicar os conceitos de Rest.

##### Requisições e comunicações
Um requisição consiste em:

- **Um verbo ou método HTTP**, que define que tipo de operação o servidor vai realizar;
- **Um header**, com o cabeçalho da requisição que passa informações sobre a requisição;
- **Um path** (caminho ou rota) para o servidor;
- **Informação no corpo da requisição**, sendo esta informação opcional.

##### Métodos HTTP
Em aplicação REST, os métodos mais utilizados são:

- O **método GET** é o método mais comum, geralmente é usado para solicitar que um servidor envie um recurso;
- O **método POST** foi projetado para enviar dados de entrada para o servidor. Na prática, é frequentemente usado para suportar formulários HTML;
- O **método PUT** edita e atualiza documentos em um servidor;
- O **método DELETE** que como o próprio nome já diz, deleta certo dado ou coleção do servidor.

Neste link você encontrará a lista completa de todos os métodos.

##### Códigos de Respostas
Cada resposta que a aplicação REST retorna, é enviado um código definindo o status da requisição. Por exemplo:

- 1xx: Informação
- 2xx: Sucesso
  - 200 (OK), requisição atendida com sucesso;
  - 201 (CREATED), objeto ou recurso criado com sucesso;
  - 204 (NO CONTENT), objeto ou recurso deletado com sucesso;
- 3xx: Redirection
- 4xx: Client Error
  - 400 (BAD REQUEST), ocorreu algum erro na requisição (podem existir inumeras causas);
  - 404 (NOT FOUND), rota ou coleção não encontrada;
- 500 (INTERNAL SERVER ERROR), ocorreu algum erro no servidor.

Estes são os principais, porém neste link você encontrará a lista completa do código de cada requisição.

### 6 Necidades (constraints) para ser RESTful
- _Cliente-server_: Separação do cliente e do armazenamento de dados (servidor), dessa forma, poderemos ter uma portabilidade do nosso sistema, usando o React para WEB e React Native para o smartphone, por exemplo.

- _Stateless_: Cada requisição que o cliente faz para o servidor, deverá conter todas as informações necessárias para o servidor entender e responder (RESPONSE) a requisição (REQUEST). Exemplo: A sessão do usuário deverá ser enviada em todas as requisições, para saber se aquele usuário está autenticado e apto a usar os serviços, e o servidor não pode lembrar que o cliente foi autenticado na requisição anterior.

- _Cacheable_: As respostas para uma  equisição, deverão ser explicitas ao dizer se aquela resquição, pode ou não ser cacheada pelo cliente.

- _Layered System_: O cliente acessa a um ((ou “ponto de extremidade”) é um componente de uma rede de segurança ou de uma aplicação/API, como um dispositivo (notebook e celular, por exemplo) conectado a essa rede.), sem precisar saber da complexidade, de quais passos estão sendo necessários para o servidor responder a requisiçao, ou quais outras camadas o servidor estará lidando, para que a requisição seja respondida.

- _Code on demand (optional)_: Dá a possibilita da nossa aplicação pegar códigos, como o javascript, por exemplo, e executar no cliente;

## RESTFUL
- RESTful, é a aplicação dos padrões REST.

## BOAS PRÁTICAS
- Utilizar verbos HTTP para nossas requisições.
- Utilizar plural ou singular na criaçao dos endpoints? _Não importa_! Use um padrão.
- Não deixar barra no final do endpoint.
- Nunca deixe o client sem resposta.