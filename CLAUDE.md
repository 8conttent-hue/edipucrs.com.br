# CLAUDE.md — EDIPUCRS

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** EDIPUCRS
**Nicho:** Negócios e Empreendedorismo
**Keywords:** PORQUE FAZEMOS O QUE FAZEMOS Nossa Equipe Sao varios canais que visam
**Paleta de cores:** sunset | **Fonte:** inter

PORQUE FAZEMOS O QUE FAZEMOS? Nossa Equipe São vários canais que visam fomentar o empreendedorismo e dar visibilidade aos pequenos negócios e as várias iniciativas. Iniciado em agosto de 2016, o nosso Blog de deu início ao movimento de resistência à crise no auge do impeachment da ex-presidente(A) Dilma. Queremos um empreendedor em cada lar! E por isso mesmo, compartilhamos aqui os nossos melhores conteúdos, tudo gratuitamente, sem esquecer absolutamente nada, sem esconder informações importantes e necessárias. Hoje, você pode aprender tudo que precisa pra criar ou levantar de vez esse seu negócio, seja ele qual for! Junte-se a esse movimento! levante nossa bandeira! e navegue no nosso Blog Já!



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-F |
| Hero | Hero-G |
| Features | Features-F |
| About Section | About-F |
| Posts | Posts-H |
| Footer | Footer-E |
| Página Sobre | Sobre-J |
| Página Contato | Contato-E |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
