<template>
  <section class="relative py-16 bg-gradient-to-br from-primary-900 via-primary-800 to-primary-700 overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0">
      <div class="absolute top-10 right-10 w-64 h-64 bg-secondary/5 rounded-full blur-3xl"></div>
      <div class="absolute bottom-10 left-10 w-80 h-80 bg-primary-600/10 rounded-full blur-3xl"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-secondary/3 rounded-full blur-3xl"></div>
    </div>

    <!-- Main content -->
    <div class="relative z-10 container mx-auto px-6">
      <div class="max-w-4xl mx-auto">
        <!-- Section Header -->
        <div class="text-center mb-16">
          <!-- Badge -->
          <div class="flex justify-center mb-8">
            <Badge text="Dúvidas Frequentes" />
          </div>

          <!-- Title -->
          <h2 class="font-primary text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-black mb-6 leading-tight">
            <span class="text-white">Perguntas </span>
            <span class="bg-gradient-to-r from-secondary via-secondary-400 to-secondary-600 bg-clip-text text-transparent">
              Frequentes
            </span>
          </h2>

          <!-- Subtitle -->
          <p class="font-body text-lg sm:text-xl text-neutral-300 max-w-2xl mx-auto">
            Tire suas dúvidas sobre o curso e o processo de compra
          </p>
        </div>

        <!-- FAQ Items -->
        <div class="space-y-6">
          <!-- Question 1 -->
          <div class="bg-primary-800/50 border-2 border-primary-600/30 rounded-2xl overflow-hidden shadow-lg hover:shadow-xl hover:border-secondary/50 transition-all duration-300">
            <button 
              @click="toggleFaq(1)"
              class="w-full px-8 py-6 text-left flex justify-between items-center hover:bg-primary-700/30 transition-colors duration-200"
            >
              <h3 class="font-primary text-lg sm:text-xl font-bold text-white pr-4">
                1. Como tenho acesso ao curso?
              </h3>
              <svg 
                :class="{'rotate-180': openFaq === 1}"
                class="w-6 h-6 text-secondary transform transition-transform duration-300 flex-shrink-0"
                fill="none" 
                stroke="currentColor" 
                viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
              </svg>
            </button>
            <div 
              :class="{'max-h-0 opacity-0': openFaq !== 1, 'max-h-96 opacity-100': openFaq === 1}"
              class="overflow-hidden transition-all duration-300"
            >
              <div class="px-8 pb-6">
                <div class="bg-gradient-to-r from-primary-700/30 to-primary-600/20 rounded-lg p-6 border border-primary-500/20">
                  <p class="font-body text-neutral-200 leading-relaxed">
                    Após a confirmação do pagamento, <span class="font-semibold text-white">todos os dados de acesso são enviados automaticamente por email</span> em até 5 minutos. Você receberá:
                  </p>
                  <ul class="mt-4 space-y-2 text-neutral-200">
                    <li class="flex items-center space-x-3">
                      <svg class="w-4 h-4 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                      </svg>
                      <span>Link da plataforma de ensino</span>
                    </li>
                    <li class="flex items-center space-x-3">
                      <svg class="w-4 h-4 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                      </svg>
                      <span>Usuário e senha personalizados</span>
                    </li>
                    <li class="flex items-center space-x-3">
                      <svg class="w-4 h-4 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                      </svg>
                      <span>Acesso à comunidade exclusiva</span>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>

          <!-- Question 2 -->
          <div class="bg-primary-800/50 border-2 border-primary-600/30 rounded-2xl overflow-hidden shadow-lg hover:shadow-xl hover:border-secondary/50 transition-all duration-300">
            <button 
              @click="toggleFaq(2)"
              class="w-full px-8 py-6 text-left flex justify-between items-center hover:bg-primary-700/30 transition-colors duration-200"
            >
              <h3 class="font-primary text-lg sm:text-xl font-bold text-white pr-4">
                2. Qual o tempo de acesso ao curso?
              </h3>
              <svg 
                :class="{'rotate-180': openFaq === 2}"
                class="w-6 h-6 text-secondary transform transition-transform duration-300 flex-shrink-0"
                fill="none" 
                stroke="currentColor" 
                viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
              </svg>
            </button>
            <div 
              :class="{'max-h-0 opacity-0': openFaq !== 2, 'max-h-96 opacity-100': openFaq === 2}"
              class="overflow-hidden transition-all duration-300"
            >
              <div class="px-8 pb-6">
                <div class="bg-gradient-to-r from-primary-700/30 to-primary-600/20 rounded-lg p-6 border border-primary-500/20">
                  <p class="font-body text-neutral-200 leading-relaxed mb-4">
                    <span class="font-semibold text-white text-xl">12 meses de acesso completo</span> a todo o conteúdo do curso, incluindo:
                  </p>
                  <ul class="space-y-2 text-neutral-200">
                    <li class="flex items-center space-x-3">
                      <svg class="w-4 h-4 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                      </svg>
                      <span>Todas as aulas e módulos</span>
                    </li>
                    <li class="flex items-center space-x-3">
                      <svg class="w-4 h-4 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                      </svg>
                      <span>Materiais complementares</span>
                    </li>
                    <li class="flex items-center space-x-3">
                      <svg class="w-4 h-4 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                      </svg>
                      <span>Atualizações e novos conteúdos</span>
                    </li>
                    <li class="flex items-center space-x-3">
                      <svg class="w-4 h-4 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                      </svg>
                      <span>Suporte da comunidade</span>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>

          <!-- Question 3 -->
          <div class="bg-primary-800/50 border-2 border-primary-600/30 rounded-2xl overflow-hidden shadow-lg hover:shadow-xl hover:border-secondary/50 transition-all duration-300">
            <button 
              @click="toggleFaq(3)"
              class="w-full px-8 py-6 text-left flex justify-between items-center hover:bg-primary-700/30 transition-colors duration-200"
            >
              <h3 class="font-primary text-lg sm:text-xl font-bold text-white pr-4">
                3. Como funciona a garantia?
              </h3>
              <svg 
                :class="{'rotate-180': openFaq === 3}"
                class="w-6 h-6 text-secondary transform transition-transform duration-300 flex-shrink-0"
                fill="none" 
                stroke="currentColor" 
                viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
              </svg>
            </button>
            <div 
              :class="{'max-h-0 opacity-0': openFaq !== 3, 'max-h-96 opacity-100': openFaq === 3}"
              class="overflow-hidden transition-all duration-300"
            >
              <div class="px-8 pb-6">
                <div class="bg-gradient-to-r from-secondary/10 to-primary-600/20 rounded-lg p-6 border border-secondary/30">
                  <div class="flex items-center space-x-3 mb-4">
                    <svg class="w-8 h-8 text-secondary" fill="currentColor" viewBox="0 0 24 24">
                      <path d="M12,1L3,5V11C3,16.55 6.84,21.74 12,23C17.16,21.74 21,16.55 21,11V5L12,1M10,17L6,13L7.41,11.59L10,14.17L16.59,7.58L18,9V17H10Z"/>
                    </svg>
                    <h4 class="font-primary font-bold text-white text-lg">Garantia de 7 dias</h4>
                  </div>
                  <p class="font-body text-neutral-200 leading-relaxed mb-4">
                    <span class="font-semibold text-secondary">Você tem 7 dias corridos</span> para acessar a plataforma, explorar o conteúdo e avaliar se o curso atende às suas expectativas.
                  </p>
                  <p class="font-body text-neutral-200 leading-relaxed mb-4">
                    <span class="font-semibold text-white">Caso o curso não atinja suas expectativas</span>, você pode solicitar o reembolso integral através do nosso suporte, sem questionamentos e sem burocracia.
                  </p>
                  <div class="bg-primary-700/30 rounded-lg p-4 border-l-4 border-secondary">
                    <p class="text-sm text-secondary font-medium">
                      💡 <strong>Processo simples:</strong> Envie um email para suporte@curso.com com o assunto "Solicitação de Reembolso" e seu pedido será processado em até 48h.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Question 4 -->
          <div class="bg-primary-800/50 border-2 border-primary-600/30 rounded-2xl overflow-hidden shadow-lg hover:shadow-xl hover:border-secondary/50 transition-all duration-300">
            <button 
              @click="toggleFaq(4)"
              class="w-full px-8 py-6 text-left flex justify-between items-center hover:bg-primary-700/30 transition-colors duration-200"
            >
              <h3 class="font-primary text-lg sm:text-xl font-bold text-white pr-4">
                4. Preciso ter experiência prévia?
              </h3>
              <svg 
                :class="{'rotate-180': openFaq === 4}"
                class="w-6 h-6 text-secondary transform transition-transform duration-300 flex-shrink-0"
                fill="none" 
                stroke="currentColor" 
                viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
              </svg>
            </button>
            <div 
              :class="{'max-h-0 opacity-0': openFaq !== 4, 'max-h-96 opacity-100': openFaq === 4}"
              class="overflow-hidden transition-all duration-300"
            >
              <div class="px-8 pb-6">
                <div class="bg-gradient-to-r from-primary-700/30 to-primary-600/20 rounded-lg p-6 border border-primary-500/20">
                  <p class="font-body text-neutral-200 leading-relaxed mb-4">
                    <span class="font-semibold text-secondary">Não é necessário ter experiência prévia!</span> O curso foi desenvolvido para atender desde iniciantes até desenvolvedores experientes.
                  </p>
                  <p class="font-body text-neutral-200 leading-relaxed">
                    Recomendamos apenas conhecimentos básicos de HTML, CSS e JavaScript. Todo o resto será ensinado do zero, seguindo a metodologia de Componentização Extrema.
                  </p>
                </div>
              </div>
            </div>
          </div>

          <!-- Question 5 -->
          <div class="bg-primary-800/50 border-2 border-primary-600/30 rounded-2xl overflow-hidden shadow-lg hover:shadow-xl hover:border-secondary/50 transition-all duration-300">
            <button 
              @click="toggleFaq(5)"
              class="w-full px-8 py-6 text-left flex justify-between items-center hover:bg-primary-700/30 transition-colors duration-200"
            >
              <h3 class="font-primary text-lg sm:text-xl font-bold text-white pr-4">
                5. Quando o curso estará disponível?
              </h3>
              <svg 
                :class="{'rotate-180': openFaq === 5}"
                class="w-6 h-6 text-secondary transform transition-transform duration-300 flex-shrink-0"
                fill="none" 
                stroke="currentColor" 
                viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
              </svg>
            </button>
            <div 
              :class="{'max-h-0 opacity-0': openFaq !== 5, 'max-h-96 opacity-100': openFaq === 5}"
              class="overflow-hidden transition-all duration-300"
            >
              <div class="px-8 pb-6">
                <div class="bg-gradient-to-r from-primary-700/30 to-primary-600/20 rounded-lg p-6 border border-primary-500/20">
                  <p class="font-body text-neutral-200 leading-relaxed mb-4">
                    <span class="font-semibold text-secondary">O curso está em desenvolvimento ativo</span> e será lançado progressivamente. Os primeiros módulos já estão disponíveis!
                  </p>
                  <p class="font-body text-neutral-200 leading-relaxed">
                    Ao comprar agora, você acompanha todo o desenvolvimento, recebe os conteúdos conforme são lançados e ainda garante o preço especial de pré-lançamento.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import Badge from '~/components/ui/Badge.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})

// Reactive state
const openFaq = ref(null)

// Methods
const toggleFaq = (index) => {
  openFaq.value = openFaq.value === index ? null : index
}
</script>