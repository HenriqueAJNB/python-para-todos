<div style="text-align: justify">

(windows)=
# Windows

Direto e reto, siga todas as instruções sem pular etapas!

## Passo 1: baixar o instalador do Python

- Navegue até <a href="https://www.python.org/downloads/" target="_blank">página oficial de download do Python</a>
- Baixe o instalador clicando no botão de download do Python.

```{admonition} Recomendação de leitura
:class: note
O site geralmente oferece a versão mais recente, como *Python 3.x.x*.
Saber detalhes sobre a versão é importante, se quiser saber mais a fundo (eu recomendo!) consulte a seção [qual versão do Python devo instalar](python-version)
```

## Passo 2: executar o instalador

- Localize o arquivo baixado (normalmente na pasta "Downloads") e clique duas vezes para abrir.
- Marque a opção **Add python.exe to PATH** conforme item (1) da {ref}`imagem abaixo <python-setup>`.

```{admonition} Atenção
:class: danger
Caso você não marque a opção **Add python.exe to PATH** você terá erros no futuro!
```

- Clique em *Install now* conforme item (2) da {ref}`imagem abaixo <python-setup>`
- Aguarde a instalação ser concluída (pode demorar alguns minutos).

```{image} ../img/cap01/sec01/python-add-to-path.png
:width: 500
:name: python-setup
```

## Passo 3: verificando a instalação

- Abra o prompt de comando (busque por `cmd` na barra de busca do Windows)
- No prompt de comando (tela preta que abriu), digite `python --version` e pressione Enter. Você deve ver a versão do Python instalada impresa no terminal, conforme abaixo, confirmando que o Python foi instalado com sucesso! Parabéns!

```bash
Microsoft Windows [Version 10.0.22631.3810]
(c) Microsoft Corporation. All rights reserved.

C:\Users\Administrator>python --version
Python 3.11.9
```

- Digite `python` no prompt de comando para entrar no interpretador do Python.
```
Python 3.11.9 (tags/v3.11.9:6abddd9, Feb  6 2024, 21:26:36) [MSC v.1937 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

```{admonition} Dica
:class: tip
Estas três flechas `>>>` indicam que você está no interpretador do Python. 
Todo e qualquer comando digitado a partir de agora já será um comando da linguagem Python.

Para sair do interpretador e retornar ao prompt de comando, digite `exit()`. 

E para abrir o interpretador novamente, digite `python`
```

</div>