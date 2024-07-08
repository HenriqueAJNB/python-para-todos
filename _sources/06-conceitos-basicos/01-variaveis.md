# Variáveis

<div style="text-align: justify">

Em todos os códigos anteriores, você percebeu que nós não salvamos o valor da expressão em lugar nenhum do nosso código? Para salvar um valor durante a execução do código, podemos usar variáveis. Vamos falar sobre elas neste capítulo!

## O que são variáveis?

Vou responder a esta pergunta de duas formas:

### Conceito básico

Variáveis são como "caixinhas" onde você pode guardar informações para usar mais tarde no seu código. Cada caixinha tem um nome para você lembrar onde guardou a informação e pode conter diferentes tipos de informações, como números, palavras ou até mesmo listas de coisas.

### Definição técnica

Variáveis são nomes que você usa para guardar valores na memória do computador enquanto um programa está sendo executado. Elas permitem armazenar e acessar dados, como números e textos, para serem usados e manipulados ao longo do programa.

A melhor forma de entender isso é através de exemplos.

## Exemplos básicos

```python
idade = 25
nome = "Henrique Branco"
```

Neste exemplo acima, estamos criando uma variável chamada `idade` que armazena o número inteiro 25, e `nome` que armazena o texto `Henrique Branco`.

No fundo, é um espaço de memória que tem um nome e um valor associado, sendo possível acessar esse valor novamente no código através do nome usado na criação.

O nome da variável fica a escolha de quem desenvolve, embora existam regras obrigatórias e boas práticas na criação de nomes de variáveis.

```{admonition} Dica de ouro
:class: tip
Eu, particularmente, não gosto de ler esta linha como *variável idade igual a 25*, pois igualdade é uma comparação, se uma coisa é igual à outra. Na criação de variáveis, usando o `=`, estamos falando de uma alocação ou de uma atribuição. Então, eu sugiro você começar a ler esta linha como *atribui o valor 25 à variável idade*, ou então *variável idade recebe 25*. Mais a frente vamos aprender que existe também o operador de comparação `==`, que pode ser facilmente confundido com `=` se você não se atentar ao que eu disse aqui.
```

E podemos usar estas variáveis para criar uma outra variável, e imprimir uma mensagem na tela

```python
idade = 25
nome = "Henrique Branco"
mensagem = f"Meu nome é {nome} e tenho {idade} anos."
print(mensagem)
```

No exemplo acima, reparem no `f` logo antes do `"` na variável `mensagem`, e reparem também que as variáveis usadas para criar o texto da mensagem estão entre `{}`.

Isso é o que chamamos de f-strings em Python. São uma maneira de tornar um texto mais dinâmico usando variáveis e expressões dentro dele. Como a variável `nome` é um texto fixo, não depende de outras variáveis, não há necessidade do `f` antes dela.

</div>
