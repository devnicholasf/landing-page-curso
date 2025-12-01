<template>
  <div class="relative max-w-4xl mx-auto">
    <!-- Video Container -->
    <div class="relative bg-gradient-to-br from-primary-800/20 via-primary-700/10 to-secondary/5 rounded-3xl p-1 backdrop-blur-sm border border-white/10">
      <!-- Inner container with better border -->
      <div class="relative bg-primary-900/40 rounded-[1.375rem] overflow-hidden border border-secondary/20 backdrop-blur-md">
        <!-- Video aspect ratio container -->
        <div class="relative w-full" style="aspect-ratio: 16 / 9;">
          <!-- YouTube iframe -->
          <iframe
            v-if="videoId"
            :src="youtubeUrl"
            :title="title"
            class="absolute inset-0 w-full h-full rounded-[1.25rem]"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
          
          <!-- Placeholder when no videoId -->
          <div
            v-else
            class="absolute inset-0 flex items-center justify-center bg-gradient-to-br from-primary-800 to-primary-900 rounded-[1.25rem]"
          >
            <div class="text-center">
              <div class="w-20 h-20 bg-secondary/20 rounded-full flex items-center justify-center mx-auto mb-4">
                <svg class="w-10 h-10 text-secondary" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M8 5v14l11-7z"/>
                </svg>
              </div>
              <p class="font-primary text-white/80 text-lg">Vídeo em breve</p>
            </div>
          </div>
        </div>

        <!-- Decorative elements -->
        <div class="absolute -top-2 -left-2 w-4 h-4 bg-secondary/30 rounded-full blur-sm"></div>
        <div class="absolute -top-1 -right-3 w-6 h-6 bg-secondary/20 rounded-full blur-sm"></div>
        <div class="absolute -bottom-3 -left-1 w-5 h-5 bg-secondary/25 rounded-full blur-sm"></div>
      </div>
    </div>

    <!-- Glow effect -->
    <div class="absolute inset-0 bg-gradient-to-r from-secondary/10 via-transparent to-secondary/10 rounded-3xl blur-xl -z-10 opacity-50"></div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  videoId: {
    type: String,
    default: ''
  },
  title: {
    type: String,
    default: 'Video Player'
  },
  autoplay: {
    type: Boolean,
    default: false
  }
})

// Generate YouTube embed URL
const youtubeUrl = computed(() => {
  if (!props.videoId) return ''
  const autoplayParam = props.autoplay ? '&autoplay=1' : ''
  return `https://www.youtube.com/embed/${props.videoId}?rel=0&modestbranding=1&showinfo=0${autoplayParam}`
})
</script>