<template>
  <div class="group cursor-pointer h-full">
    <div class="bg-gradient-to-br from-primary-800 to-primary-900 border border-neutral-600 rounded-xl p-6 shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 hover:border-secondary/50 h-full flex flex-col">
      <!-- Icon -->
      <div :class="iconBgClass" class="w-12 h-12 rounded-lg flex items-center justify-center mb-4 shadow-md group-hover:shadow-lg transition-all duration-300 flex-shrink-0">
        <!-- Document Icon -->
        <svg v-if="icon === 'document'" class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
          <path d="M14,2H6A2,2 0 0,0 4,4V20A2,2 0 0,0 6,22H18A2,2 0 0,0 20,20V8L14,2M18,20H6V4H13V9H18V20Z"/>
        </svg>
        
        <!-- Chart/Dashboard Icon -->
        <svg v-else-if="icon === 'chart' || icon === 'dashboard'" class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
          <path d="M13,3V9H21V3M13,21H21V11H13M3,21H11V15H3M3,13H11V3H3V13Z"/>
        </svg>
        
        <!-- Shopping Icon -->
        <svg v-else-if="icon === 'shopping'" class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
          <path d="M17,18C17.56,18 18,18.44 18,19C18,19.56 17.56,20 17,20C16.44,20 16,19.56 16,19C16,18.44 16.44,18 17,18M1,2V4H3L6.6,11.59L5.24,14.04C5.09,14.32 5,14.65 5,15C5,16.1 5.9,17 7,17H19V15H7.42C7.28,15 7.17,14.89 7.17,14.75L7.2,14.63L8.1,13H15.55C16.3,13 16.96,12.58 17.3,11.97L20.88,5H5.21L4.27,3H1M7,18C7.56,18 8,18.44 8,19C8,19.56 7.56,20 7,20C6.44,20 6,19.56 6,19C6,18.44 6.44,18 7,18Z"/>
        </svg>
        
        <!-- Health Icon -->
        <svg v-else-if="icon === 'health'" class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
          <path d="M12,2L13.09,8.26L22,9L13.09,9.74L12,16L10.91,9.74L2,9L10.91,8.26L12,2M6.5,14.5L7.5,12H9.5L8.5,14.5L11,15.5L8.5,16.5L7.5,19H5.5L6.5,16.5L4,15.5L6.5,14.5Z"/>
        </svg>
        
        <!-- Social Icon -->
        <svg v-else-if="icon === 'social'" class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
          <path d="M12,2C13.1,2 14,2.9 14,4C14,5.1 13.1,6 12,6C10.9,6 10,5.1 10,4C10,2.9 10.9,2 12,2M21,9V20A2,2 0 0,1 19,22H5A2,2 0 0,1 3,20V9C3,7.9 3.9,7 5,7H8C8.6,7 9.1,7.4 9.4,8H14.6C14.9,7.4 15.4,7 16,7H19C20.1,7 21,7.9 21,9Z"/>
        </svg>
        
        <!-- Users Icon -->
        <svg v-else-if="icon === 'users'" class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
          <path d="M16,4C18.21,4 20,5.79 20,8C20,10.21 18.21,12 16,12C13.79,12 12,10.21 12,8C12,5.79 13.79,4 16,4M16,14C18.67,14 24,15.33 24,18V20H8V18C8,15.33 13.33,14 16,14M8,4C10.21,4 12,5.79 12,8C12,10.21 10.21,12 8,12C5.79,12 4,10.21 4,8C4,5.79 5.79,4 8,4M8,14C10.67,14 16,15.33 16,18V20H0V18C0,15.33 5.33,14 8,14Z"/>
        </svg>
        
        <!-- Mobile Icon -->
        <svg v-else-if="icon === 'mobile'" class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
          <path d="M17,19H7V5H17V19M17,1H7A2,2 0 0,0 5,3V21A2,2 0 0,0 7,23H17A2,2 0 0,0 19,21V3A2,2 0 0,0 17,1M9,18H15V6H9V18Z"/>
        </svg>
        
        <!-- Default Icon -->
        <svg v-else class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
          <path d="M9,3V4H4V6H5V19A2,2 0 0,0 7,21H17A2,2 0 0,0 19,19V6H20V4H15V3H9M7,6H17V19H7V6M9,8V17H11V8H9M13,8V17H15V8H13Z"/>
        </svg>
      </div>
      
      <!-- Title -->
      <h3 class="font-primary text-lg font-bold text-white mb-2 group-hover:text-secondary transition-colors flex-shrink-0">
        {{ title }}
      </h3>
      
      <!-- Description -->
      <p class="font-body text-sm text-neutral-300 leading-relaxed group-hover:text-neutral-200 transition-colors flex-grow">
        {{ description }}
      </p>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

// Props
const props = defineProps({
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    default: 'document'
  }
})

// Icon background colors for visual variety
const iconBgClass = computed(() => {
  const colorMap = {
    dashboard: 'bg-gradient-to-br from-blue-500 to-blue-600 group-hover:from-blue-400 group-hover:to-blue-500',
    shopping: 'bg-gradient-to-br from-purple-500 to-purple-600 group-hover:from-purple-400 group-hover:to-purple-500',
    health: 'bg-gradient-to-br from-red-500 to-red-600 group-hover:from-red-400 group-hover:to-red-500',
    social: 'bg-gradient-to-br from-pink-500 to-pink-600 group-hover:from-pink-400 group-hover:to-pink-500',
    mobile: 'bg-gradient-to-br from-orange-500 to-orange-600 group-hover:from-orange-400 group-hover:to-orange-500',
    users: 'bg-gradient-to-br from-indigo-500 to-indigo-600 group-hover:from-indigo-400 group-hover:to-indigo-500',
    document: 'bg-gradient-to-br from-green-500 to-green-600 group-hover:from-green-400 group-hover:to-green-500',
    chart: 'bg-gradient-to-br from-yellow-500 to-yellow-600 group-hover:from-yellow-400 group-hover:to-yellow-500'
  }
  
  return colorMap[props.icon] || colorMap.document
})
</script>