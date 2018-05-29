# Formas de Fazer Server Side Render

Sempre que você quiser fazer Server Render de algum conteúdo, primeiramente você deverá colocar o método **getInitialData\(\)** em seu componente que representa a página que terá dados carregados pelo servidor:

{% embed data="{\"url\":\"https://gist.github.com/omariosouto/ed46a94e47b5ab91d6d89032bb6049f6\",\"type\":\"rich\",\"title\":\"React Charger: getInitialData\(\)\",\"description\":\"React Charger: getInitialData\(\) · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars1.githubusercontent.com/u/13791385?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\"text/javascript\\" src=\\"https://gist.github.com/ed46a94e47b5ab91d6d89032bb6049f6.js\\"></script>\",\"aspectRatio\":0}}" %}

Após isso, automaticamente quando a página carregar estará disponível no objeto window da sua página o atributo **\_\_PRELOADED\_STATE\_\_:**

![](../.gitbook/assets/image%20%286%29.png)

Para entender como você pode aproveitá-lo para conseguir fazer sua página vir com Server Render confira os links abaixo:

{% page-ref page="react-com-react-router-e-redux.md" %}

{% page-ref page="react-com-react-router.md" %}



