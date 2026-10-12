# Slides WEB3UP

Apresentações dos workshops WEB3UP, publicadas em https://web3uprising.github.io/slides/.

Cada apresentação é um ficheiro Markdown em `decks/<nome>/slides.md`, transformado em
slides com [reveal-md](https://github.com/webpro/reveal-md). A estrutura é uma versão
simplificada do [pba-content](https://github.com/Polkadot-Blockchain-Academy/pba-content)
da Polkadot Blockchain Academy, sem a agenda, os temas antigos nem os plugins de gráficos.

## Escrever

```sh
npm install
npm start            # http://localhost:1948 com recarga automática
npm run build        # site estático em build/
```

`---` separa slides e `---v` cria um slide vertical por baixo do anterior. `Note:` começa as
notas de quem fala, que aparecem ao carregar em S. As classes do tema estão em
`assets/theme.css` e seguem o site web3up.org: `hero` para slides de abertura com o gradiente, `cols`, `card`, `flow`, `steps`, `pills`, `eyebrow` e `lead`.

Para uma apresentação nova, cria `decks/<nome>/slides.md` com `title` e `description` no
cabeçalho. A página inicial lista-a automaticamente.

## Publicar

Cada push para `main` constrói o site e publica-o no GitHub Pages pelo workflow
`.github/workflows/pages.yml`.
