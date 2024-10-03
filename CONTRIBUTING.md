# Guia de contribuição

## Regras de Contribuição

Para mantermos o projeto organizado, siga estas orientações ao contribuir:
- As pastas devem começar com números sequenciais, seguidos de um hífen e o nome da pasta.
  - Exemplo: `01-instalacao-python`
  - Cada pasta representa uma seção no menu lateral esquerdo do livro.
  - Não utilize acentos, espaços em branco ou caracteres especiais no nome das pastas.
- Os arquivos dentro das pastas também seguem essa numeração e formato de nome.
  - Exemplo: `01-intro.md`
  - Não utilize acentos, espaços em branco ou caracteres especiais no nome dos arquivos.
  - Cada arquivo será uma subseção no menu lateral esquerdo.
- O arquivo `_toc.yml` configura o menu lateral do livro. **Não esqueça de atualizá-lo** sempre que adicionar um novo arquivo ou pasta.
- Você pode escrever o conteúdo do livro tanto em formato `.md` quanto em formato `.ipynb`.
- As imagens e gifs devem seguir o padrão de nomeação: 
  - `<numero-da-pasta>-<numero-do-arquivo>-descricao-da-imagem-ou-gif.extensao`. Exemplo: `09-03-modulos.png`
  - Esses arquivos são armazenados nas pastas `book/img` e `book/gifs`. Siga o padrão já existente para manter a consistência.

## Como contribuir

1. Faça um **fork** deste repositório para sua conta do GitHub.
2. Clone o seu repositório para a sua máquina.
3. Instale o poetry com o comando:
```bash
pip install poetry
```
4. Instale as dependências do projeto com o comando:
```bash
poetry install --with dev
```
5. Faça suas alterações. Caso adicione novos arquivos ou pastas, **lembre-se de adicioná-los em `book/_toc.yml`**.
6. Teste o build local do livro com o comando abaixo. O buid deve ser executado sem erros.
```bash
task build
```
7. Faça o commit e o push das suas alterações para o seu repositório.
8. Abra um Pull Request para o repositório original, explicando as mudanças que você fez. 
9. Vincule alguma issue se houver para que ela seja encerrada automaticamente quando o PR for aceito. Caso tenha dúvidas de como fazer esta etapa, consulte este [link](https://docs.github.com/pt/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue).
10. Suas alterações passarão por uma revisão antes de serem aceitas.
11. Após aprovadas, suas alterações serão refletidas no livro em poucos minutos!
