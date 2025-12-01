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
            <Badge text="Método Exclusivo" />
          </div>

          <!-- Title -->
          <h2 class="font-primary text-2xl sm:text-3xl md:text-4xl lg:text-5xl font-black text-white mb-6 leading-tight">
            <span class="bg-gradient-to-r from-secondary via-secondary-400 to-secondary-600 bg-clip-text text-transparent">
              Componentização Extrema
            </span>
          </h2>

          <!-- Description -->
          <p class="font-body text-base sm:text-lg text-neutral-300 mb-8 leading-relaxed">
            Transforme sua forma de desenvolver aplicativos com nossa metodologia revolucionária que combina Inteligência Artificial com componentização modular. Crie sistemas robustos, escaláveis e manteníveis em uma fração do tempo tradicional, aproveitando o poder da automação inteligente para acelerar cada etapa do seu desenvolvimento.
          </p>

          <!-- Additional content can be added here -->
        </div>

        <!-- Right Column - App Mockup -->
        <div class="flex justify-center lg:justify-end">
          <AppMockup />
        </div>
      </div>
    </div>

    <!-- Bottom gradient fade -->
    <div class="absolute bottom-0 left-0 right-0 h-20 bg-gradient-fade"></div>
  </section>
</template>

<script setup>
import Badge from '~/components/ui/Badge.vue'
import AppMockup from '~/components/ui/AppMockup.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>