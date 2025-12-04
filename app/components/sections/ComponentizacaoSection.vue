<template>
  <section class="relative py-20 bg-gradient-to-br from-primary-900 via-primary-800 to-primary-700 overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0">
      <div class="absolute top-10 right-20 w-64 h-64 bg-secondary/5 rounded-full blur-3xl"></div>
      <div class="absolute bottom-10 left-20 w-80 h-80 bg-primary-600/10 rounded-full blur-3xl"></div>
    </div>

    <!-- Main content -->
    <div class="relative z-10 container mx-auto px-6">
      <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
        <!-- Left Column - Content -->
        <div class="max-w-xl">
          <!-- Badge -->
          <div class="mb-8">
            <Badge text="Método Componentização Extrema" />
          </div>

          <!-- Title -->
          <h2 class="font-primary text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-black mb-6 leading-tight">
            <span class="text-white">Método </span><span class="text-secondary">Estruturado</span>
          </h2>

          <!-- Description -->
          <p class="font-body text-base sm:text-lg text-neutral-300 mb-8 leading-relaxed">
            Abordagem profissional que combina prompts estratégicos com arquitetura de componentes. Cada solicitação à IA é planejada para gerar código modular, testável e de qualidade enterprise.
          </p>

          <!-- Benefits List -->
          <div class="space-y-4">
            <div class="flex items-center space-x-3">
              <div class="w-2 h-2 bg-secondary rounded-full"></div>
              <span class="font-body text-neutral-300 text-sm">Arquitetura modular e escalável</span>
            </div>
            <div class="flex items-center space-x-3">
              <div class="w-2 h-2 bg-secondary rounded-full"></div>
              <span class="font-body text-neutral-300 text-sm">Código testável e maintível</span>
            </div>
            <div class="flex items-center space-x-3">
              <div class="w-2 h-2 bg-secondary rounded-full"></div>
              <span class="font-body text-neutral-300 text-sm">Padrões de qualidade enterprise</span>
            </div>
          </div>
        </div>

        <!-- Right Column - Chat Mockup -->
        <div class="flex justify-center lg:justify-end">
          <ChatMockup 
            titulo="Prompt Estruturado"
            texto="Crie BaseButton e BaseInput reutilizáveis. Implemente onClick no BaseButton que chama a função principal do userCustomer..."
          />
        </div>
      </div>

      <!-- App Result -->
      <div class="mt-24">
        <div class="text-center mb-12">
          <h3 class="font-primary text-2xl sm:text-3xl font-bold mb-3 leading-tight tracking-tight">
            <span class="text-white">Resultado da </span>
            <span class="text-neutral-400">Abordagem </span>
            <span class="text-secondary">Estruturada:</span>
          </h3>
          <p class="font-body text-neutral-300 text-sm">Aplicação robusta e profissional</p>
        </div>
        
        <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-start">
          <!-- Left Column - Benefits Text -->
          <div class="max-w-xl text-left">
            <!-- Title -->
            <h4 class="font-primary text-xl sm:text-2xl font-bold mb-6 leading-tight tracking-tight flex items-center">
              <!-- Success Icon -->
              <div class="w-8 h-8 bg-gradient-to-br from-green-500 to-green-600 rounded-lg flex items-center justify-center mr-4 shadow-lg border border-green-400/50">
                <svg class="w-5 h-5 text-white drop-shadow-sm" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/>
                </svg>
              </div>
              <div>
                <span class="text-white">Vantagens da </span>
                <span class="text-secondary">Abordagem</span>
              </div>
            </h4>

            <!-- Benefits Text -->
            <p class="font-body text-base leading-relaxed">
              <span class="text-neutral-300">Prompts </span>
              <span class="text-secondary">estratégicos e planejados</span>
              <span class="text-neutral-300"> geram componentes </span>
              <span class="text-green-300">modulares e testáveis</span>
              <span class="text-neutral-300">. A IA produz soluções que seguem </span>
              <span class="text-green-400">padrões de arquitetura enterprise</span>
              <span class="text-neutral-300">, criando uma </span>
              <span class="text-green-300">base de código profissional</span>
              <span class="text-neutral-300">. Diferente do </span>
              <span class="text-red-300">desenvolvimento sem método</span>
              <span class="text-neutral-300">, esta abordagem resulta em </span>
              <span class="text-secondary">sistemas robustos</span>
              <span class="text-neutral-300"> com componentes bem definidos. O resultado é </span>
              <span class="text-secondary">código de qualidade</span>
              <span class="text-neutral-300"> que </span>
              <span class="text-green-300">escala facilmente</span>
              <span class="text-neutral-300"> e facilita futuras expansões.</span>
            </p>
          </div>

          <!-- Right Column - Folder Structure -->
          <div class="flex justify-center lg:justify-end">
            <FolderStructure />
          </div>
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
import FolderStructure from '~/components/ui/FolderStructure.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>