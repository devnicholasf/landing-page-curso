<template>
  <section id="checkout" class="relative py-20 bg-gradient-to-br from-primary-900 via-primary-800 to-primary-700 overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0">
      <div class="absolute top-10 left-10 w-96 h-96 bg-secondary/3 rounded-full blur-3xl"></div>
      <div class="absolute bottom-10 right-10 w-80 h-80 bg-secondary/5 rounded-full blur-3xl"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-72 h-72 bg-green-500/3 rounded-full blur-3xl"></div>
    </div>

    <!-- Main content -->
    <div class="relative z-10 container mx-auto px-6">
      <div class="max-w-4xl mx-auto">
        <!-- Section Header -->
        <div class="text-center mb-12">
          <!-- Badge -->
          <div class="flex justify-center mb-8">
            <Badge text="🔥 Pré-Lançamento" />
          </div>

          <!-- Title -->
          <h2 class="font-primary text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-black mb-6 leading-tight">
            <span class="text-white">Garanta Seu </span>
            <span class="bg-gradient-to-r from-secondary via-secondary-400 to-secondary-600 bg-clip-text text-transparent">
              Acesso
            </span>
          </h2>

          <!-- Urgency -->
          <p class="font-body text-lg sm:text-xl text-neutral-200 mb-8">
            <span class="text-yellow-400 font-semibold">Últimas vagas</span> com preço especial de pré-lançamento
          </p>
        </div>

        <!-- Checkout Card -->
        <div class="bg-gradient-to-br from-primary-800 to-primary-900 border-2 border-secondary/30 rounded-3xl p-8 sm:p-12 shadow-2xl shadow-secondary/10">
          
          <!-- Course Info -->
          <div class="text-center mb-8">
            <h3 class="font-primary text-2xl sm:text-3xl font-bold text-white mb-4">
              Curso Componentização Extrema
            </h3>
            <p class="text-neutral-300 text-lg mb-6">
              Do Zero ao Deploy • Metodologia Completa • Projetos Práticos
            </p>
            
            <!-- Features List -->
            <div class="grid sm:grid-cols-2 gap-4 max-w-2xl mx-auto mb-8">
              <div class="flex items-center space-x-3">
                <svg class="w-5 h-5 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                </svg>
                <span class="text-neutral-200 text-sm">5 módulos completos</span>
              </div>
              <div class="flex items-center space-x-3">
                <svg class="w-5 h-5 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                </svg>
                <span class="text-neutral-200 text-sm">Projetos práticos</span>
              </div>
              <div class="flex items-center space-x-3">
                <svg class="w-5 h-5 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                </svg>
                <span class="text-neutral-200 text-sm">Suporte da comunidade</span>
              </div>
              <div class="flex items-center space-x-3">
                <svg class="w-5 h-5 text-secondary flex-shrink-0" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                </svg>
                <span class="text-neutral-200 text-sm">Acesso durante 12 meses</span>
              </div>
            </div>
          </div>

          <!-- Pricing -->
          <div class="text-center mb-8">
            <!-- Original Price -->
            <div class="mb-4">
              <span class="text-neutral-400 text-lg line-through">De R$ 1.497</span>
            </div>
            
            <!-- Discount Banner -->
            <div class="bg-gradient-to-r from-red-600 to-red-700 text-white text-sm font-bold px-4 py-2 rounded-full inline-block mb-6">
              🎯 67% OFF - APENAS PRÉ-LANÇAMENTO
            </div>

            <!-- Current Price -->
            <div class="mb-6">
              <div class="text-5xl sm:text-6xl font-black text-secondary mb-2">
                R$ 497
              </div>
              <div class="text-neutral-300 text-lg">
                ou <span class="text-white font-semibold">12x de R$ 41,42</span> sem juros
              </div>
            </div>

            <!-- Savings -->
            <div class="bg-green-600/20 border border-green-500/30 rounded-lg p-4 mb-8">
              <p class="text-green-400 font-semibold">
                💰 Você economiza <span class="text-green-300 text-xl">R$ 1.000</span> comprando agora!
              </p>
            </div>
          </div>

          <!-- CTA -->
          <div class="text-center">
            <CheckoutButton 
              text="🚀 Comprar Agora por R$ 497"
              className="w-full sm:w-auto text-xl"
              @click="handlePurchase"
            />
            
            <!-- Security Info -->
            <div class="flex flex-wrap justify-center items-center gap-4 mt-6 text-neutral-400 text-sm">
              <div class="flex items-center space-x-2">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12,1L3,5V11C3,16.55 6.84,21.74 12,23C17.16,21.74 21,16.55 21,11V5L12,1M12,7C13.4,7 14.8,8.6 14.8,10V11.5C15.4,11.5 16,12.4 16,13V16C16,17.4 15.4,18 14.8,18H9.2C8.6,18 8,17.4 8,16V13C8,12.4 8.6,11.5 9.2,11.5V10C9.2,8.6 10.6,7 12,7M12,8.2C11.2,8.2 10.5,8.7 10.5,10V11.5H13.5V10C13.5,8.7 12.8,8.2 12,8.2Z"/>
                </svg>
                <span>Compra 100% Segura</span>
              </div>
              <div class="flex items-center space-x-2">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M9,20.42L2.79,14.21L5.62,11.38L9,14.77L18.88,4.88L21.71,7.71L9,20.42Z"/>
                </svg>
                <span>Garantia de 7 dias</span>
              </div>
              <div class="flex items-center space-x-2">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12,2C6.48,2 2,6.48 2,12C2,17.52 6.48,22 12,22C17.52,22 22,17.52 22,12C22,6.48 17.52,2 12,2M12,20C7.59,20 4,16.41 4,12C4,7.59 7.59,4 12,4C16.41,4 20,7.59 20,12C20,16.41 16.41,20 12,20M12,6A6,6 0 0,0 6,12A6,6 0 0,0 12,18A6,6 0 0,0 18,12A6,6 0 0,0 12,6M12,16A4,4 0 0,1 8,12A4,4 0 0,1 12,8A4,4 0 0,1 16,12A4,4 0 0,1 12,16Z"/>
                </svg>
                <span>Suporte Premium</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Bottom Warning -->
        <div class="text-center mt-8">
          <p class="text-neutral-300 text-sm">
            ⚠️ <span class="text-yellow-400 font-semibold">Atenção:</span> Este preço especial é válido apenas durante o pré-lançamento. 
            Após o lançamento oficial, o curso retornará ao valor integral de R$ 1.497.
          </p>
        </div>
      </div>
    </div>

    <!-- Bottom gradient fade -->
    <div class="absolute bottom-0 left-0 right-0 h-20 bg-gradient-fade"></div>
  </section>
</template>

<script setup>
import Badge from '~/components/ui/Badge.vue'
import CheckoutButton from '~/components/ui/CheckoutButton.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})

// Methods
const handlePurchase = () => {
  // Aqui você pode adicionar a lógica de compra/redirecionamento
  console.log('Iniciando processo de compra...')
  // Exemplo: window.open('https://link-de-pagamento.com', '_blank')
}
</script>