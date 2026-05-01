# 📝 Instruções para Criação de Posts no Blog

## IA Advocacia Empresarial — Guia de Publicação

---

## 📋 Visão Geral

Cada post do blog é um arquivo HTML individual baseado no template `post-template.html`. Para criar um novo artigo, duplique o template, altere o conteúdo conforme as instruções abaixo, e salve na pasta correta.

---

## 🗂️ Estrutura de Arquivos

```
site2/
├── post-template.html          ← Template base (NÃO editar)
├── blog/
│   └── index.html              ← Listagem do blog
├── [nome-do-post]/
│   └── index.html              ← Cada post vive aqui
└── assets/
    └── images/
        └── [imagens-do-post].jpg
```

> [!IMPORTANT]
> Cada post deve estar em sua **própria pasta** na raiz do projeto. O nome da pasta deve ser o slug do artigo (sem acentos, sem espaços, usando hífens).

### Exemplo de Nomenclatura

| Título do Artigo | Slug / Nome da Pasta |
|---|---|
| STJ invalida notificação por e-mail | `stj-invalida-notificacao-por-email` |
| Defesa em leilões de imóveis | `defesa-em-leiloes-de-imoveis` |
| Usucapião de imóvel financiado | `usucapiao-de-imovel-financiado` |

---

## 🔧 Passo a Passo

### 1. Duplicar o Template

```
Copiar: post-template.html
Colar em: [slug-do-post]/index.html
```

### 2. Atualizar o `<head>` (Metadados SEO)

Localize e edite as seguintes tags no `<head>`:

```html
<!-- TÍTULO DA PÁGINA (aparece na aba do navegador) -->
<title>[TÍTULO DO POST] – IA Advocacia Empresarial</title>

<!-- DESCRIÇÃO SEO (aparece no Google) -->
<meta name="description" content="[Resumo do artigo em 150-160 caracteres]">

<!-- OPEN GRAPH (compartilhamento em redes sociais) -->
<meta property="og:type" content="article">
<meta property="og:title" content="[TÍTULO DO POST] – IA Advocacia Empresarial">
<meta property="og:description" content="[Resumo do artigo em 150-160 caracteres]">
<meta property="og:image" content="../assets/images/[imagem-capa].jpg">
```

> [!TIP]
> A descrição SEO ideal tem entre **150 e 160 caracteres** e deve conter as palavras-chave principais do artigo.

---

### 3. Atualizar o Banner (Título do Post)

Localize o comentário `<!-- BANNER DO POST -->` e edite:

```html
<h2 class="elementor-heading-title elementor-size-default">
    [TÍTULO DO SEU POST AQUI]
</h2>
```

---

### 4. Atualizar a Imagem de Capa

Localize o bloco da imagem destacada:

```html
<img alt="[Descrição da imagem]" width="1800" height="1080" 
     src="../assets/images/[sua-imagem-de-capa].jpg">
```

> [!NOTE]
> - A imagem deve ter **1800×1080 pixels** (proporção 16:10)
> - Formatos aceitos: `.jpg`, `.png`, `.webp`
> - Salvar em: `assets/images/`
> - Usar nomes descritivos: `artigo-usucapiao-imovel.jpg`

---

### 5. Atualizar a Data de Publicação

Localize o bloco de data (aparece 1 vez no post):

```html
<time>01 de janeiro de 2025</time>
```

Altere para a data real de publicação:

```html
<time>[DIA] de [MÊS] de [ANO]</time>
```

---

### 6. Escrever o Conteúdo do Artigo

Localize o comentário `<!-- CONTEÚDO DO POST -->` e o bloco `<article>`. Substitua o conteúdo Lorem Ipsum:

```html
<article class="elementor-element elementor-element-610a690 ...">
    
    <h1>[TÍTULO PRINCIPAL DO ARTIGO]</h1>
    
    <p class="elementor-post-info__item--type-date">[DATA]</p>
    
    <img alt="[Descrição]" src="../assets/images/[imagem-capa].jpg">
    
    <!-- CONTEÚDO AQUI ↓ -->
    
    <p>Primeiro parágrafo do artigo...</p>
    
    <h2>Subtítulo da Seção</h2>
    <p>Conteúdo da seção...</p>
    
    <h3>Sub-subtítulo</h3>
    <p>Detalhamento...</p>
    
    <blockquote>
        <p>"Citação relevante de jurisprudência ou legislação."</p>
    </blockquote>
    
    <ul>
        <li>Ponto importante 1</li>
        <li>Ponto importante 2</li>
        <li>Ponto importante 3</li>
    </ul>
    
    <p><strong>Texto em negrito</strong> para destaque.</p>
    <p><em>Texto em itálico</em> para ênfase.</p>
    
    <p>Fonte: <a href="[URL]" target="_blank" rel="noopener">[Nome da Fonte]</a></p>
    
</article>
```

---

### 7. Tags HTML Permitidas no Conteúdo

| Tag | Uso | Exemplo |
|---|---|---|
| `<h1>` | Título principal (1 por post) | `<h1>Título do Artigo</h1>` |
| `<h2>` | Subtítulos de seção | `<h2>Fundamentação Legal</h2>` |
| `<h3>` | Sub-subtítulos | `<h3>Art. 50 do Código Civil</h3>` |
| `<p>` | Parágrafos | `<p>Texto do parágrafo.</p>` |
| `<strong>` | Negrito | `<strong>importante</strong>` |
| `<em>` | Itálico | `<em>ver art. 28 do CDC</em>` |
| `<a>` | Links | `<a href="URL" target="_blank">texto</a>` |
| `<ul>` / `<li>` | Listas | `<ul><li>Item</li></ul>` |
| `<ol>` / `<li>` | Listas numeradas | `<ol><li>Primeiro</li></ol>` |
| `<blockquote>` | Citações | `<blockquote><p>Citação</p></blockquote>` |
| `<img>` | Imagens extras | `<img src="../assets/images/x.jpg" alt="desc">` |

---

### 8. Ajustar o Link do WhatsApp (CTA)

O botão "QUERO FALAR COM UM ADVOGADO" já está configurado com o link correto:

```html
<a class="elementor-button elementor-button-link elementor-size-sm" 
   href="https://wa.me/5531922925411">
```

> [!NOTE]
> Não altere o link do WhatsApp a menos que o número mude.

---

## 🎨 Paleta de Cores e Tipografia

| Token | Cor | Uso |
|---|---|---|
| Midnight | `#1B2A4A` | Títulos, cabeçalho |
| Champagne Gold | `#C3A84C` | Acentos, botões, dividers |
| Carrara White | `#F5F3EF` | Fundo alternado |
| Graphite Gray | `#444A4A` | Texto corpo |

**Fonte**: Montserrat Bold (700) para títulos, Montserrat Regular (400-500) para corpo.

---

## ✅ Checklist Antes de Publicar

- [ ] Pasta criada com slug correto (sem acentos, com hífens)
- [ ] `<title>` atualizado
- [ ] `<meta name="description">` preenchido (150-160 chars)
- [ ] Tags Open Graph atualizadas
- [ ] Banner com título correto
- [ ] Imagem de capa salva em `assets/images/` (1800×1080)
- [ ] Data de publicação correta
- [ ] Conteúdo do `<article>` escrito e formatado
- [ ] Links verificados (sem links quebrados)
- [ ] CTA de WhatsApp funcionando
- [ ] Testado no navegador local (`http://localhost:8080/[slug]/index.html`)

---

## 📂 Adicionando à Listagem do Blog (Opcional)

Se desejar que o post apareça na listagem do blog (`blog/index.html`), adicione um bloco de card dentro do grid existente:

```html
<div class="jet-posts__item">
    <div class="jet-posts__inner-box">
        <div class="post-thumbnail">
            <a href="../[slug-do-post]/index.html" class="post-thumbnail__link">
                <img class="post-thumbnail__img wp-post-image" 
                     alt="[Título do Post]" 
                     width="1800" height="1080" 
                     src="../assets/images/[imagem-capa].jpg">
            </a>
        </div>
        <div class="jet-posts__inner-content">
            <h4 class="entry-title">
                <a href="../[slug-do-post]/index.html">[Título do Post]</a>
            </h4>
            <div class="post-meta">
                <span class="post__date post-meta__item">
                    <time>[DD/MM/AAAA]</time>
                </span>
            </div>
            <div class="entry-excerpt">
                [Resumo do artigo em 1-2 linhas]
            </div>
        </div>
    </div>
</div>
```

---

> [!CAUTION]
> **Nunca edite diretamente o `post-template.html`**. Ele serve como modelo limpo para futuros posts. Sempre duplique antes de editar.
