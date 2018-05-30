# Como lidar com autenticação?

O React Charger não possui um padrão para autenticação. O que o projeto oferece é um suporte para caso você precise ter acesso a um token do usuário ou algo do gênero no lado do back-end por meio da função **getInitialData\(\)**

![](.gitbook/assets/image%20%289%29.png)

É possível acessar um parâmetro que resgata as informações do request feito, e como essa função roda no lado do server, caso seja necessário algum token para pegar alguma info do usário na sua aplicação é recomendado que esse token fique armazenado em um cookie para facilitar o acesso a informação no lado do server e do front.

