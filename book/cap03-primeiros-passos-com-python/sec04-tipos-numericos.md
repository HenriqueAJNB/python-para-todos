# Tipos de dados numéricos

<div style="text-align: justify">

Dentro do mundo da programação, nós temos os chamados tipos de dados, e nesta seção vamos falar de dois tipos de dados numéricos básicos: inteiros, representados por `int` e o ponto flutuante, também chamado de `float`, representando um número decimal.

## `float` e `int`

Conforme vimos na seção anterior, a divisão `4 / 2` retornou `2.0`, e não simplesmente `2`. Porque isso acontece?

As operações de soma e divisão de números inteiros, como `5 + 4` e `5 - 6` sempre resultam em valores inteiros, chamados de `int`.

Na divisão, porém, nem sempre. Podemos ter divisões que resultam em valores inteiros, `4 / 2` e outras não, como é o caso de `3 / 4`, que resulta em `0.75`. Como forma de generalizar, toda divisão em Python retorna um número decimal por padrão. Isso está escrito no tutorial da documentação oficial, seção [3.1.1. Numbers](https://docs.python.org/3/tutorial/introduction.html#numbers) no qual temos escrito (traduzido aqui no livro) que `# divisão sempre retorna um ponto flutuante`.

Portanto, temos os tipos `int`, representando um número inteiro, e o tipo `float` representando um número com casas decimais.

Na maioria das linguagens de programação, incluindo Python, a casa decimal é representada pelo ponto `.`.

A radiciação é outra operação que retorna valores `float` por padrão. Da seção passada, vimos que `16 ** (1/2)` nos trouxe `4.0` e não `4`.

Interessante que, embora matematicamente `2` e `2.0` sejam iguais, no mundo da programação, `2` e `2.0` são diferentes, pois estamos falando de um `int` e um `float`. 

## A função `type`

Na seção [Primeiro programa: Olá mundo!](hello-world) vimos nossa primeira função `print` que imprime uma mensagem no terminal. Vamos aprender uma segunda, a função `type`. 

A função `type` faz parte de um conjunto de funções nativas do Python. Você pode acessar a lista completa destas funções nativas [aqui](https://docs.python.org/3/library/functions.html). 

**Esta função vai te acompanhar no resto do livro**, acredite em mim! Ela é simples, e super importante. Lembrando que teremos uma seção específica sobre funções.

De acordo com a documentação oficial, esta função `type` retorna literalmente o tipo de algo passado para ela. Vamos vê-la na prática?

```python
print(type(4 / 2))
```

Ao executar o código acima, veremos `<class 'float'>` impresso no terminal, indicando que divisão sempre retorna um ponto flutuante, ou `float`.

Vamos entender a execução. Ela acontece "de dentro para fora".

1. O Python primeiro realiza a operação `4 / 2`, resultando em `2.0`
2. Este resultado é passado então para a função `type`, no qual teremos `type(2.0)`
3. A função `type`, por sua vez, retorna o tipo do que foi passado para ela, no caso, o tipo de dado do número `2.0`, um `float`.
4. Finalmente, o tipo do dado é impresso na tela: `<class 'float'>`

```{admonition} Grave isso!
:class: note
Quando eu perguntar ao longo do livro **como sei qual é o tipo de dado?**, a resposta sempre será: **usando a função `type`**!
```

Na próxima seção vamos aprender sobre a ordem na qual as operações são executadas!

</div>
