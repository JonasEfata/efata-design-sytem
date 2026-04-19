# 🎨 Efatá Book — Design System

> **"Amor pela Palavra"** · [www.efatabook.com.br](http://www.efatabook.com.br)

Repositório oficial do Design System da **Efatá Book**. Centraliza todos os padrões visuais, tokens de design, componentes de interface e diretrizes de uso da marca.

---

## 📋 Conteúdo

| Arquivo / Pasta | Descrição |
|---|---|
| `index.html` | Guia visual interativo completo |
| `tokens/colors.css` | Variáveis CSS oficiais da paleta |
| `tokens/typography.css` | Variáveis CSS de tipografia |
| `components/` | Componentes HTML prontos para uso |
| `assets/` | Logos, ícones e imagens da marca |

---

## 🎨 Paleta Oficial

| Nome | Hex | Uso |
|---|---|---|
| Azul Institucional | `#140083` | Cor primária, fundos, cabeçalho |
| Azul Complementar | `#1A2D84` | Gradientes, seções secundárias |
| Laranja Principal | `#F28500` | CTAs, links, destaques |
| Amarelo Claro | `#FFEF00` | Preços, badges, alertas |
| Amarelo Dourado | `#FFD700` | Hover, estrelas, bordas especiais |

---

## 🔤 Tipografia

- **Títulos** → `Montserrat` Bold / ExtraBold (700, 800)
- **Subtítulos** → `Montserrat` SemiBold (600)
- **Destaques** → `Montserrat` SemiBold Itálico
- **Corpo** → `Lato` ou `Open Sans` Regular (400)

```css
/* Importar no projeto */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&family=Lato:wght@300;400;700&display=swap');
```

---

## ⚡ Como usar os tokens CSS

Copie o bloco abaixo no início do seu CSS:

```css
:root {
  /* Cores */
  --eb-azul:        #140083;
  --eb-azul-comp:   #1A2D84;
  --eb-laranja:     #F28500;
  --eb-amarelo:     #FFEF00;
  --eb-dourado:     #FFD700;
  --eb-branco:      #FFFFFF;

  /* Tipografia */
  --eb-font-titulo: 'Montserrat', sans-serif;
  --eb-font-corpo:  'Lato', sans-serif;

  /* Gradiente institucional */
  --eb-gradiente: linear-gradient(135deg, #140083, #F28500);
}
```

---

## 🧩 Componentes disponíveis

### Botão Primário
```html
<button class="eb-btn-primary">Comprar Agora</button>
```
```css
.eb-btn-primary {
  background: var(--eb-laranja);
  color: #fff;
  font-family: var(--eb-font-titulo);
  font-weight: 700;
  padding: 12px 28px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  transition: background 0.2s ease;
}
.eb-btn-primary:hover {
  background: var(--eb-dourado);
  color: var(--eb-azul);
}
```

### Cabeçalho padrão
```html
<header class="eb-header">
  <div class="eb-header-logo">Efatá <span>Book</span></div>
  <nav>...</nav>
</header>
```
```css
.eb-header {
  background: var(--eb-azul);
  color: #fff;
  padding: 16px 48px;
}
.eb-header-logo span { color: var(--eb-laranja); }
```

---

## 🚫 Diretrizes importantes

- ✅ Usar sempre as 5 cores da paleta oficial
- ✅ Montserrat para títulos, Lato para corpo de texto
- ✅ Ilustrações em estilo vetorial, cartoon ou abstrato/cubista
- ✅ Ícones e elementos visuais sempre dentro da paleta institucional
- 🚫 Não representar literalmente Deus, Jesus ou o Espírito Santo
- 🚫 Não criar variações de cor fora da paleta sem aprovação

---

## 🌐 Visualizar o Guia

Acesse o guia visual interativo em:
**[jonasefata.github.io/efata-design-system](https://jonasefata.github.io/efata-design-system)**

---

## 📁 Estrutura recomendada do repositório

```
efata-design-system/
├── index.html              # Guia visual principal
├── README.md               # Este arquivo
├── .gitignore
├── tokens/
│   ├── colors.css          # Variáveis de cor
│   └── typography.css      # Variáveis de tipografia
├── components/
│   ├── buttons.html        # Exemplos de botões
│   ├── cards.html          # Cards de produto
│   └── header-footer.html  # Cabeçalho e rodapé
└── assets/
    ├── logo/               # Versões do logotipo
    └── icons/              # Ícones da marca
```

---

## 👤 Mantenedor

**Jonas Vieira** · [JonasEfata](https://github.com/JonasEfata)  
Efatá Book · São Paulo, Brasil

---

*Última atualização: Abril 2026*
