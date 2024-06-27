(python-version)=
# Qual versão do Python devo instalar?

<div style="text-align: justify">

Se você está começando agora, e tem um certo senso crítico e um perfil questionador, provavelmente você deve ter feito esta pergunta.

Esta seção é um guia geral para o ajudar a escolher a versão do Python a ser instalada, bem como descrever e detalhar o tópico sobre versões do Python.

Tudo bem também se você só instalou a versão mais recente.

```{admonition} Atenção
:class: danger
Recomendo que você leia este material ao menos para ter uma noção geral do tema, pois versões diferentes do Python é a causa raiz de muitos problemas!
```

## Compatibilidade com sistema operacional

Conforme os desenvolvedores e mantenedores do Python avançam, cada versão nova lançada vai deixando de ser compatível com versões de sistemas operacionais mais antigos. 

Ao passar o mouse aba *Downloads* (na aba, e não o botão amarelo pra fazer o download!) da <a href="https://www.python.org/downloads/" target="_blank">página oficial de download do Python</a> você verá a seguinte imagem, caso esteja usando Windows:

```{figure} ../img/python-os-compat.png
:name: python-os-compat

fonte: <a href="https://www.python.org/downloads/" target="_blank">https://www.python.org/downloads/</a>
```

Reparem que há explícito *Note that Python 3.9+ cannot be used on Windows 7 or earlier*, ou seja, Python na versão 3.9 ou acima (3.10, 3.11, 3.12) não podem mais ser usados no Windows 7 ou versões anteriores.

## O que significam aqueles números na versão?

As versões da linguagem Python segue um padrão chamado <a href="https://semver.org/" target="_blank">versionamento semântico</a>.

É uma forma de dar números às versões de um software ou linguagem de programação de maneira organizada e significativa. Ele usa três números separados por pontos, no formato X.Y.Z (exemplo: *Python 3.11.9*). Os nomes técnicos destes números são X (major), Y (minor) e Z (patch) onde:

- **X (versão principal):** É incrementado quando há mudanças grandes e incompatíveis com versões anteriores. Por exemplo, no Python, isso aconteceu quando passou da versão 2 para a versão 3. Esta mudança para Python 3 introduziu várias incompatibilidades com o Python 2.

```{admonition} Cuidado
:class: danger
A mudança do Python 2 para Python 3 aconteceu em 2008, há quase duas décadas atrás. Python 2 é, portanto, muito antigo. A versão 2.7 do Python deixou de receber suporte e atualizações dos seus criadores e mantenedores em 2020.

Se vir alguém explicando algo usando Python 2, fuja para as montanhas! 🏃‍♂️💨⛰️
```

- **Y (versão secundária):** É incrementado quando são adicionadas novas funcionalidades, mas de maneira que ainda é compatível com versões anteriores. Por exemplo, quando Python 3.6 introduziu novas funcionalidades, mas ainda era compatível com Python 3.5.
- **Z (versão de correção):** É incrementado para corrigir pequenos problemas ou bugs. Essas correções não afetam as funcionalidades existentes nem adicionam novas funcionalidades significativas. Por exemplo, a atualização de Python 3.6.1 para 3.6.2 trouxe correções de bugs sem adicionar novas funcionalidades significativas.

Para você compreender melhor, supondo que o Python esteja na versão 3.6.2:

- Se for feita uma pequena correção de bug, a versão vai para 3.6.3.
- Se for adicionada uma nova funcionalidade, a versão vai para 3.7.0.
- Se houver uma mudança grande e incompatível, a versão vai para 4.0.0.

Essa forma de versionar ajuda as pessoas a entenderem o tipo de mudanças que foram feitas nas novas versões da linguagem Python, facilitando a manutenção e a evolução da linguagem como um todo.

## Tá, legal, mas qual versão instalar então? 👀

Chegamos a um ponto importante. Agora que você entendeu sobre versionamento semântico, é hora de ter argumentos pra decidir qual versão instalar.

```{admonition} Recomendação (direto ao ponto)
:class: tip
Instale a versão mais recente com status de *security* desta <a href="https://devguide.python.org/versions/#supported-versions" target="_blank">tabela</a>.
```

Existe esse site oficial do <a href="https://devguide.python.org/versions/" target="_blank">status das versões do Python</a> que serve como um guia geral do que já foi feito, o que está em andamento e o que está por vir em relação às versões do Python. 

Este site contém as seguintes seções:

```{dropdown} Python release cycle
Esta seção do site explica de uma forma visual e agradável como o Python é lançado e atualizado. Basicamente, há fases como desenvolvimento, pré-lançamento, correção de bugs, segurança e fim de vida detalhado por cada versão da linguagem ao longo dos meses e anos.
```

```{dropdown} Supported versions
Aqui temos quais versões do Python ainda recebem suporte e atualizações, e até quando esse suporte vai durar. É uma ótima recomendação, sempre que possível, usar alguma destas versões que ainda são suportadas e mantidas pela comunidade.
```

```{admonition} Unsupported versions
:class: danger, dropdown
Lista as versões que não recebem mais suporte. **Evite essas versões, pois não terão mais atualizações ou correções de segurança.**
```

```{dropdown} Status key
Esta seção é dedicada a explicar os diferentes estados das versões do Python, como "feature", "prerelease", "bugfix", "security" e "end-of-life". Isso ajuda a entender em que fase de suporte a versão está. Vamos entender melhor cada uma destas fases:
- **Feature:** Versão nova com novos recursos. Não foi lançada pois ainda está sendo desenvolvida e recebendo melhorias.
- **Prerelease:** Versão em fase de testes antes do lançamento oficial, podendo conter bugs e erros.
- **Bugfix:** Versão estável que recebe apenas correções de bugs, sem novos recursos.
- **Security:** Versão que só recebe atualizações de segurança, sem novas funcionalidades ou correções de bugs comuns.
- **End-of-life (EOL):** Versão que não recebe mais atualizações nem suporte ⚠️
```

Para escolher a melhor versão do Python, opte por uma versão (preferencialmente a mais recente) que esteja na fase de "security" ou "bugfix" para garantir que você receba atualizações e suporte.

```{admonition} Atenção
:class: warning
Atente-se ao mês/ano do fim do ciclo de vida de cada versão. O que é o mais atual hoje com certeza vai atingir esta data limite!
```

</div>
