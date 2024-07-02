# Operações matemáticas básicas

<div style="text-align: justify">

```{admonition} Lembrete
:class: tip
Ao ver `>>>`, estamos executando o código no terminal, por isso o `print()` não se faz necessário.

Caso queira experimentar o código em script (arquivos `.py`), é necessário imprimir a saída na tela.
```

## Comentários

```{admonition} Nota 
:class: note
O trecho abaixo é uma adaptação desta seção [3. Uma introdução informal ao Python](https://docs.python.org/pt-br/3/tutorial/introduction.html#an-informal-introduction-to-python) da documentação oficial. Fiz alguns pequenos ajustes no texto e nos exemplos com objetivo de torná-lo mais simples e compreensível
```

> Muitos exemplos neste livro, mesmo aqueles no terminal, incluem comentários. Comentários em Python começam com o caractere cerquilha `#` e estende até o final da linha. Um comentário pode aparecer no inicio da linha ou após espaço em branco ou código, mas não dentro de uma string. O caracterer cerquilha dentro de uma string é apenas uma cerquilha, um texto comum. Como os comentários são para esclarecer o código e não são executados pelo Python, eles podem ser omitidos ao digitar exemplos.
>
> 
> Alguns exemplos:
```python
# este é apenas um comentário que aparece no início da linha
spam = 1  # e este é um comentário que aparece depois de um código
          # ... e agora um terceiro comentário!
text = "# Este trecho não é um comentário, mas sim uma string, pois está entre aspas duplas, apesar de começar com cerquilha"
```

## As várias operações matemáticas

```{admonition} Nota 
:class: note
Este é um **livro de Python** e não de matemática! Portanto, parto do princípio que você entenda matemática básica para seguir com o livro.

Se achar necessário, posso esclarecer alguuns tópicos em específico. Mas, no geral, não haverá explicações de conceitos matemáticos.
```

Com Python é possível realizar operações como soma, subtração, multiplicação, divisão comum, divisão inteira (ou quociente da divisão), resto da divisão, potenciação e radiciação.

Cada operação tem seu chamado operador, que são, para:
- Soma: `+`
- Subtração: `-`
- Multiplicação: `*`
- Divisão comun: `/`
- Divisão inteira (ou quociente da divisão): `//`
- Resto da divisão: `%`
- Potenciação: `**` ou função `pow()`
- Radiciação: potenciação de uma fração `**(1/2)`

Vamos à exemplos!

```python
print(5 + 4)        # Soma de 5 com 4: 9
print(5 - 6)        # Subtraçaõ de 5 e 6: -1
print(10 * 20)      # Multiplicação entre 10 e 20: 200
print(4 / 2)        # Divisão comum entre 4 e 2: 2.0
print(50 // 30)     # Divisão inteira entre 50 e 30: 1
print(50 % 30)      # Resto da divisão entre 50 e 30: 20
print(2 ** 3)       # 2 elevado à 3: 8
print(16 ** (1/2))  # Raiz quadrada de 16: 4
```

Ao executar o código acima, você verá a seguinte saída (observem que os comentários foram ignorados pelo Python):
```
9
-1
200
2.0
1
20
8
4.0
```

Reparem que duas operações retornaram um valor com `.` no meio. O que significa isso? E o que estas duas operações tem de diferente?

## Os tipos de dados numéricos

</div>
