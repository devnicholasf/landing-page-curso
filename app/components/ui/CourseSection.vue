<template>
  <div class="border border-neutral-600 rounded-xl bg-gradient-to-br from-primary-800 to-primary-900 overflow-hidden">
    <!-- Section Header -->
    <div 
      @click="toggleExpanded" 
      class="flex items-start sm:items-center justify-between p-4 sm:p-6 cursor-pointer hover:bg-primary-700/30 transition-colors"
    >
      <div class="flex items-start sm:items-center space-x-3 sm:space-x-4 flex-1 min-w-0">
        <!-- Section Number -->
        <div class="w-10 h-10 sm:w-10 sm:h-10 bg-gradient-to-br from-secondary to-secondary-600 rounded-lg flex items-center justify-center font-bold text-white text-lg shadow-md flex-shrink-0">
          {{ sectionNumber }}
        </div>
        
        <!-- Section Info -->
        <div class="flex-1 min-w-0">
          <h3 class="font-primary text-lg sm:text-xl font-bold text-white mb-1 break-words">{{ title }}</h3>
          <p class="font-body text-xs sm:text-sm text-neutral-300 break-words">{{ description }}</p>
        </div>
      </div>
      
      <!-- Expand Icon -->
      <div class="transform transition-transform duration-300 flex-shrink-0 ml-2" :class="{ 'rotate-180': isExpanded }">
        <svg class="w-5 h-5 sm:w-6 sm:h-6 text-neutral-400" fill="currentColor" viewBox="0 0 24 24">
          <path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z"/>
        </svg>
      </div>
    </div>

    <!-- Expandable Content -->
    <div 
      class="transition-all duration-300 ease-in-out overflow-hidden"
      :class="isExpanded ? 'max-h-screen opacity-100' : 'max-h-0 opacity-0'"
    >
      <div class="px-4 sm:px-6 pb-4 sm:pb-6">
        <div class="space-y-3">
          <div 
            v-for="module in modules" 
            :key="module.title"
            class="flex items-start sm:items-center justify-between p-3 sm:p-4 bg-primary-950/50 rounded-lg border border-neutral-700/50 hover:border-secondary/30 transition-colors group"
          >
            <div class="flex items-start sm:items-center space-x-3 flex-1 min-w-0">
              <!-- Module Icon -->
              <div class="w-7 h-7 sm:w-8 sm:h-8 bg-gradient-to-br from-neutral-600 to-neutral-700 rounded-lg flex items-center justify-center group-hover:from-secondary/20 group-hover:to-secondary/30 transition-colors flex-shrink-0 mt-0.5 sm:mt-0">
                <svg class="w-3 h-3 sm:w-4 sm:h-4 text-neutral-300 group-hover:text-secondary transition-colors" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M8,5.14V19.14L19,12.14L8,5.14Z"/>
                </svg>
              </div>
              
              <!-- Module Info -->
              <div class="flex-1 min-w-0">
                <h4 class="font-medium text-white group-hover:text-secondary transition-colors text-sm sm:text-base break-words">{{ module.title }}</h4>
                <p class="text-xs text-neutral-400 group-hover:text-neutral-300 transition-colors break-words">{{ module.description }}</p>
              </div>
            </div>
            
            <!-- Status Badge -->
            <div class="flex items-center space-x-2 flex-shrink-0 ml-2">
              <span 
                class="px-2 py-1 text-xs font-medium rounded-full whitespace-nowrap"
                :class="module.status === 'LIBERADO' ? 'bg-green-500/20 text-green-400 border border-green-500/30' : 'bg-yellow-500/20 text-yellow-400 border border-yellow-500/30'"
              >
                {{ module.status }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// Props
const props = defineProps({
  sectionNumber: {
    type: [String, Number],
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  modules: {
    type: Array,
    default: () => []
  },
  initialExpanded: {
    type: Boolean,
    default: false
  }
})

// Reactive state
const isExpanded = ref(props.initialExpanded)

// Methods
const toggleExpanded = () => {
  isExpanded.value = !isExpanded.value
}
</script>