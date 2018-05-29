# Dicas

## Evitando requests desnecessários para o servidor

Sempre que você pegar algum dado via Server Side Render, lembre-se de no **componentDidMount\(\)** fazer uma validação para caso o componente tenha os dados via props ou estado na hora que a página carrega ele não faz nada, do contrario dispara um fetch para a sua API para pegar os dados:

![](../.gitbook/assets/image%20%284%29.png)



