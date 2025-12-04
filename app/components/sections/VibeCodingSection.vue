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
            <span class="text-white">Vibe </span><span class="text-red-400">Coding</span>
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
            texto="Crie um aplicativo de gestão"
          />
        </div>
      </div>

      <!-- Code Error Result -->
      <div class="mt-24">
        <div class="text-center mb-12">
          <h3 class="font-primary text-2xl sm:text-3xl font-bold mb-3 leading-tight tracking-tight">
            <span class="text-white">Resultado do </span>
            <span class="text-red-400">Vibe </span>
            <span class="text-red-400">Coding:</span>
          </h3>
          <p class="font-body text-neutral-300 text-sm">Código gerado pela IA sem metodologia</p>
        </div>
        
        <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-start">
          <!-- Left Column - Problems Text -->
          <div class="max-w-xl text-left">
            <!-- Title -->
            <h4 class="font-primary text-xl sm:text-2xl font-bold mb-6 leading-tight tracking-tight flex items-center">
              <!-- Warning Icon -->
              <div class="w-8 h-8 bg-gradient-to-br from-red-500 to-red-600 rounded-lg flex items-center justify-center mr-4 shadow-lg border border-red-400/50">
                <svg class="w-5 h-5 text-white drop-shadow-sm" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M1 21h22L12 2 1 21zm12-3h-2v-2h2v2zm0-4h-2v-4h2v4z"/>
                </svg>
              </div>
              <div>
                <span class="text-white">Problemas do Código </span>
                <span class="text-red-400">sem Metodologia</span>
              </div>
            </h4>

            <!-- Problems Text -->
            <p class="font-body text-base leading-relaxed">
              <span class="text-neutral-300">Quando desenvolvedores usam </span>
              <span class="text-red-300">prompts aleatórios</span>
              <span class="text-neutral-300"> sem uma metodologia estruturada, o resultado é sempre o mesmo: </span>
              <span class="text-red-400">código inconsistente, cheio de erros e impossível de manter</span>
              <span class="text-neutral-300">. A IA gera soluções pontuais que não conversam entre si, criando um </span>
              <span class="text-red-300">emaranhado de dependências quebradas</span>
              <span class="text-neutral-300"> e funções mal implementadas. O que deveria ser um </span>
              <span class="text-secondary">projeto simples</span>
              <span class="text-neutral-300"> se transforma rapidamente em um </span>
              <span class="text-red-400">pesadelo técnico</span>
              <span class="text-neutral-300">, onde cada nova funcionalidade quebra três outras já existentes. Sem </span>
              <span class="text-secondary">componentização adequada</span>
              <span class="text-neutral-300">, o código se torna uma </span>
              <span class="text-red-300">torre de cartas pronta para desabar</span>
              <span class="text-neutral-300"> ao menor toque.</span>
            </p>
          </div>

          <!-- Right Column - Code Error -->
          <div class="flex justify-center lg:justify-end">
            <CodeError 
              fileName="AppGestao.vue"
              :errorCount="15"
            />
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
import CodeError from '~/components/ui/CodeError.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>