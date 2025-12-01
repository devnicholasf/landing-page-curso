# Agent Steering - Landing Page Componentização Extrema

## 📋 Contexto do Projeto
Este é uma landing page para vender o **Método de Componentização Extrema** - um curso/método que ensina a criar aplicativos e sites com Inteligência Artificial de forma modular e escalável.

### 🎯 Objetivo
Vender o método através de uma landing page moderna, elegante e persuasiva que demonstre na prática os conceitos de componentização extrema.

### 🛠️ Stack Tecnológica
- **Nuxt 4.2.1** - Framework Vue.js
- **Tailwind CSS** - Framework de CSS utilitário
- **Vue 3** - Composition API
- **TypeScript** - Tipagem estática

---

## 🎨 Design System

### Cores Principais
```js
// Cores baseadas no Nuxt oficial
Primary (Azul Escuro): #020618 - Predominante (85% dos gradientes)
Secondary (Verde Nuxt): #00DC82 - Accent/Destaque (15% dos gradientes)
```

### Paleta Completa
- **Primary**: Escala 50-950 com #020618 como DEFAULT
- **Secondary**: Escala 50-950 com #00DC82 como DEFAULT  
- **Neutral**: Escala de cinzas 50-950
- **Success/Error/Warning/Info**: Cores de estado
- **Aliases**: dark, light, accent, muted, border, background, foreground

### Gradientes Pré-definidos
- `bg-gradient-hero` - Gradiente principal (85% azul, 15% verde)
- `bg-gradient-primary` - Variação alternativa
- `bg-gradient-radial-primary` - Gradiente radial
- `bg-gradient-subtle` - Versão sutil
- `bg-gradient-fade` - Para transições

### Tipografia
- **Font Principal**: 'Public Sans' (Google Fonts)
- **Font Secundária**: 'Inter' (backup)
- **Font Mono**: 'JetBrains Mono' (código)
- **Tamanhos semânticos**: heading-xs até heading-2xl, body-sm/base/lg

---

## 📁 Estrutura de Arquivos

```
app/
├── components/
│   ├── Badge.vue                    # Badge reutilizável
│   ├── VideoPlayer.vue             # Player YouTube elegante
│   └── sections/
│       └── HeroSection.vue         # Seção principal
├── pages/
│   └── index.vue                   # Página inicial
└── app.vue                         # Layout principal
```

### 🔧 Convenções de Nomenclatura
- **Componentes**: PascalCase (ex: `VideoPlayer.vue`, `HeroSection.vue`)
- **Props**: camelCase (ex: `videoId`, `autoplay`)
- **Arquivos**: PascalCase para componentes, kebab-case para outros
- **Pastas**: lowercase (ex: `sections`, `components`)

---

## 📐 Regras de Desenvolvimento

### 1. Imports Explícitos OBRIGATÓRIOS
```vue
// ✅ CORRETO
<script setup>
import Badge from '~/components/Badge.vue'
import VideoPlayer from '~/components/VideoPlayer.vue'
</script>

// ❌ ERRADO - Auto-imports proibidos
<template>
  <Badge text="Auto import" /> <!-- Não permitido -->
</template>
```

### 2. Estrutura de Componentes
```vue
<template>
  <!-- HTML limpo e semântico -->
</template>

<script setup>
// Imports explícitos primeiro
import ComponenteA from '~/components/ComponenteA.vue'

// Props definidas corretamente
const props = defineProps({
  propName: {
    type: String,
    required: true
  }
})
</script>
```

### 3. Responsividade
- **Mobile First**: Sempre começar com design mobile
- **Breakpoints**: `sm:` (640px), `md:` (768px), `lg:` (1024px), `xl:` (1280px)
- **Tipografia responsiva**: `text-sm sm:text-base md:text-lg`

### 4. Classes Tailwind
- **Usar classes do design system**: Preferir `text-primary` ao invés de `text-[#020618]`
- **Gradientes**: Usar classes pré-definidas `bg-gradient-hero`
- **Espaciamentos**: Manter consistência (`mb-6`, `mb-8`, `mb-12`)

---

## 🎯 Componentes Existentes

### Badge
- **Props**: `text` (string, required)
- **Estilo**: Fundo semitransparente, borda secondary, sem seta
- **Uso**: Labels, categorias, destaques

### VideoPlayer  
- **Props**: `videoId` (string), `title` (string), `autoplay` (boolean)
- **Estilo**: Bordas duplas, gradientes, aspect ratio 16:9
- **Funcionalidade**: Embed YouTube com fallback elegante

### HeroSection
- **Elementos**: Badge, título, subtítulo, VideoPlayer, cards de features
- **Design**: Gradiente hero, elementos decorativos, mobile responsivo

---

## 📋 Diretrizes Específicas

### Para Novos Componentes
1. Criar na pasta `app/components/` ou subpastas apropriadas
2. Nome em PascalCase terminando em `.vue`
3. Props tipadas e com defaults
4. Usar design system (cores, fontes, espaciamentos)
5. Mobile first e responsivo
6. Imports explícitos obrigatórios

### Para Novas Seções
1. Criar em `app/components/sections/`
2. Nome terminado em `Section.vue` (ex: `AboutSection.vue`)
3. Seguir padrão do HeroSection
4. Reutilizar gradientes e componentes existentes

### Para Páginas
1. Criar em `app/pages/`
2. Importar seções explicitamente
3. Usar `definePageMeta()` para SEO
4. Manter componentes limpos e organizados

---

## 🚫 O Que NÃO Fazer

- ❌ Auto-imports de componentes
- ❌ Cores inline (ex: `text-[#020618]`)
- ❌ Classes CSS customizadas fora do design system
- ❌ Componentes sem props tipadas
- ❌ Design não responsivo
- ❌ Nomenclatura inconsistente
- ❌ Imports relativos confusos

---

## ✅ Checklist para Novos Desenvolvimentos

- [ ] Componente nomeado corretamente (PascalCase)
- [ ] Imports explícitos utilizados
- [ ] Props tipadas com defaults
- [ ] Design system seguido (cores, fontes, espaciamentos)
- [ ] Responsivo mobile-first
- [ ] Classes Tailwind do sistema
- [ ] Testado em mobile e desktop
- [ ] Documentação atualizada se necessário

---

**Lembre-se**: Esta landing page é uma demonstração prática do método de componentização extrema. Cada componente deve ser um exemplo de código limpo, reutilizável e bem estruturado.