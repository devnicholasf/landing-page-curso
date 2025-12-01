<template>
  <section class="relative min-h-screen bg-gradient-hero overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0">
      <div class="absolute top-20 left-10 w-72 h-72 bg-secondary/10 rounded-full blur-3xl"></div>
      <div class="absolute bottom-20 right-10 w-96 h-96 bg-primary-700/20 rounded-full blur-3xl"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-gradient-radial-primary opacity-30 rounded-full blur-3xl"></div>
    </div>

    <!-- Main content -->
    <div class="relative z-10 container mx-auto px-6 py-20 flex items-center min-h-screen">
      <div class="max-w-4xl mx-auto text-center">
        <!-- Badge -->
        <div class="mb-8">
          <Badge text="Método componentização extrema" />
        </div>

        <!-- Main heading -->
        <h1 class="font-primary text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-black text-white mb-6 leading-[1.1]">
          Crie o seu 
          <span class="bg-gradient-to-r from-secondary via-secondary-400 to-secondary-600 bg-clip-text text-transparent">
            SaaS com IA
          </span>
          até 10x mais rápido
        </h1>

        <!-- Subtitle -->
        <p class="font-body text-sm sm:text-base md:text-lg text-neutral-300 mb-8 max-w-2xl mx-auto leading-relaxed">
          Desenvolva aplicativos de forma segura, escalável e com total controle sobre seu código com Inteligência Artificial
        </p>

        <!-- Video Player -->
        <div class="mb-12">
          <VideoPlayer 
            video-id="dQw4w9WgXcQ" 
            title="Como criar SaaS com IA - Demo"
          />
        </div>

        <!-- Features highlights -->
        <div class="grid md:grid-cols-3 gap-8 mt-16">
          <div class="bg-white/5 backdrop-blur-md rounded-2xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300">
            <div class="w-12 h-12 bg-secondary/20 rounded-lg mx-auto mb-4 flex items-center justify-center">
              <span class="text-secondary text-2xl">⚡</span>
            </div>
            <h3 class="font-primary text-heading-sm text-white mb-2">10x Mais Rápido</h3>
            <p class="font-body text-body-sm text-neutral-400">Acelere seu desenvolvimento com IA inteligente</p>
          </div>

          <div class="bg-white/5 backdrop-blur-md rounded-2xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300">
            <div class="w-12 h-12 bg-secondary/20 rounded-lg mx-auto mb-4 flex items-center justify-center">
              <span class="text-secondary text-2xl">🔒</span>
            </div>
            <h3 class="font-primary text-heading-sm text-white mb-2">100% Seguro</h3>
            <p class="font-body text-body-sm text-neutral-400">Seu código permanece privado e protegido</p>
          </div>

          <div class="bg-white/5 backdrop-blur-md rounded-2xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300">
            <div class="w-12 h-12 bg-secondary/20 rounded-lg mx-auto mb-4 flex items-center justify-center">
              <span class="text-secondary text-2xl">📈</span>
            </div>
            <h3 class="font-primary text-heading-sm text-white mb-2">Escalável</h3>
            <p class="font-body text-body-sm text-neutral-400">Cresça sem limites com arquitetura robusta</p>
          </div>
        </div>

        <!-- Action Button -->
        <div class="mt-12 text-center">
          <ActionButton texto="Começar agora" />
        </div>
      </div>
    </div>

    <!-- Bottom gradient fade -->
    <div class="absolute bottom-0 left-0 right-0 h-32 bg-gradient-fade"></div>
  </section>
</template>

<script setup>
import Badge from '~/components/ui/Badge.vue'
import VideoPlayer from '~/components/ui/VideoPlayer.vue'
import ActionButton from '~/components/ui/ActionButton.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>