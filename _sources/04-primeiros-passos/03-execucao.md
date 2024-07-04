# Formas de execução

<div style="text-align: justify">

Antes de proseguirmos com operações matemática, vale a pena entender como podemos executar nosso código.

## Executando script via VSCode

Na seção anterior, vimos que é possível executar um script usando o próprio VSCode. Lembre-se que scripts são um arquivo com comandos que quando executados rodam todos em sequência, linha a linha.

## Executando script via terminal

Mencionamos também que o VSCode executa o script através do terminal, e tivemos a seguinte saída quando executamos nosso primeiro script:

```bash
PS C:\Users\Administrator\Documents\personal\python-para-todos\scripts> & C:/Users/Administrator/AppData/Local/Programs/Python/Python312/python.exe c:/Users/Administrator/Documents/personal/python-para-todos/scripts/meu_primeiro_script.py
Olá mundo!
PS C:\Users\Administrator\Documents\personal\python-para-todos\scripts>
```

Vamos endender mais a fundo o que são estas mensagens a mais além do *Olá mundo!*, dividindo o comando em partes:

1. `C:\Users\Administrator\Documents\personal\python-para-todos\scripts>`: esta parte significa o caminho da pasta na qual estamos trabalhando. Lembra que a abrimos no VSCode? Pois bem, quando abrimos o terminal integrado no VSCode, ele já abre na pasta do projeto.

2. `C:/Users/Administrator/AppData/Local/Programs/Python/Python312/python.exe`: esta outra parte significa o caminho completo para o interpretador Python que está sendo usado para executar o nosso script. Reparem que é possível identificar inclusive qual é a versão do Python, no meu caso, a 3.12.

3. `c:/Users/Administrator/Documents/personal/python-para-todos/scripts/meu_primeiro_script.py`: finalmente, temos o caminho completo apontando para o script executado.

De uma forma bem mais simplificada, podemos executar o nosso script direto do terminal se entendermos o comando acima como uma combinação de `caminho do Python + caminho do script`. O caminho do Python não precisa ser colocado sempre de forma absoluta, como o VSCode faz. Se você seguiu todos os passos durante a instalação, em especial o passo de [marcar a opção **Add python.exe to PATH**](execute-installer), então você pode encurtar o caminho completo do Python simplesmente com o comando `python`!

Ou seja, `C:/Users/Administrator/AppData/Local/Programs/Python/Python312/python.exe` acaba virando apenas `python`. Vamos experimentar?

Para isso, temos 2 opções:

- Abrir o terminal integrado do VSCode: basta clicar em "Terminal > New Terminal" no menu superior do VSCode.
- Abrir o prompt de comando (cmd) fora do VSCode: fizemos isso na seção [Passo 3: verificando a instalação](checking-instalation) no capítulo de instalação do Python, lembra?

Ambos funcionam da mesma forma. A única diferença é que, caso você esteja com a pasta aberta no VSCode, o terminal se abre já na pasta do projeto. Caso contrário será preciso ou navegar até a pasta do script para executá-lo ou usar um caminho relativo entre a pasta atual e o script.

Quando eu abro o cmd, ele é aberto na pasta `C:\Users\Administrator>`. Desta pasta, podemos:
- Ou apontar para o script a partir da pasta atual. Desta forma o script será executado diretamente.
```bash
C:\Users\Administrator>python Documents/personal/python-para-todos/scripts/meu_primeiro_script.py`
```

- Ou navegar até a pasta do script com o comand `cd`, e, em seguida, executar o script:
```bash
C:\Users\Administrator>cd Documents/personal/python-para-todos/scripts

C:\Users\Administrator\Documents\personal\python-para-todos\scripts>python meu_primeiro_script.py
Olá mundo!

C:\Users\Administrator\Documents\personal\python-para-todos\scripts>
```

Ambas as formas acima são válidas. A segunda, porém, é mais utilizada.

## Executando comandos isolados via interpredador do Python

Uma outra forma de executar nosso código é usando o interpretador do Python. Aqui não estamos falando de executar um script com uma sequência de comandos, mas sim rodar comandos isolados. Vamos entender melhor.

Na seção [Passo 3: verificando a instalação](checking-instalation) no capítulo de instalação do Python vimos como abrir o interpretador do Python simplesmente digitando `python` no terminal. O interpretador estará ativo quando as três flechas `>>>` aparecerem na tela.

Podemos agora replicar o comando `print("Olá mundo!")` no interpretador que a mensagem será impressa na tela e o nosso código será executado.

## Qual a diferença, afinal de contas? 🤔

Quando executamos um script, ele roda **todos os comandos em sequência** enquanto que rodar via interpretador do Python requer a execução de cada um dos comandos praticamente de forma manual. Imagine agora ter que rodar um programa com 100 linhas no interpretador, rodando uma a uma...

💬 *Então você está dizendo que o interpredar é ruim, e nunca devemos usá-lo, certo?* 💬

**Não!** O interpretador é uma forma simplificada de rodar comandos de forma rápida e, sem necessidade de pensar em caminhos de arquivos e caminho do Python. É só uma forma diferente com suas peculiaridades para executar código. Nem melhor, nem pior.

O interpretador é tão simplificado na execução de códigos que nem requer o uso de `print()` para imprimir algo na tela. A saída de todos os comandos já são impressas automaticamente. Eu poderia simplesmente rodar o código retirando a função `print()` no interpretador que funcionaria do mesmo jeito.

```bash
>>> print("Olá mundo!")
Olá mundo!
>>> "Olá mundo!"
'Olá mundo!'
```

Porém, se eu fizesse o mesmo no script, ele não imprimiria nada na tela. Faça o teste, remova o `print()` do seu script, deixando somente a string `"Olá mundo!"` e execute!

Vamos agora aprender sobre operações matemáticas em Python!

</div>