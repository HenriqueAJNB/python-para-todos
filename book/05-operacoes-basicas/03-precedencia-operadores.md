(precedencia-operadores)=
# Precedência de operadores

<div style="text-align: justify">

Na seção anterior vimos várias operações matemáticas bem como os tipos de dados resultantes. Vamos agora aumentar a complexidade um pouco falando sobre precedência de operadores.

Basicamente a precedência de operadores é a ordem na qual as operações mais complexas são feitas.

Vamos entender melhor com um exemplo prático.

## A ordem das operações importa!

Qual seria o resultado desta operação em linguagem Python? Menos três elevado ao quadrado: `-3**2`

Que resultado você espera? Pare e execute esta operação antes de continuar a leitura. Executou? O resultado saiu conforme esperado?

Quando você executa esse código , surpreendentemente você obtém `-9` como resultado! 😱

Por que isso acontece? Vamos compreender melhor.

## Programação não é matemática

Bom, no mundo da matemática, aprendemos que...

> *Todo número negativo elevado ao quadrado resulta em um número positivo*

Mas então porque a operação `-3**2` resultou em `-9` e não `9`? O Python está em desacordo com a matemática então?

Na verdade, não! Programação e matemática são coisas distintas. E precisamos discernir isso.

O conceito mais simples de programação seria:

> Programação é como dar instruções para um robô ou computador fazer coisas. Você escreve uma lista de passos, como uma receita de bolo, e o robô ou computador segue esses passos para fazer o que você pediu.

Bom, no nosso programa, temos basicamente duas operações: `-` (subtração) e `**` (potenciação). Só que o nosso programa não é executado sempre na sequência linear de leitura, da esquerda para direita. Dependendo dos operadores, alguns podem ser executados antes de outros, como uma fila de prioridade. E é justamente o caso que acontece aqui.

(tabela-precedencia)=
## A tabela de precedência

| Operador                                                   | Descrição                                                                                       |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| (expressions...), [expressões...], {chave: valor...}, {expressões...} | Expressão entre parênteses ou de ligação, sintaxe de criação de lista, sintaxe de criação de dicionário, sintaxe de criação de conjunto |
| x[índice], x[índice:índice], x(argumentos...), x.atributo  | subscrição, fatiamento, chamada, referência a atributo                                          |
| await x                                                    | Expressão await                                                                                 |
| **                                                         | Exponenciação [5]                                                                               |
| +x, -x, ~x                                                 | positivo, negativo, NEGAÇÃO (NOT) bit a bit                                                     |
| *, @, /, //, %                                             | Multiplicação, multiplicação de matrizes, divisão, divisão pelo piso, resto [6]                 |
| +, -                                                       | Adição e subtração                                                                              |
| <<, >>                                                     | Deslocamentos                                                                                   |
| &                                                          | E (AND) bit a bit                                                                               |
| ^                                                          | OU EXCLUSIVO (XOR) bit a bit                                                                    |
| \|                                                         | OU (OR) bit a bit                                                                               |
| in, not in, is, is not, <, <=, >, >=, !=, ==               | Comparações, incluindo testes de pertinência e testes de identidade                             |
| not x                                                      | NEGAÇÃO (NOT) booleana                                                                          |
| and                                                        | E (AND) booleano                                                                                |
| or                                                         | OU (OR) booleano                                                                                |
| if - else                                                  | Expressão condicional                                                                           |
| lambda                                                     | Expressão lambda                                                                                |
| :=                                                         | Expressão de atribuição                                                                         |

*Fonte: seção [6.17. Precedência de operadores](https://docs.python.org/pt-br/3/reference/expressions.html#operator-precedence) da documentação oficial*

Esta tabela acima representa uma lista com todos os operadores do Python. Não se preocupe se ainda não vimos (e talvez não vamos ver todos mesmo) alguns da lista. Pra este momento o que você precisa saber o que eles fazem, somente consultar a ordem que eles aparecem. Vou deixar destacado e em negrito:

> Os operadores são executados na ordem **de cima para baixo**. Em outras palavras, **se tenho duas operações, a operação mais acima na tabela é executada primeiro**.

Caso eles estejam na mesma linha, dai a ordem passa a ser da esquerda para a direita (ordem de leitura comum).

Retornando à nossa expressão, reparem que a exponenciação `**` aparece antes da subtração (`-`) na tabela, sendo executada primeiro, portanto.

A ordem de execução do nosso programa então seria:

1. Eleva o três ao quadrado, `3**2`, resultando em `9`.
2. Aloca o sinal de `-` ao resultado acima, retornando `-9`.

Estão aprendendo que programação é uma execução de operações que não segue exatamente a ordem de leitura?

## Mas e a matemática então, como fica?

Bom, se quisermos que o nosso programa seja "compatível com a regra matemática", precisamos ser super explícitos, e usar a ordem de execução da tabela acima ao nosso favor.

Para nosso programa ser fiel ao que a matemática diz, não é o `3` que deve ser elevado ao quadrado, e sim o `-3`. E para forçarmos que esta operação de alocação do `-` ao `3` seja feita antes da operação de `**`, é necessario deixar explícito no programa da seguinte forma: `(-3)**2`. 

Observem que a primeira linha da tabela contém *expressões entre parênteses `()`*. Nós forçamos a execução da operação `-3` para ser executada antes de `**` colocando-a entre `()`.

E agora sim o nosso programa está compatível com a regra matemática. Mas percebam que a ordem das operações é que determinou a correção!

## Operadores com mesma precedência

Quando existem operadores com mesma precedência, eles são executados da esquerda para direita, na mesma ordem de leitura.

Um exemplo super simples: `1 + 2 - 5` é executado como `1 + 2` resultado em `3` e depois `3 - 5` resultado em `-2`. Do ponto de vista matemático, para este caso, a ordem de execução não importaria, pois se fizermos `2 - 5 = -3` e `-3 + 1 = -2`, o resultado seria o mesmo. 

Mas, quando chegarmos lá na frente com conceitos de programação pura, podemos nos deparar com a seguinte expressão como exemplo:

```python
imposto == "COFINS" and imposto in lista_de_impostos 
```

```{admonition} Nota
:class: note
Não se preocupe com o que você não aprendeu ainda, foque em conceitos específicos! Neste momento, o conceito é a **ordem da lista de precedência para execução das operações**
```

No código acima, temos 3 operações: `in`, `and` e `==`. Qual delas seria executada primeiro?

De acordo com a tabela de precedência:
1. `imposto == "COFINS"`
2. `imposto in lista_de_impostos`
3. E, por último, `and`

Porque o `==` é executado antes do `in`? Eles estão na mesma linha da tabela de precedencia dos operadores, e, neste caso, o que vale é a ordem que ele aparece na expressão. Como o `==` aparece primeiro que o `in`, ele é executado antes do `in`.

Do ponto de vista de regras de negócio, estamos verificando primeiro se o imposto é COFINS e depois se ele está presente em alguma lista de impostos. 

E se quiséssemos inverter tal regra ou verificação para verificar primeiro se o imposto está presente em uma lista de impostos, e somente depois, verificar se o imposto é COFINS?

Precisaríamos:
- ou inverter a ordem e deixar `imposto in lista_de_impostos` à esquerda:

```python
imposto in lista_de_impostos and imposto == "COFINS"
```

- ou colocar a expressão entre `()`:

```python
imposto == "COFINS" and (imposto in lista_de_impostos) 
```

## Prática

Recomendo você fazer o [exercício 3](exercício-3) da lista!

## Conclusão

Vimos a importância da ordem de execução dos operadores com vários exemplos didáticos e um exemplo real. Na próxima seção, vamos detalhar mais variáveis.

</div>
