# Landing do ebook — "Quando Deus fica em silêncio"

## Resumo
- Página estática em HTML/CSS para divulgação de um ebook curto e ilustrado.
- Foco: leitura rápida, conteúdo profundo e reflexões práticas.

## Estrutura do projeto
- `page.html` — markup principal (seções: hero, "Rápido de ler. Profundo no conteúdo.", "Para quem é este ebook?", "O que você vai encontrar", Ebook ilustrado, "O que NÃO é", CTA com preço, footer).
- `styles.css` — estilos e variáveis (cores, tipografia, utilitários).
- `images/` — ilustrações e capa (referenciadas em page.html).
- `robots.txt` — permite indexação por buscadores.
- `sitemap.xml` — mapa do site para SEO (facilita indexação).
- `README.md` — este arquivo.

## Como testar localmente
1. Abra `page.html` no navegador (duplo clique) ou rode um servidor simples:
   ```bash
   python -m http.server 8000
   ```
   - Acesse: http://localhost:8000/page.html

2. Verifique que `sitemap.xml` está acessível em http://localhost:8000/sitemap.xml

## Fontes e problema de negrito
- Fontes definidas em `:root`:
  - `--font-sans`: Inter
  - `--font-serif`: Cormorant Garamond
- Garanta que Cormorant Garamond esteja carregada apenas uma vez (preferível via `<link>` no HTML). Se usar `@import` e `<link>` ao mesmo tempo, remova a duplicação.
- Para forçar título em negrito usando a classe existente, edite/garanta em `styles.css`:
  ```css
  .heading-section { font-family: var(--font-serif); font-weight: 700; }
  ```
- Após alteração, limpar cache e recarregar com **Ctrl+F5**. Verifique DevTools → Network (filtrar "font") para confirmar download.

## SEO e Indexação
- **robots.txt**: Permite indexação de todos os buscadores (Googlebot, Bingbot, etc).
- **sitemap.xml**: Mapa do site com 2 URLs (página principal e page.html).
  - Após deploy na Vercel, submeta o sitemap em:
    - [Google Search Console](https://search.google.com/search-console)
    - [Bing Webmaster Tools](https://www.bing.com/webmaster)
  - URL do sitemap na Vercel: `https://seu-projeto.vercel.app/sitemap.xml`

## Edição rápida
- Trocar texto: editar `page.html`.
- Alterar estilos principais: editar variáveis e classes em `styles.css` (procurar `:root` e seção "TYPOGRAPHY").
- Para forçar fonte/peso em elementos pontuais, use utilitários: `.font-serif`, `.fw-700`.
- Atualizar `sitemap.xml`: adicione/remova URLs conforme necessário e atualize `<lastmod>` com a data.

## Deploy
- Projetos estáticos podem ser publicados no GitHub Pages ou qualquer hospedagem estática.
- **Recomendado**: Use Vercel para deploy automático (conecte seu repositório GitHub).
- Certifique-se de incluir `images/`, `styles.css`, `page.html`, `robots.txt` e `sitemap.xml` no repositório.
- Após deploy, teste acesso às URLs e à `sitemap.xml`.

## Observações
- Robots configurado para permitir indexação (arquivo `robots.txt` presente).
- Sitemap.xml inclui prioridade e frequência de atualização para otimizar crawling.
- Design modular com variáveis CSS para facilitar mudanças.
- Meta tags OG (Open Graph) incluídas para melhor compartilhamento em redes sociais.

## Licença
- Adicione uma licença no repositório conforme desejar (ex: MIT).