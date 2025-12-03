<template>
  <div class="relative w-full max-w-2xl mx-auto">
    <!-- Chat Container -->
    <div class="bg-gradient-to-br from-primary-800 via-primary-700 to-primary-600 rounded-2xl shadow-2xl border border-white/10 backdrop-blur-md overflow-hidden">
      <!-- Chat Header -->
      <div class="bg-primary-900/60 px-6 py-4 border-b border-white/10 flex items-center justify-between">
        <div class="flex items-center space-x-3">
          <div class="w-3 h-3 bg-red-500 rounded-full"></div>
          <div class="w-3 h-3 bg-yellow-500 rounded-full"></div>
          <div class="w-3 h-3 bg-green-500 rounded-full"></div>
        </div>
        <h3 class="font-primary text-white text-sm font-medium">{{ titulo }}</h3>
        <div class="w-6 h-6 bg-secondary/20 rounded flex items-center justify-center">
          <span class="text-secondary text-xs">AI</span>
        </div>
      </div>

      <!-- Chat Content -->
      <div class="p-6 space-y-4 min-h-[300px]">
        <!-- User Message -->
        <div class="flex justify-end">
          <div class="max-w-xs bg-secondary/10 rounded-2xl rounded-br-md px-4 py-3 border border-secondary/20">
            <p class="font-body text-white text-sm leading-relaxed">
              {{ texto }}<span class="text-secondary animate-blink">|</span>
            </p>
          </div>
        </div>

        <!-- Typing Indicator (AI) -->
        <div class="flex justify-start">
          <div class="max-w-xs bg-white/5 rounded-2xl rounded-bl-md px-4 py-3 border border-white/10">
            <div class="flex space-x-1">
              <div class="w-2 h-2 bg-white/40 rounded-full animate-bounce"></div>
              <div class="w-2 h-2 bg-white/40 rounded-full animate-bounce delay-100"></div>
              <div class="w-2 h-2 bg-white/40 rounded-full animate-bounce delay-200"></div>
            </div>
          </div>
        </div>
      </div>

      <!-- Chat Input Area -->
      <div class="bg-primary-900/60 px-6 py-4 border-t border-white/10">
        <div class="flex items-center space-x-3">
          <div class="flex-1 bg-white/5 rounded-lg px-4 py-2 border border-white/10">
            <span class="font-body text-white/50 text-sm">Escreva sua mensagem...</span>
          </div>
          <button class="bg-secondary/80 hover:bg-secondary rounded-lg px-4 py-2 transition-colors">
            <svg class="w-4 h-4 text-primary" fill="currentColor" viewBox="0 0 24 24">
              <path d="M2.01 21L23 12 2.01 3 2 10l15 2-15 2z"/>
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Glow effect -->
    <div class="absolute inset-0 bg-gradient-to-br from-secondary/5 via-transparent to-secondary/5 rounded-2xl blur-xl -z-10 opacity-60"></div>
  </div>
</template>

<script setup>
const props = defineProps({
  titulo: {
    type: String,
    required: true
  },
  texto: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
@keyframes blink {
  0%, 50% {
    opacity: 1;
  }
  51%, 100% {
    opacity: 0;
  }
}

.animate-blink {
  animation: blink 1s infinite;
}
</style>