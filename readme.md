# Landing do ebook — "Quando Deus fica em silêncio"

Resumo
- Página estática em HTML/CSS para divulgação de um ebook curto e ilustrado.
- Foco: leitura rápida, conteúdo profundo e reflexões práticas.

Estrutura do projeto
- page.html — markup principal (seções: hero, "Para quem é este ebook?", seção destacada "Rápido de ler. Profundo no conteúdo.", "O que você vai encontrar", Ebook ilustrado, footer).
- styles.css — estilos e variáveis (cores, tipografia, utilitários).
- images/ — ilustrações e capa (referenciadas em page.html).
- robots.txt — permite indexação.

Como testar localmente
1. Abra `page.html` no navegador (duplo clique) ou rode um servidor simples:
   - No terminal (Windows):
     python -m http.server 8000
   - Acesse: http://localhost:8000/page.html

Fontes e problema de negrito
- Fontes definidas em :root:
  --font-sans: Inter
  --font-serif: Cormorant Garamond
- Garanta que Cormorant Garamond esteja carregada apenas uma vez (preferível via <link> no HTML). Se usar @import e <link> ao mesmo tempo, remova a duplicação.
- Para forçar título em negrito usando a classe existente, edite/garanta em `styles.css`:
  .heading-section { font-family: var(--font-serif); font-weight: 700; }
- Após alteração, limpar cache e recarregar com Ctrl+F5. Verifique DevTools → Network (filtrar "font") para confirmar download.

Edição rápida
- Trocar texto: editar `page.html`.
- Alterar estilos principais: editar variáveis e classes no `styles.css` (procurar :root e seção "TYPOGRAPHY").
- Para forçar fonte/peso em elementos pontuais, use utilitários: `.font-serif`, `.fw-700`.

Deploy
- Projetos estáticos podem ser publicados no GitHub Pages ou qualquer hospedagem estática.
- Certifique-se de incluir `images/`, `styles.css` e `page.html` no repositório.

Observações
- Robots configurado para permitir indexação (arquivo `robots.txt` presente).
- Mantive design modular com variáveis CSS para facilitar mudanças.

Licença
- Adicione uma licença no repositório conforme desejar (ex: MIT).

```// filepath: c:\Users\Tiago\python_2025\testando5\README.md
# Landing do ebook — "Quando Deus fica em silêncio"

Resumo
- Página estática em HTML/CSS para divulgação de um ebook curto e ilustrado.
- Foco: leitura rápida, conteúdo profundo e reflexões práticas.

Estrutura do projeto
- page.html — markup principal (seções: hero, "Para quem é este ebook?", seção destacada "Rápido de ler. Profundo no conteúdo.", "O que você vai encontrar", Ebook ilustrado, footer).
- styles.css — estilos e variáveis (cores, tipografia, utilitários).
- images/ — ilustrações e capa (referenciadas em page.html).
- robots.txt — permite indexação.

Como testar localmente
1. Abra `page.html` no navegador (duplo clique) ou rode um servidor simples:
   - No terminal (Windows):
     python -m http.server 8000
   - Acesse: http://localhost:8000/page.html

Fontes e problema de negrito
- Fontes definidas em :root:
  --font-sans: Inter
  --font-serif: Cormorant Garamond
- Garanta que Cormorant Garamond esteja carregada apenas uma vez (preferível via <link> no HTML). Se usar @import e <link> ao mesmo tempo, remova a duplicação.
- Para forçar título em negrito usando a classe existente, edite/garanta em `styles.css`:
  .heading-section { font-family: var(--font-serif); font-weight: 700; }
- Após alteração, limpar cache e recarregar com Ctrl+F5. Verifique DevTools → Network (filtrar "font") para confirmar download.

Edição rápida
- Trocar texto: editar `page.html`.
- Alterar estilos principais: editar variáveis e classes no `styles.css` (procurar :root e seção "TYPOGRAPHY").
- Para forçar fonte/peso em elementos pontuais, use utilitários: `.font-serif`, `.fw-700`.

Deploy
- Projetos estáticos podem ser publicados no GitHub Pages ou qualquer hospedagem estática.
- Certifique-se de incluir `images/`, `styles.css` e `page.html` no repositório.

Observações
- Robots configurado para permitir indexação (arquivo `robots.txt` presente).
- Mantive design modular com variáveis CSS para facilitar mudanças.

Licença
- Adicione uma licença no repositório conforme desejar (ex: MIT).
