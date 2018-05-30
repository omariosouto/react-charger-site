# React com React Router e Redux

## Como fazer Server Render com Redux

O React Charger Razzle faz um mapeamento do objeto da sua store do Redux no servidor para facilitar o preenchimento dos dados para o carregamento inicial.

### Passo a passo

* Primeiro baixe o projeto conforme as instruções no tópico item:

{% page-ref page="../comecando-com-react-charger.md" %}

* Após baixar o projeto, caso queira manipular algo relacionado ao redu abra o arquivo **./src/store.js**, ****ele contém todas a lógicas para criar a sua store do Redux.

![](../.gitbook/assets/image%20%287%29.png)

* Sabendo desse arquivo, tudo começa pelo arquivo **./src/client.js** :

![](../.gitbook/assets/image%20%282%29.png)

* Esse arquivo possui a inicialização normal de uma aplicação React com Redux, porém ao criar a store da aplicação passamos como argumento para a store o valor contido em **window.\_\_PRELOADED\_STATE\_\_**, que nada mais é que o objeto que o servidor gera com os dados que ele irá pré-carregar para nossa aplicação.

## Como o servidor pré-carrega os dados?

Sempre que você quiser fazer alguma página ter conteúdo carregado por meio de Server Render, você deve colocar um método chamado **getInitialData\(\)** na classe do seu componente:

{% embed data="{\"url\":\"https://gist.github.com/omariosouto/ed46a94e47b5ab91d6d89032bb6049f6\",\"type\":\"rich\",\"title\":\"React Charger: getInitialData\(\)\",\"description\":\"React Charger: getInitialData\(\) · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars1.githubusercontent.com/u/13791385?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\\"text/javascript\\\" src=\\\"https://gist.github.com/ed46a94e47b5ab91d6d89032bb6049f6.js\\\"></script>\",\"aspectRatio\":0}}" %}

A chave 'repos' no objeto, possui esse nome pois o valor que for carregado ali irá preencher os dados no atributo 'repos' que temos na store do Redux.

### Fazendo os dados passarem da store para o Componente

No React Charger, uma das ideias é que você terá container components que irão pegar os dados que vieram de **window.\_\_PRELOADED\_STATE\_\_** e carregados na versão inicial da store e repassar como props para os componentes:

{% embed data="{\"url\":\"https://gist.github.com/omariosouto/2ecdcc6611ce6f182f0ca195a1c0b3c1\",\"type\":\"rich\",\"title\":\"containerComponentExample.js\",\"description\":\"containerComponentExample.js · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars1.githubusercontent.com/u/13791385?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\\"text/javascript\\\" src=\\\"https://gist.github.com/2ecdcc6611ce6f182f0ca195a1c0b3c1.js\\\"></script>\",\"aspectRatio\":0}}" %}



 

