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


### Exemplo 1

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

E podemos usar estas variáveis para criar uma outra variável, e imprimir uma mensagem na tela.

(exemplo-2)=
### Exemplo 2

```python
idade = 25
nome = "Henrique Branco"
mensagem = f"Meu nome é {nome} e tenho {idade} anos."
print(mensagem)
```

No exemplo acima, reparem no `f` logo antes do `"` na variável `mensagem`, e reparem também que as variáveis usadas para criar o texto da mensagem estão entre `{}`.

Isso é o que chamamos de f-strings em Python. São uma maneira de tornar um texto mais dinâmico usando variáveis e expressões dentro dele. Como a variável `nome` é um texto fixo e não depende de outras variáveis, não há necessidade do `f` antes de abrir o texto com `"` ou `'`. Vamos ver f-strings mais a fundo futuramente.

## Comportamento

### Declaração antes do uso

Pra usarmos uma variável, ela precisa ser criada antes. Caso contrário, o Python não reconhece o que não foi declarado. Vide, por exemplo, o exemplo simples:

```python
nome = "Henrique Branco"
mensagem = f"Meu nome é {nome} e tenho {idade} anos."
print(mensagem)
```

Ao executar, teremos um erro, pois a variável idade não foi definida antes de ser usada:
```bash
    mensagem = f"Meu nome é {nome} e tenho {idade} anos."
                                            ^^^^^
NameError: name 'idade' is not defined
```

### Case sensitive

Variáveis em Python são case-sensitive. Em outras palavras mais simples, elas são sensíveis à letras maiúsculas e minúsculas. Por isso, as variáveis `nome`, `Nome`, e `NOME` são diferentes. Veja o que acontece se declararmos a variável de uma forma e usarmos ela de outra:

```python
nome = "Henrique Branco"
print(Nome)
```

Ao executar o código acima:

```bash
    print(Nome)
          ^^^^
NameError: name 'Nome' is not defined. Did you mean: 'nome'?
```

(regras-nomenclatura-variaveis)=
## Regras na nomenclatura de variáveis

Estas regras são **obrigatórias**. Sem seguí-las, seu código gera erros!

Na nomeação de variáveis, **podemos**:

1. Iniciar o nome da variável com uma letra (a-z, A-Z) ou um sublinhado (_);
2. Criar variáveis que contenham números após o primeiro caractere;
3. Misturar maiúsculas e minúsculas no nome da variável;

Por outro lado, **não podemos**:

1. Iniciar o nome da variável com um número;
2. Criar variáveis que contenham caracteres especiais como @, -, $, dentre outros, exceto sublinhado (_);
3. Ter espaço em branco no nome da variável;
4. Usar palavras reservadas do Python como nome de variáveis;

Vamos para exemplos:

### Nomes de variáveis válidos

- `usuario`
- `_saldo_inicial` 
- `QuantidadeDeProdutos`
- `modeloV2`
- `abc123`

### Nomes de variáveis inválidos

- `1cliente` (começa com um número)
- `123valor` (começa com um número)
- `endereco-email` (contém um caractere especial `-`)
- `@usuario` (contém um caractere especial `@`)
- `preco$` (contém um caractere especial `$`)
- `idade#` (contém um caractere especial `#`)
- `nome completo` (contém espaço em branco)
- `idade usuario` (contém espaço em branco)
- `print` (palavra reservada do Python)
- `int` (palavra reservada do Python)

## Boas práticas

Aqui são algumas orientações e recomendações. Diferente das regras, não é obrigatório seguí-las e ainda sim o código pode funcionar sem erros. Recomendo, porém, seguí-las sempre que possível, pois garante maior clareza, legibilidade e manutenção de quem for ler seu código no futuro. Vamos à elas:

- **Clareza e descritividade:** Escolha nomes que descrevam claramente o propósito e o conteúdo da variável. Evite abreviações obscuras ou acrônimos pouco conhecidos.

- **Consistência:** Mantenha um padrão na escolha de nomes ao longo do seu código. Isso facilita a compreensão e a manutenção por outros desenvolvedores (ou por você mesmo no futuro). Vamos falar sobre padrões e convenções de nomenclatura logo na sequência.

- **Evite nomes genéricos:** Nomes como `x`, `temp`, `n`, `i` ou `var` podem ser ambíguos e dificultar a compreensão do uso da variável. Prefira nomes específicos que refletem seu papel no contexto.

- **Tamanho adequado:** Nomes de variáveis devem ser concisos, mas não tão curtos que percam significado. Evite nomes excessivamente longos que possam complicar a leitura do código, como por exempo `data_na_qual_o_usuario_se_cadastrou_na_plataforma_pela_primeira_vez`.

## Padrões e convenções

Há várias convenções na criação do nome de variáveis de forma geral, e os padrões mais comuns são:

- `sneak_case`: todas as letras em minúsculas, e usa o `_` para separar as palavras
- `camelCase`: todas as palavras iniciam com letra maiúsculas exceto a primeira, sem espaços entre as palavras
- `PascalCase`: todas as palavras iniciam com letra maiúsculas, sem espaços entre as palavras
- `UPPERCASE`: todas as letras em maiúscula, usa o `_` para separar as palavras

A partir de agora, vamos adotar a convenção amplamente utilizada pela comunidade, `sneak_case`, para nomear nossas variáveis por agora.

Há casos em que usaremos `UPPERCASE` quando formos representar uma variável constante. Apesar de ser estranho dizer "variável constante", em programação isso é totalmente possível. Trata-se de uma variável que é definida, e seu valor não se modifica em nenhum momento durante a execução do programa. É bastante comum em matemática e física, nas quais temos valores constantes. O exemplo mais comum é o valor `PI` da matemática, que, seguindo nossa convenção, seria definido da seguinte forma:

```python
PI = 3.1415
```

E mais à frente veremos que a convenção para nomeação de classes é a `PascalCase`. Mas não se preocupe com isso por agora.

## Prática

Sugiro fazer os exercícios [4](exercicio-4) e [5](exercicio-5) da lista! Boa prática!

## Conclusão

Neste capítulo, exploramos o conceito de variáveis, que são fundamentais em qualquer linguagem de programação, inclusive Python. Compreendemos o que são variáveis de maneira básica e técnica, vimos como criar e usar variáveis através de exemplos práticos e discutimos as regras obrigatórias e boas práticas para nomear variáveis de forma eficiente e clara. Também aprendemos sobre diferentes convenções de nomenclatura e a importância de manter a consistência e a clareza nos nomes das variáveis.

Ao seguir essas diretrizes e práticas, seu código se tornará mais legível, compreensível e fácil de manter, tanto para você quanto para outros desenvolvedores que possam trabalhar com ele no futuro. No próximo capítulo, aprofundaremos mais sobre o tipo de dado textual chamado de `string`.

</div>