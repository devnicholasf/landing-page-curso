<template>
  <div class="bg-gradient-to-br from-primary-800 to-primary-900 border border-neutral-600 rounded-xl p-6 shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105">
    <!-- Quote Icon -->
    <div class="mb-4">
      <svg class="w-8 h-8 text-secondary/60" fill="currentColor" viewBox="0 0 24 24">
        <path d="M14,17H17L19,13V7H13V13H16M6,17H9L11,13V7H5V13H8L6,17Z"/>
      </svg>
    </div>

    <!-- Testimonial Text -->
    <p class="font-body text-neutral-200 leading-relaxed mb-6 italic">
      "{{ text }}"
    </p>

    <!-- User Info -->
    <div class="flex items-center space-x-4">
      <!-- Avatar -->
      <div class="w-12 h-12 bg-gradient-to-br from-secondary to-secondary-600 rounded-full flex items-center justify-center text-white font-bold text-lg shadow-md">
        {{ avatarInitials }}
      </div>
      
      <!-- Name and Role -->
      <div>
        <h4 class="font-primary font-semibold text-white">{{ name }}</h4>
        <p class="font-body text-sm text-neutral-400">{{ role }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

// Props
const props = defineProps({
  name: {
    type: String,
    required: true
  },
  role: {
    type: String,
    required: true
  },
  text: {
    type: String,
    required: true
  }
})

// Computed avatar initials
const avatarInitials = computed(() => {
  return props.name
    .split(' ')
    .map(word => word.charAt(0))
    .join('')
    .toUpperCase()
    .slice(0, 2)
})
</script>