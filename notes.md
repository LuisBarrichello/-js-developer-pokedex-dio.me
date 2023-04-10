# Requisição HTTP

URL: https://pokeapi.co/api/v2/pokemon
${IP = endereço}/${path = caminho de identificação do recurso}

IP: https://pokeapi.co

Request Method: GET | POST | PUT | DELETE | PATCH
GER = BUSCAR | PUSH = INSERIR ALGO | PUT = ATULIZAR ALGO
Cada método tem sua finalidade específica e deve ser usado de acordo com as necessidades do desenvolvedor ou do aplicativo

## Path Params e Query String

PATH-PARAMES = passasr informaçoes obrigatórias em uma URL
URL: https://pokeapi.co/api/v2/pokemon/1
    "/1" ID  / PATH-PARAMES

QUERY-STRING = clausula where, um filtro p/ api
URL: https://pokeapi.co/api/v2/pokemon'?type=grass&name=i'

A query string é um conjunto de parâmetros que são adicionados ao final de uma URL, separados por um ponto de interrogação. Os parâmetros na query string são usados para transmitir informações opcionais para o servidor. Por exemplo, em uma URL como "https://www.exemplo.com/busca?q=termo-de-busca", o valor "termo-de-busca" é um parâmetro da query string chamado "q". O servidor pode usar esse valor para pesquisar por conteúdo relacionado.

Os path parameters, por outro lado, são usados para transmitir informações obrigatórias em uma URL. Eles são especificados como parte do caminho da URL e geralmente são separados por barras. Por exemplo, em uma URL como "https://www.exemplo.com/produtos/123", "produtos" é o caminho e "123" é um path parameter que representa o ID do produto solicitado. O servidor pode usar esse valor para buscar as informações do produto correspondente.
Em resumo, a query string é usada para enviar informações opcionais para o servidor, enquanto os path parameters são usados para enviar informações obrigatórias. Ambos são importantes para construir URLs únicas e personalizadas para cada solicitação.

pagina o filtro com querystring:
    https://pokeapi.co/api/v2/pokemon?offset=20&limit=20



## Request Header
Area de dados para receber e enviar dados;
descrever ou complementar a requisição;
especie de configuracao da nossa requisicao;

Response header: servidor respondendo a requisição
Request header: é a solicitação do cliente, no caso servidor


## Request Body e Status Code
#### Request Body
O body de uma requisição HTTP é a parte da mensagem da requisição que contém os dados enviados pelo cliente para o servidor. É como um "corpo" da requisição que pode conter informações como texto, JSON, XML, arquivos, imagens, etc.
O corpo da requisição é definido pelo tipo de mídia (media type) especificado no cabeçalho da requisição. Por exemplo, o tipo de mídia "application/json" indica que o corpo da requisição contém dados em formato JSON. O tipo de mídia "multipart/form-data" é usado para enviar arquivos e dados de formulário. 
Em resumo, o body de uma requisição HTTP é a parte da mensagem da requisição que contém os dados enviados pelo cliente para o servidor. Ele é usado principalmente em requisições POST, PUT e PATCH para enviar informações do cliente para o servidor.

#### Status Code
Ele informa ao cliente se a requisição foi bem-sucedida ou não, e também pode fornecer informações adicionais sobre o resultado da requisição.
Alguns dos códigos de status mais comuns incluem:

200 OK: A requisição foi bem-sucedida.
201 Created: A requisição foi bem-sucedida e um novo recurso foi criado.
400 Bad Request: A requisição não pôde ser entendida ou foi malformada.
401 Unauthorized: O cliente não forneceu credenciais válidas para acessar o recurso solicitado.
404 Not Found: O servidor não conseguiu encontrar o recurso solicitado.
500 Internal Server Error: O servidor encontrou um erro interno ao processar a requisição.


## Fetch API
#### Fetch API
Fetch API é uma interface web que permite que o cliente (geralmente um navegador da web) faça requisições HTTP para um servidor e obtenha a resposta em um formato legível por máquina, como JSON ou XML. A Fetch API é baseada em Promises, o que significa que as requisições são feitas de forma assíncrona, sem bloquear a execução do código.
A Fetch API fornece uma série de recursos avançados, como suporte nativo a Promises, opções de configuração mais flexíveis e uma sintaxe mais simples.
A sintaxe básica da Fetch API é a seguinte:

fetch(url, options)
  .then(response => {
    // processar a resposta
  })
  .catch(error => {
    // tratar erros
  });


O parâmetro url é a URL do servidor para o qual a requisição será enviada, enquanto options é um objeto que contém várias opções de configuração, como método HTTP, cabeçalhos e corpo da requisição.

A resposta do servidor é retornada como uma Promise, que pode ser manipulada usando os métodos then e catch. Dentro do bloco then, podemos processar a resposta do servidor, enquanto dentro do bloco catch, podemos lidar com quaisquer erros que possam ter ocorrido durante a requisição.


#### Processamento assincrono
o processamento assíncrono é uma técnica de programação que permite que um programa execute várias tarefas simultaneamente, sem bloquear a execução de outras tarefas. É feito por meio do uso de callbacks, Promises ou async/await e é particularmente útil quando temos tarefas que podem levar um tempo desconhecido para serem concluídas.

Promises
Promises são um recurso do JavaScript que permitem que as operações assíncronas sejam tratadas de maneira mais simples e organizada. Basicamente, uma Promise é um objeto que representa a eventual conclusão (ou falha) de uma operação assíncrona e permite que o código reaja a esse resultado de maneira síncrona.
Uma Promise tem três estados possíveis: pendente, resolvida e rejeitada. Quando uma Promise é criada, ela está no estado pendente. Isso significa que a operação assíncrona ainda não foi concluída.  Quando a operação é concluída com sucesso, a Promise é resolvida com um valor. Quando a operação falha, a Promise é rejeitada com um erro.


