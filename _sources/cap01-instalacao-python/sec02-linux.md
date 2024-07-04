(linux)=
# Linux

<div style="text-align: justify">

O Python no Linux é instalado via comandos no terminal. Você pode abrir o terminal através do atalho `Ctrl + Alt + T`. 

Os sistemas Linux mais recentes ja possuem uma versão do Python instalada junto com o sistema operacional. Para verificar se o seu sistema já o tem instalado, digite:

```bash
henrique@ubuntu:~$ python3 --version
Python 3.10.6
```

Caso você veja a versão do Python no terminal, significa que ele já está instalado.

```{admonition} Atenção
:class: danger
O Python que vem por padrão instalado é o Python do sistema operacional. Ao manipular este Python, você corre o risco de corromper o seu sistema operacional. Por isso não vamos usar esta versão, e sim instalar outra, justamente para isolar o Python do sistema operacional.
```

## Comandos para instalação

Para instalar outra versão do Python no Linux, digite os seguintes comandos, explicados em sequência:

```bash
sudo apt-get install software-properties-common
```

```{admonition} Em caso de erro
:class: warning
Caso se depare com esta mensagem de erro `usuario is not in sudoers file. This incident will be reported.`, vá para a seção [Erro comum - permissão de admin](common-error-linux).
```

O `software-properties-common` é um pacote no Linux que facilita a adição de novos repositórios de software, que são como lojas onde você pode baixar e instalar novos programas. Nós o usamos para instalar programas que não estão nas "lojas" padrão do seu sistema. Isso inclui versões mais recentes ou específicas de software, como o Python.

A instalação de outras versões do Python no Linux se dá através de um PPA. Os PPAs (Personal Package Archives) são repositórios de software criados por usuários ou desenvolvedores. Eles permitem que você instale programas e atualizações que não estão disponíveis nos repositórios oficiais do seu sistema Linux.

Para o Python, há um PPA chamado deadsnakes, cujo site oficial você encontra [aqui](https://launchpad.net/~deadsnakes/+archive/ubuntu/ppa). Você precisa dizer ao seu sistema onde encontrar essa nova "loja" de software e podemos fazer isso com o comando abaixo: 

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
```

E, finalmente, estamos prontos para instalar o Python:

```bash
sudo apt-get install python3.12
```

```{admonition} Nota sobre versões do Python
:class: note
Neste caso em específico estamos instalando a versão 3.12.
Saber detalhes sobre a versão é importante, se quiser saber mais a fundo (eu recomendo!) consulte a seção [qual versão do Python devo instalar](python-version)
```

(common-error-linux)=
## Erro comum - permissão de admin

O `sudo` sudo é um comando no Linux que permite que você execute ações como administrador. Pense nele como um superpoder temporário que dá a você permissão para fazer mudanças importantes no sistema. Caso você, ao executar alguns dos comandos com `sudo`, se depare com o erro...

```bash
usuario is not in sudoers file. This incident will be reported.
```

... significa que seu usuário não tem permissão de administrador do seu computador. Aqui existem 2 situações:

**Você realmente não tem permissão**. Normalmente é o caso de computadores de empresas com governança e restrições de acesso por questões de segurança.
```{admonition} Atenção
:class: danger
Se for este seu caso, **não dê sequencia com os passos abaixo!** Recomendo envolver alguém da sua empresa para dar suporte na instalação do Python sem ferir as políticas de segurança e governança da sua empresa.
```

**Seu usuário não foi alocado como administrador da máquina**, caso muito comum em máquinas pessoais. Neste caso você mesmo consegue resolver, conforme os passos abaixo:

- Entre no modo administrador
```bash
su root
``` 

- Abra o arquivo `sudoers` para colocar seu usuário como admin
```
nano /etc/sudoers
```

```{admonition} Consultando seu usuário
:class: tip
Se você não souber o seu nome de usuário, digite o comando `whoami` no terminal.
```

- Coloque este trecho no final do arquivo, substituindo `<seu-usuario>` pelo seu nome de usuário
```text
<seu-usuario> ALL=(ALL) ALL
```

- Pressione `Ctrl + O` para salvar o arquivo e `Ctrl + X` para sair.
  
- Feche o terminal e abra-o novamente. O problema foi resolvido e a mensagem de erro não deverá mais aparecer!

</div>
