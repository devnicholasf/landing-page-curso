# Guia Rápido - Componentização Extrema

## 🚀 Comandos Rápidos

### Criar novo componente
```bash
# Componente genérico
touch app/components/NomeComponente.vue

# Seção específica  
touch app/components/sections/NomeSection.vue
```

### Template base para componentes
```vue
<template>
  <div>
    <!-- Conteúdo do componente -->
  </div>
</template>

<script setup>
// Imports explícitos OBRIGATÓRIOS
import OutroComponente from '~/components/OutroComponente.vue'

// Props tipadas
const props = defineProps({
  propName: {
    type: String,
    required: true
  }
})
</script>
```

## 🎨 Classes Tailwind Principais

### Cores
- `text-primary` / `bg-primary` - Azul escuro #020618
- `text-secondary` / `bg-secondary` - Verde #00DC82
- `text-neutral-300` - Cinza claro para subtítulos

### Gradientes
- `bg-gradient-hero` - Gradiente principal (85% azul)
- `bg-gradient-primary` - Variação alternativa

### Tipografia
- `font-primary` - Public Sans
- `text-heading-xl` - Títulos grandes
- `text-body-base` - Texto normal

### Responsividade
- `text-3xl sm:text-4xl md:text-5xl` - Mobile para desktop

## 📋 Checklist Rápido
- [ ] Import explícito ✅
- [ ] Props tipadas ✅  
- [ ] PascalCase no nome ✅
- [ ] Mobile responsivo ✅
- [ ] Classes do design system ✅

## 🔄 Fluxo de Desenvolvimento
1. Criar componente na pasta correta
2. Definir template HTML limpo
3. Adicionar props tipadas
4. Aplicar classes Tailwind do sistema
5. Testar responsividade
6. Importar explicitamente onde usar