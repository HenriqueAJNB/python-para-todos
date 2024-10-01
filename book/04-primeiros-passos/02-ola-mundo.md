(hello-world)=
# Primeiro programa: Olá mundo!



No seu script, digite o seguinte código:

```python
print("Olá mundo!")
```

**Salve o seu script** pressionando Ctrl + S no teclado ou clicando em "File > Save" no menu superior do VSCode. 

Após salvá-lo, clique no botão "Run Python file" no canto superior direito da tela, conforme a imagem abaixo, para executá-lo.

```{image} ../img/04-02-run-python-file-icon.png
```

</br>Neste momento, o terminal integrado do VSCode se abre, e nele será possível ver nosso texto *Olá mundo!* impresso na tela.

```bash
PS C:\Users\Administrator\Documents\personal\python-para-todos\scripts> & C:/Users/Administrator/AppData/Local/Programs/Python/Python312/python.exe c:/Users/Administrator/Documents/personal/python-para-todos/scripts/meu_primeiro_script.py
Olá mundo!
PS C:\Users\Administrator\Documents\personal\python-para-todos\scripts>
```

```{admonition} Nota 1
:class: note
O terminal mostra algumas mensagens "estranhas" junto com `Olá mundo!`, mas elas têm um motivo. O VSCode executa um comando no prompt de comando para rodar nosso código. Essas mensagens extras são parte desse comando.
```

```{admonition} Nota 2
:class: note
O terminal é um programa usado no Linux e macOS para digitar e executar comandos. O prompt de comando é a versão do Windows para a mesma finalidade. Ambos permitem que você digite comandos e veja os resultados, mas são usados em sistemas operacionais diferentes.

No fundo, mesmo usando Windows, é bastante comum falar em terminal ao invés de prompt de comando.
```

## Explicação detalhada

Neste primeiro exemplo, apesar de simples, temos alguns detalhes pra você começar a entender mais a fundo sobre Python. Vamos tender mais a fundo?

### Entendendo cada parte

No código temos o seguinte:
- `print()`: Esta é uma função que já vem pronta na linguagem Python. A função `print` é usada para imprimir algo no terminal. Nos próximos capítulos entraremos mais no detalhe sobre funções.
- `"Olá mundo!"`: Esta é a mensagem que queremos que apareça na tela. As aspas duplas `"` são usadas para indicar que `"Olá mundo!"` é um texto. Todo text no mundo da programação são chamados de `string`. Também haverá um capítulo dedicados à `string`.

Agora que entendemos cada parte separada, vamos ver como elas se comportam todas juntas.
  
### Como funciona

- Quando você executa o programa, o Python executa o código linha a linha em sequência.
- Na única linha presente, o Python encontra a função `print`.
- Ele vê que dentro dos parênteses da função `print()` há um texto `Olá mundo!` entre aspas duplas `"`.
- Então, o Python mostra esse texto no terminal `Olá mundo`

### O resultado final

A mensagem `Olá mundo!` é exibida no terminal


## Prática

A esta altura do livro, você está apto a fazer o [exercício 1](exercício-1) proposto!

## Conclusão

Você acabou de criar e executar o seu primeiro programa em linguagem Python! Embora seja simples, já é um avanço enorme para quem saiu do zero! E perceba quanta coisa você já aprendeu!

Parabéns! Comemore se você chegou até aqui! 🤝🎉🙌🥳🤩

Na próxima seção vamos avançar com uma breve explicação sobre as diferentes formas de executar código. E, na sequencia, vamos começar a falar sobre operações matemáticas com Python.

