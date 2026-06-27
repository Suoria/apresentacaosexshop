# Dreza Sex Shop — Catálogo

Site estático (HTML + CSS + JS num arquivo só). 84 produtos separados por categoria, busca, filtro e botão de "Comprar via WhatsApp" pré-preenchido por produto.

## Estrutura
```
dreza-site/
├── index.html        ← o site (catálogo embutido, abre direto no navegador)
├── produtos.json     ← fonte dos dados (caso queira editar produtos/preços depois)
└── imagens/          ← 90 imagens do catálogo
```

## Testar localmente
Basta abrir o `index.html` no navegador. Como o catálogo está embutido no HTML, funciona via `file://` sem servidor.

## Publicar de graça

**Opção mais simples — Netlify Drop:**
1. Acesse https://app.netlify.com/drop
2. Arraste a pasta `dreza-site` inteira pra janela.
3. Pronto, sai no ar em `algumacoisa.netlify.app`.

**Cloudflare Pages (se já versiona em Git):**
1. Suba a pasta num repo.
2. Cloudflare Pages → conecta o repo → build command vazio, output dir `/`.

## Editar produtos depois
Os dados estão tanto no `produtos.json` quanto embutidos no `index.html` (dentro de `const PRODUTOS = [...]`). Para alterar via interface, mexa direto no array dentro do `index.html`. Campos: `nome`, `preco` (número ou `null` p/ "Consultar"), `cat` (id da categoria), `desc`, `img`.

## Observações
- WhatsApp configurado: 34 98877-4824 (link wa.me com mensagem pré-preenchida).
- "Dragon & Tiger" ficou como **Consultar** porque o preço não aparecia legível na imagem — ajuste se souber o valor.
- Algumas imagens de lingerie têm modelos em poses explícitas. Se quiser uma versão mais discreta pro site público, dá pra trocar por fotos só da peça.
