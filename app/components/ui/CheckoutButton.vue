<template>
  <button 
    :class="[
      'group relative overflow-hidden',
      'bg-gradient-to-r from-secondary to-secondary-600 hover:from-secondary-400 hover:to-secondary-500',
      'text-white font-bold',
      'px-8 py-4 rounded-xl',
      'shadow-lg shadow-secondary/25 hover:shadow-xl hover:shadow-secondary/40',
      'transform hover:scale-105 active:scale-95',
      'transition-all duration-200',
      'border border-secondary-400/50',
      className
    ]"
    @click="$emit('click')"
  >
    <!-- Background Animation -->
    <div class="absolute inset-0 bg-gradient-to-r from-white/0 via-white/20 to-white/0 translate-x-[-200%] group-hover:translate-x-[200%] transition-transform duration-700"></div>
    
    <!-- Button Content -->
    <div class="relative flex items-center justify-center space-x-3">
      <!-- Icon -->
      <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
        <path d="M7,18C7.56,18 8,18.44 8,19C8,19.56 7.56,20 7,20C6.44,20 6,19.56 6,19C6,18.44 6.44,18 7,18M1,2V4H3L6.6,11.59L5.24,14.04C5.09,14.32 5,14.65 5,15C5,16.1 5.9,17 7,17H19V15H7.42C7.28,15 7.17,14.89 7.17,14.75L7.2,14.63L8.1,13H15.55C16.3,13 16.96,12.58 17.3,11.97L20.88,5H5.21L4.27,3H1M17,18C17.56,18 18,18.44 18,19C18,19.56 17.56,20 17,20C16.44,20 16,19.56 16,19C16,18.44 16.44,18 17,18Z"/>
      </svg>
      
      <!-- Text -->
      <span class="text-lg">{{ text }}</span>
      
      <!-- Arrow -->
      <svg class="w-5 h-5 transform group-hover:translate-x-1 transition-transform" fill="currentColor" viewBox="0 0 24 24">
        <path d="M4,11V13H16L10.5,18.5L11.92,19.92L19.84,12L11.92,4.08L10.5,5.5L16,11H4Z"/>
      </svg>
    </div>
  </button>
</template>

<script setup>
// Props
const props = defineProps({
  text: {
    type: String,
    default: 'Comprar Agora'
  },
  className: {
    type: String,
    default: ''
  }
})

// Emits
defineEmits(['click'])
</script>