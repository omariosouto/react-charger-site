# Lazy Loading de Componentes

O React Charger, usa por padrão um projeto chamado [React Loadable](https://github.com/jamiebuilds/react-loadable). Este projeto permite que seja possível carregar componentes React de forma assincrona. Isso é bem importante pois pode ajudar a melhorar a performance do seu projeto carregando determinadas rotas somente quando for necessário.

## Como utilizar?

Basta você fazer o import do React Loadable no arquivo que você deseja carregar um componente assincrono, invocar a função retornada pelo import passando um objeto com um loader \(arquivo que será carregado\) e um loading \(caso queria alguma coisa aparecendo antes do componente renderizar\) e pronto.

Isso se aplica tanto para rotas, quanto para trechos da sua página. Para utilizar segue um exemplo:

```javascript
import Loadable from 'react-loadable'

const AsyncAbout = Loadable({
 loader: () => import('./pages/About'),
 loading: () => null,
});

```

Para saber se deu certo, acesse a aba network do console, e devera aparecer vários arquivos JS com o nome **chunk:**

![](.gitbook/assets/image%20%288%29.png)



