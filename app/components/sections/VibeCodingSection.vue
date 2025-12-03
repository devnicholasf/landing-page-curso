<template>
  <section class="relative py-20 bg-gradient-to-br from-primary-900 via-primary-800 to-primary-700 overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0">
      <div class="absolute top-10 left-20 w-64 h-64 bg-red-500/5 rounded-full blur-3xl"></div>
      <div class="absolute bottom-10 right-20 w-80 h-80 bg-yellow-500/5 rounded-full blur-3xl"></div>
    </div>

    <!-- Main content -->
    <div class="relative z-10 container mx-auto px-6">
      <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
        <!-- Left Column - Content -->
        <div class="max-w-xl">
          <!-- Badge -->
          <div class="mb-8">
            <Badge text="Método Tradicional" />
          </div>

          <!-- Title -->
          <h2 class="font-primary text-2xl sm:text-3xl md:text-4xl lg:text-5xl font-black mb-6 leading-tight">
            <span class="text-white">Vibe </span><span class="text-secondary">Coding</span>
          </h2>

          <!-- Description -->
          <p class="font-body text-base sm:text-lg text-neutral-300 mb-8 leading-relaxed">
            O método tradicional onde desenvolvedores enviam prompts aleatórios para IA, sem estrutura ou metodologia. Resulta em código inconsistente, difícil manutenção e projetos que se tornam inviáveis rapidamente.
          </p>

          <!-- Problems List -->
          <div class="space-y-4">
            <div class="flex items-center space-x-3">
              <div class="w-2 h-2 bg-red-400 rounded-full"></div>
              <span class="font-body text-neutral-400 text-sm">Código desorganizado e inconsistente</span>
            </div>
            <div class="flex items-center space-x-3">
              <div class="w-2 h-2 bg-yellow-400 rounded-full"></div>
              <span class="font-body text-neutral-400 text-sm">Projetos que se tornam inviáveis</span>
            </div>
            <div class="flex items-center space-x-3">
              <div class="w-2 h-2 bg-orange-400 rounded-full"></div>
              <span class="font-body text-neutral-400 text-sm">Dependência total da IA sem método</span>
            </div>
          </div>
        </div>

        <!-- Right Column - Chat Mockup -->
        <div class="flex justify-center lg:justify-end">
          <ChatMockup 
            titulo="Vibe Coding"
            texto="Crie um aplicativo de gestão..."
          />
        </div>
      </div>
    </div>

    <!-- Bottom gradient fade -->
    <div class="absolute bottom-0 left-0 right-0 h-20 bg-gradient-fade"></div>
  </section>
</template>

<script setup>
import Badge from '~/components/ui/Badge.vue'
import ChatMockup from '~/components/ui/ChatMockup.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>