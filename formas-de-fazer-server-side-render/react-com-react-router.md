---
description: >-
  OBS: Essa parte pode ser melhorada caso tenhamos disponível uma CLI para gerar
  os projetos
---

# React com React Router

O React Charger foi criado pensando em utilizar Redux por padrão. Porém em projetos que não utilizem é perfeitamente possível trabalhar com o React Charger.

## Configurações

Primeiramente, você deve baixar o projeto neste link: [https://github.com/omariosouto/react-charger-razzle](https://github.com/omariosouto/react-charger-razzle)

Após ter baixado, deve comentar os códigos referentes ao Redux:

#### ./src/client.js

![](../.gitbook/assets/image%20%285%29.png)

#### 

#### ./src/server/index.js

![](../.gitbook/assets/image%20%283%29.png)



Após comentar os códigos do Redux, seu arquivo **./src/pages/Home/index.js** deve estar com o seguinte código:

{% embed data="{\"url\":\"https://gist.github.com/omariosouto/6cf2bd72fa1bd6b33a6dedb9d525a605\",\"type\":\"rich\",\"title\":\"React Charger: React + React Router\",\"description\":\"React Charger: React + React Router · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars1.githubusercontent.com/u/13791385?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\\"text/javascript\\\" src=\\\"https://gist.github.com/6cf2bd72fa1bd6b33a6dedb9d525a605.js\\\"></script>\",\"aspectRatio\":0}}" %}

## Como funciona/fazer o Server Side Render?

* Quando a URL **"/"**  for acessada o servidor irá pegar o componente **&lt;Home&gt;**
* O servidor irá resolver todos os **fetchs** dentro do objeto retornado pelo método **getInitialData\(\)**;
* Após pegar os dados iniciais, o servidor irá gerar a versão inicial da sua aplicação injetando os dados dinâmicos por meio do atributo no props do seu componente `props.staticContext`
* Já no lado do client, você terá acesso aos dados dinâmicos por meio de `window.__PRELOADED_STATE__`
* É importante ressaltar que o importante é que você use esses dois valores no construtor do seu componente e decida como preencher o state inicial da aplicação em cada lado. Um código bem comum é o do exemplo abaixo:

{% embed data="{\"url\":\"https://gist.github.com/omariosouto/a507075896d606c678abd79803143098\",\"type\":\"rich\",\"title\":\"constructorReactPure.js\",\"description\":\"constructorReactPure.js · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars1.githubusercontent.com/u/13791385?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\\"text/javascript\\\" src=\\\"https://gist.github.com/a507075896d606c678abd79803143098.js\\\"></script>\",\"aspectRatio\":0}}" %}



