# 📁 Efatá Book — Design System
### Documentação Oficial da Pasta `efata-design-system`

> **"Amor pela Palavra"** · [www.efatabook.com.br](http://www.efatabook.com.br)  
> Mantenedor: Jonas Vieira · [@JonasEfata](https://github.com/JonasEfata) · Abril 2026

---

## Índice

1. [Visão Geral](#1-visão-geral)
2. [Estrutura de Pastas](#2-estrutura-de-pastas)
3. [Quem usa e como](#3-quem-usa-e-como)
4. [tokens/colors.css](#4-tokenscolorscss)
5. [tokens/typography.css](#5-tokenstypographycss)
6. [Como usar nos projetos](#6-como-usar-nos-projetos)
7. [Resumo Rápido](#7-resumo-rápido)

---

## 1. Visão Geral

O repositório `efata-design-system` é o coração da identidade visual da **Efatá Book**. Ele reúne em um único lugar todos os padrões visuais, tokens de design, componentes de interface e diretrizes de uso da marca.

**Sem um design system**, cada projeto precisa reinventar a roda — escolher cores, fontes e padrões do zero, com risco de inconsistências entre o site, e-books, e-mails e apresentações.

**Com o design system**, qualquer projeto nasce automaticamente dentro da identidade da Efatá Book, economizando tempo e garantindo consistência em todos os canais.

> 💡 **Tokens são as "verdades imutáveis" da marca — o DNA visual do projeto.**

---

## 2. Estrutura de Pastas

```
efata-design-system/
├── index.html                  ← Guia visual interativo completo
├── README.md                   ← Documentação principal
├── DESIGN-SYSTEM.md            ← Este arquivo
├── .gitignore
│
├── tokens/
│   ├── colors.css              ← Variáveis CSS de cor
│   └── typography.css          ← Variáveis CSS de tipografia
│
├── components/
│   ├── buttons.html            ← Exemplos de botões
│   ├── cards.html              ← Cards de produto
│   └── header-footer.html      ← Cabeçalho e rodapé
│
└── assets/
    ├── logo/                   ← Versões do logotipo
    └── icons/                  ← Ícones da marca
```

---

## 3. Quem usa e como

| Perfil | Como acessa | Para que usa |
|---|---|---|
| Desenvolvedor | VS Code + GitHub | Importa os CSS, copia componentes prontos |
| Designer | GitHub Pages (link) | Consulta cores, fontes e padrões visuais |
| Colaborador | Notion (embed) | Referência visual para criação de conteúdo |
| Gestor | Qualquer navegador | Valida se materiais seguem a identidade |

---

## 4. `tokens/colors.css`

### O que é

Arquivo que define todas as **cores oficiais da Efatá Book como variáveis CSS**. É o "único lugar da verdade" para cores — se uma cor mudar, altera-se aqui e o projeto inteiro se atualiza automaticamente.

### O problema que resolve

Imagine o laranja `#F28500` espalhado em 50 arquivos CSS diferentes — botões, links, ícones, bordas. Se for necessário ajustar o tom, seria preciso encontrar e alterar os 50 arquivos manualmente. Com o token, muda-se apenas **uma linha**.

### Paleta oficial

| Nome | Hex | Token CSS | Uso principal |
|---|---|---|---|
| Azul Institucional | `#140083` | `--eb-azul` | Fundos, cabeçalho, rodapé |
| Azul Complementar | `#1A2D84` | `--eb-azul-comp` | Gradientes, seções secundárias |
| Laranja Principal | `#F28500` | `--eb-laranja` | CTAs, links, destaques |
| Amarelo Claro | `#FFEF00` | `--eb-amarelo` | Preços, badges, alertas |
| Amarelo Dourado | `#FFD700` | `--eb-dourado` | Hover, estrelas, bordas especiais |

### Categorias de tokens

| Categoria | Tokens disponíveis |
|---|---|
| Paleta principal | `--eb-azul` `--eb-azul-comp` `--eb-laranja` `--eb-amarelo` `--eb-dourado` |
| Neutros | `--eb-branco` `--eb-cinza-claro` `--eb-cinza-medio` `--eb-cinza-texto` |
| Transparências | `--eb-azul-10` `--eb-azul-20` `--eb-azul-50` `--eb-laranja-10` `--eb-laranja-20` |
| Gradientes | `--eb-grad-principal` `--eb-grad-suave` `--eb-grad-dourado` |
| Sombras | `--eb-sombra-card` `--eb-sombra-hover` `--eb-sombra-btn` |
| Bordas | `--eb-borda-card` `--eb-borda-input` `--eb-borda-foco` |

### Exemplo de uso

```css
/* ✅ Correto — usando tokens */
.botao-comprar {
  background: var(--eb-laranja);
  color: var(--eb-branco);
  box-shadow: var(--eb-sombra-btn);
}

.botao-comprar:hover {
  background: var(--eb-dourado);
  color: var(--eb-azul);
}

header {
  background: var(--eb-azul);
  box-shadow: var(--eb-sombra-card);
}

.banner {
  background: var(--eb-grad-principal);
}

/* ❌ Errado — código direto sem token */
.botao-comprar {
  background: #F28500; /* nunca faça isso */
}
```

---

## 5. `tokens/typography.css`

### O que é

Arquivo que define todos os **padrões tipográficos da Efatá Book como variáveis CSS**. Também importa automaticamente as fontes do Google Fonts, então basta incluir o arquivo e as fontes já estão disponíveis.

### Fontes oficiais

| Fonte | Token | Pesos | Uso |
|---|---|---|---|
| Montserrat | `--eb-font-titulo` | 600, 700, 800 | Títulos, marca, botões, labels |
| Lato | `--eb-font-corpo` | 300, 400, 700 | Parágrafos, descrições |
| Open Sans | `--eb-font-alt` | 400, 600 | Alternativa ao Lato |

### Escala de tamanhos

| Token | Tamanho | Uso típico |
|---|---|---|
| `--eb-texto-xs` | 11px | Labels, badges, legendas |
| `--eb-texto-sm` | 13px | Notas, rodapé, metadados |
| `--eb-texto-md` | 15px | Corpo padrão |
| `--eb-texto-lg` | 17px | Corpo de leitura confortável |
| `--eb-texto-xl` | 20px | Subtítulos menores |
| `--eb-texto-2xl` | 26px | Subtítulos |
| `--eb-texto-3xl` | 32px | Títulos de seção |
| `--eb-texto-4xl` | 42px | Títulos de página |
| `--eb-texto-5xl` | 56px | Títulos de hero / capa |
| `--eb-texto-hero` | 80px | Display / logotipo grande |

### Classes prontas para HTML

O arquivo já inclui classes CSS prontas — basta adicionar ao elemento HTML:

```html
<!-- Título principal -->
<h1 class="eb-titulo">Amor pela Palavra</h1>

<!-- Subtítulo -->
<h2 class="eb-subtitulo">Livros que transformam vidas</h2>

<!-- Destaque / citação -->
<p class="eb-destaque">"A melhor seleção de literatura cristã"</p>

<!-- Corpo de texto -->
<p class="eb-corpo">Texto do parágrafo aqui...</p>

<!-- Label / etiqueta -->
<span class="eb-label">Categoria</span>

<!-- Legenda / nota -->
<small class="eb-legenda">* Frete grátis acima de R$ 80</small>
```

### Outros tokens disponíveis

| Categoria | Tokens |
|---|---|
| Pesos | `--eb-peso-leve` `--eb-peso-normal` `--eb-peso-semibold` `--eb-peso-bold` `--eb-peso-extrabold` |
| Altura de linha | `--eb-linha-apertada` `--eb-linha-normal` `--eb-linha-conforto` `--eb-linha-ampla` |
| Espaçamento | `--eb-espaco-apertado` `--eb-espaco-normal` `--eb-espaco-aberto` `--eb-espaco-largo` |

---

## 6. Como usar nos projetos

### Opção A — Importar via CSS (recomendado)

No arquivo CSS principal do projeto, adicione no início:

```css
@import url('./tokens/colors.css');
@import url('./tokens/typography.css');

/* A partir daqui todas as variáveis e classes estão disponíveis */
```

### Opção B — Importar via HTML

```html
<head>
  <link rel="stylesheet" href="./tokens/colors.css">
  <link rel="stylesheet" href="./tokens/typography.css">
</head>
```

### Opção C — Via GitHub Pages (projetos externos)

Se o projeto não estiver no mesmo repositório, importe pelo link do GitHub Pages:

```css
@import url('https://jonasefata.github.io/efata-design-system/tokens/colors.css');
@import url('https://jonasefata.github.io/efata-design-system/tokens/typography.css');
```

> ⚠️ Esta opção depende do GitHub Pages estar ativado no repositório.

---

## 7. Resumo Rápido

| Arquivo | Responsabilidade | Resultado prático |
|---|---|---|
| `index.html` | Guia visual interativo | Consulta rápida da identidade visual completa |
| `tokens/colors.css` | Cores da marca | Paleta, gradientes, sombras e bordas prontas |
| `tokens/typography.css` | Tipografia da marca | Fontes, tamanhos e classes HTML prontas |
| `README.md` | Documentação principal | Guia para qualquer colaborador do repositório |
| `.gitignore` | Proteção do repositório | Impede envio de arquivos desnecessários |

---

> *"Um design system bem mantido poupa horas de trabalho e garante que a marca da Efatá Book seja sempre reconhecida, em qualquer canal."*

---

**Efatá Book · Amor pela Palavra · [www.efatabook.com.br](http://www.efatabook.com.br)**  
*Última atualização: Abril 2026*
