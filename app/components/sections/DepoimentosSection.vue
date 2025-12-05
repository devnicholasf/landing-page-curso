<template>
  <section class="relative py-20 bg-gradient-to-br from-primary-900 via-primary-800 to-primary-700 overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0">
      <div class="absolute top-20 right-20 w-64 h-64 bg-secondary/5 rounded-full blur-3xl"></div>
      <div class="absolute bottom-20 left-20 w-80 h-80 bg-primary-600/10 rounded-full blur-3xl"></div>
    </div>

    <!-- Main content -->
    <div class="relative z-10 container mx-auto px-6">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <!-- Badge -->
        <div class="flex justify-center mb-8">
          <Badge text="Depoimentos" />
        </div>

        <!-- Title -->
        <h2 class="font-primary text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-black mb-6 leading-tight">
          <span class="text-white">O que Nossos </span>
          <span class="bg-gradient-to-r from-secondary via-secondary-400 to-secondary-600 bg-clip-text text-transparent">
            Alunos Dizem
          </span>
        </h2>

        <!-- Description -->
        <p class="font-body text-lg sm:text-xl text-neutral-300 max-w-3xl mx-auto leading-relaxed">
          Histórias reais de desenvolvedores que transformaram sua forma de programar 
          <span class="text-white">com a Componentização Extrema</span>.
        </p>
      </div>

      <!-- Testimonials Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
        <!-- Testimonial 1 -->
        <TestimonialCard
          name="Carlos Silva"
          role="Desenvolvedor Frontend"
          text="A metodologia mudou completamente minha forma de desenvolver. Meus projetos agora são muito mais organizados e fáceis de manter."
        />

        <!-- Testimonial 2 -->
        <TestimonialCard
          name="Ana Martins"
          role="Tech Lead"
          text="Incredible! Consegui implementar um sistema de gestão completo em apenas 3 semanas usando essa abordagem estruturada."
        />

        <!-- Testimonial 3 -->
        <TestimonialCard
          name="Pedro Santos"
          role="Freelancer"
          text="Meus clientes ficaram impressionados com a velocidade de entrega. O método realmente funciona para projetos de qualquer tamanho."
        />

        <!-- Testimonial 4 -->
        <TestimonialCard
          name="Mariana Costa"
          role="Desenvolvedora Full-Stack"
          text="Finalmente encontrei uma forma de usar IA para programar sem criar uma bagunça. O código fica limpo e profissional."
        />

        <!-- Testimonial 5 -->
        <TestimonialCard
          name="Roberto Lima"
          role="CTO Startup"
          text="Implementamos essa metodologia na nossa startup e conseguimos acelerar o desenvolvimento em 300%. Recomendo fortemente."
        />

        <!-- Testimonial 6 -->
        <TestimonialCard
          name="Julia Ferreira"
          role="Desenvolvedora Junior"
          text="Como iniciante, esse método me deu a confiança que precisava. Agora consigo criar aplicações complexas sem me perder no código."
        />
      </div>
      
    </div>

    <!-- Bottom gradient fade -->
    <div class="absolute bottom-0 left-0 right-0 h-20 bg-gradient-fade"></div>
  </section>
</template>

<script setup>
import Badge from '~/components/ui/Badge.vue'
import TestimonialCard from '~/components/ui/TestimonialCard.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>