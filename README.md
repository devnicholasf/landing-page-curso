<div align="center">
  
# 🚀 Landing Page - Curso Componentização Extrema

[![Nuxt](https://img.shields.io/badge/Nuxt-4.2.1-00DC82?style=for-the-badge&logo=nuxtdotjs&logoColor=white)](https://nuxt.com/)
[![Vue.js](https://img.shields.io/badge/Vue.js-3.5.25-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white)](https://vuejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.7.2-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4.16-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

</div>

> Uma landing page moderna e responsiva desenvolvida em Nuxt.js para promover o curso de **Componentização Extrema**, demonstrando as melhores práticas de desenvolvimento Vue.js através de uma experiência visual impactante.

---

## 📋 Índice

- [✨ Visão Geral](#-visão-geral)
- [🎯 Características](#-características)
- [🛠️ Tecnologias](#️-tecnologias)
- [📁 Estrutura do Projeto](#-estrutura-do-projeto)
- [🚀 Instalação e Uso](#-instalação-e-uso)
- [🎨 Design System](#-design-system)
- [📱 Seções da Landing Page](#-seções-da-landing-page)
- [🔧 Funcionalidades](#-funcionalidades)
- [📊 Performance](#-performance)
- [🤝 Contribuição](#-contribuição)

---

## ✨ Visão Geral

Esta landing page foi desenvolvida utilizando a **metodologia de Componentização Extrema**, demonstrando na prática os conceitos ensinados no curso. Cada elemento da página é um componente reutilizável, seguindo as melhores práticas de desenvolvimento moderno.

### 🎯 Objetivo

Apresentar o curso de **Componentização Extrema** de forma atrativa e converter visitantes em alunos através de uma experiência de usuário excepcional e design profissional.

---

## 🎯 Características

### ⚡ Performance
- **SSR** (Server-Side Rendering) com Nuxt.js
- **Otimização automática** de imagens e assets
- **Code splitting** para carregamento rápido
- **Build otimizado** com compressão gzip (478 kB)

### 🎨 Design
- **Design responsivo** mobile-first
- **Animações suaves** e transições profissionais
- **Sistema de cores consistente**
- **Tipografia hierárquica** bem definida

### 🧩 Arquitetura
- **Componentização extrema** - cada elemento é um componente
- **Imports explícitos** seguindo metodologia específica
- **TypeScript** para type safety
- **Composables** para lógica reutilizável

---

## 🛠️ Tecnologias

### Core
- **[Nuxt.js 4.2.1](https://nuxt.com/)** - Framework Vue.js full-stack
- **[Vue.js 3.5.25](https://vuejs.org/)** - Framework JavaScript reativo
- **[TypeScript](https://www.typescriptlang.org/)** - Superset tipado do JavaScript

### Styling
- **[Tailwind CSS 3.4.16](https://tailwindcss.com/)** - Framework CSS utility-first
- **[Google Fonts](https://fonts.google.com/)** - Public Sans, Inter, JetBrains Mono

### Build & Development
- **[Vite 7.2.4](https://vitejs.dev/)** - Build tool moderna e rápida
- **[Nitro 2.12.9](https://nitro.unjs.io/)** - Server engine do Nuxt

---

## 📁 Estrutura do Projeto

```
landpage/
├── 📁 app/
│   ├── 📁 components/
│   │   ├── 📁 ui/                    # Componentes reutilizáveis
│   │   │   ├── ActionButton.vue      # Botão de ação principal
│   │   │   ├── Badge.vue             # Badges informativos
│   │   │   ├── VideoPlayer.vue       # Player de vídeo YouTube
│   │   │   ├── AppMockup.vue         # Mockup animado de aplicação
│   │   │   ├── ChatMockup.vue        # Simulação de chat
│   │   │   ├── CodeError.vue         # Editor de código com erros
│   │   │   ├── FolderStructure.vue   # Estrutura de pastas VS Code
│   │   │   ├── AppTypeCard.vue       # Cards de tipos de aplicação
│   │   │   ├── CourseSection.vue     # Seções expansíveis do curso
│   │   │   ├── TestimonialCard.vue   # Cards de depoimentos
│   │   │   ├── CheckoutButton.vue    # Botão especializado de compra
│   │   │   └── WhatsAppButton.vue    # Botão flutuante do WhatsApp
│   │   └── 📁 sections/              # Seções da landing page
│   │       ├── HeroSection.vue       # Seção principal/hero
│   │       ├── VibeCodingSection.vue # Demonstração de problemas
│   │       ├── MetodoSection.vue     # Apresentação da solução
│   │       ├── ComponentizacaoSection.vue # Metodologia detalhada
│   │       ├── PossibilidadesSection.vue  # Possibilidades de aplicação
│   │       ├── ConteudoCursoSection.vue   # Conteúdo do curso
│   │       ├── DepoimentosSection.vue     # Depoimentos de alunos
│   │       ├── CheckoutSection.vue        # Seção de compra
│   │       ├── FaqSection.vue             # Perguntas frequentes
│   │       └── FooterSection.vue          # Rodapé
│   ├── 📁 pages/
│   │   └── index.vue                 # Página principal
│   └── app.vue                       # App root component
├── 📁 public/
│   └── robots.txt                    # SEO robots
├── 📄 nuxt.config.ts                 # Configuração do Nuxt
├── 📄 tailwind.config.js             # Configuração do Tailwind
├── 📄 tsconfig.json                  # Configuração TypeScript
└── 📄 package.json                   # Dependências do projeto
```

---

## 🚀 Instalação e Uso

### Pré-requisitos
- Node.js 18+ 
- npm ou yarn

### Instalação

```bash
# Clone o repositório
git clone <repository-url>
cd landpage

# Instale as dependências
npm install

# Execute em modo de desenvolvimento
npm run dev

# Build para produção
npm run build

# Preview do build de produção
node .output/server/index.mjs
```

### Scripts Disponíveis

```bash
npm run dev        # Servidor de desenvolvimento
npm run build      # Build para produção
npm run preview    # Preview do build
npm run lint       # Linting do código
npm run type-check # Verificação de tipos
```

---

## 🎨 Design System

### 🎨 Paleta de Cores

```css
/* Cores Primárias */
--primary: #020618     /* Azul escuro profissional */
--secondary: #00DC82   /* Verde Nuxt (accent) */

/* Cores Neutras */
--neutral-50: #FAFAFA
--neutral-200: #E5E5E5
--neutral-400: #A3A3A3
--neutral-700: #404040
--neutral-900: #171717
```

### 📝 Tipografia

- **Heading**: Public Sans (Black, Bold)
- **Body**: Public Sans (Regular, Medium) 
- **Code**: JetBrains Mono (Monospace)

### 🎭 Componentes Base

#### ActionButton
```vue
<ActionButton texto="Começar agora" />
```

#### Badge
```vue
<Badge text="🚀 Metodologia" />
```

#### VideoPlayer
```vue
<VideoPlayer videoId="dQw4w9WgXcQ" />
```

---

## 📱 Seções da Landing Page

### 1. 🦸 Hero Section
- **Título impactante** com gradientes
- **Vídeo demonstrativo** do YouTube
- **CTA principal** direcionando para checkout

### 2. 😵 Vibe Coding Section  
- **Demonstração visual** dos problemas comuns
- **Mockups animados** de aplicações
- **Chat simulado** mostrando dificuldades

### 3. 💡 Método Section
- **Apresentação da solução**
- **Benefícios visuais** da metodologia
- **Comparativo** antes vs depois

### 4. 🧩 Componentização Section
- **Estrutura de pastas** interativa
- **Demonstração prática** da organização
- **Vantagens** da componentização extrema

### 5. 🌟 Possibilidades Section
- **Cards de aplicações** com ícones coloridos
- **8 tipos diferentes** de projetos
- **Design responsivo** em grid

### 6. 📚 Conteúdo do Curso Section
- **5 módulos expandíveis** 
- **Detalhamento** de cada módulo
- **Indicadores visuais** de progresso

### 7. 💬 Depoimentos Section
- **6 depoimentos** de alunos fictícios
- **Estatísticas** de aprovação
- **Avatars** e informações credíveis

### 8. 💳 Checkout Section
- **Preço promocional** destacado (R$ 497 vs R$ 1.497)
- **Desconto visual** de 67% OFF
- **Parcelamento** em 12x sem juros
- **Garantia** de 7 dias

### 9. ❓ FAQ Section
- **5 perguntas** principais
- **Accordion animado**
- **CTA de contato** no final

### 10. 📄 Footer Section
- **Informações legais** da empresa
- **CNPJ** e localização
- **Design minimalista**

---

## 🔧 Funcionalidades

### 🎯 Navegação Inteligente
- **ActionButtons** direcionam automaticamente para checkout
- **Scroll suave** entre seções
- **ID anchors** para navegação direta

### 📱 WhatsApp Integration
- **Botão flutuante** no canto inferior direito
- **Número teste** pré-configurado (+5585999999999)
- **Mensagem automática** sobre o curso
- **Animação pulse** para chamar atenção

### 🎬 Animações e Interações
- **Hover effects** em todos os componentes
- **Transições suaves** entre estados
- **Animações CSS** personalizadas
- **Loading states** visuais

### 📱 Responsividade
- **Mobile-first** design approach
- **Breakpoints** otimizados (sm, md, lg, xl)
- **Grid responsivo** em todas as seções
- **Tipografia escalável**

---

## 📊 Performance

### 🚀 Métricas de Build

```
Client Build: ~2.2s
Server Build: ~740ms
Total Size: 1.96 MB
Gzipped: 478 kB
```

### ⚡ Otimizações

- **Tree shaking** automático
- **Code splitting** por rota
- **Asset optimization** 
- **CSS purging** do Tailwind
- **Component lazy loading**

### 🔍 SEO

- **Server-Side Rendering** (SSR)
- **Meta tags** otimizadas
- **Estrutura semântica** HTML5
- **Robots.txt** configurado
- **Performance otimizada**

---

## 🤝 Contribuição

### Metodologia de Desenvolvimento

Este projeto segue a **metodologia de Componentização Extrema**:

1. **Um componente por arquivo**
2. **Imports explícitos obrigatórios**
3. **Props tipadas** com TypeScript
4. **Naming convention** PascalCase
5. **Estrutura organizada** ui/ e sections/

### Padrões de Código

```vue
<!-- Exemplo de componente seguindo a metodologia -->
<template>
  <div class="component-container">
    <!-- Conteúdo do componente -->
  </div>
</template>

<script setup>
// Imports explícitos
import ComponenteFilho from '~/components/ui/ComponenteFilho.vue'

// Props tipadas
const props = defineProps({
  texto: {
    type: String,
    required: true
  }
})
</script>

```

---

<div align="center">

**Desenvolvido por Nicholas**

[![Nuxt](https://img.shields.io/badge/Powered_by-Nuxt.js-00DC82?style=flat-square&logo=nuxtdotjs&logoColor=white)](https://nuxt.com/)

</div>
