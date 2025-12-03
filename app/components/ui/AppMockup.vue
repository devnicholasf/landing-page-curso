<template>
  <div class="relative w-full max-w-lg mx-auto">
    <!-- App Container -->
    <div class="bg-gradient-to-br from-primary-800 via-primary-700 to-primary-600 rounded-2xl p-6 shadow-2xl border border-white/10 backdrop-blur-md">
      <!-- App Header -->
      <div class="flex items-center justify-between mb-6 animate-slideInTop">
        <!-- Logo/Icon -->
        <div class="w-8 h-8 bg-secondary/20 rounded-lg flex items-center justify-center">
          <div class="w-4 h-4 bg-secondary rounded-sm"></div>
        </div>
        
        <!-- Navigation dots -->
        <div class="flex space-x-2">
          <div class="w-12 h-2 bg-white/20 rounded-full"></div>
          <div class="w-12 h-2 bg-white/20 rounded-full"></div>
          <div class="w-12 h-2 bg-white/20 rounded-full"></div>
        </div>
        
        <!-- Action button -->
        <div class="w-16 h-6 bg-secondary/80 rounded-md"></div>
      </div>

      <!-- Content Area -->
      <div class="space-y-4 mb-6 animate-slideInLeft">
        <!-- Title lines -->
        <div class="space-y-2">
          <div class="w-3/4 h-3 bg-white/40 rounded-full"></div>
          <div class="w-1/2 h-2 bg-white/25 rounded-full"></div>
        </div>
        
        <!-- Text content -->
        <div class="space-y-2">
          <div class="w-full h-2 bg-white/20 rounded-full"></div>
          <div class="w-5/6 h-2 bg-white/20 rounded-full"></div>
          <div class="w-2/3 h-2 bg-white/20 rounded-full"></div>
        </div>
      </div>

      <!-- Featured Component (highlighted in green) -->
      <div class="relative mb-6 animate-slideInRight">
        <div class="bg-secondary/10 border-2 border-secondary border-dashed rounded-xl p-4 relative">
          <div class="w-full h-16 bg-secondary/20 rounded-lg flex items-center justify-center">
            <div class="text-secondary text-xs font-medium">Componente Reutilizável</div>
          </div>
          <!-- Glow effect -->
          <div class="absolute inset-0 bg-secondary/5 rounded-xl blur-sm"></div>
        </div>
      </div>

      <!-- Grid of Components -->
      <div class="grid grid-cols-3 gap-3">
        <!-- Component 1 -->
        <div class="bg-white/10 rounded-lg h-16 flex items-center justify-center animate-slideInBottom1">
          <div class="w-8 h-8 bg-white/30 rounded"></div>
        </div>
        
        <!-- Component 2 -->
        <div class="bg-white/10 rounded-lg h-16 flex items-center justify-center animate-slideInBottom2">
          <div class="w-8 h-8 bg-white/30 rounded"></div>
        </div>
        
        <!-- Component 3 -->
        <div class="bg-white/10 rounded-lg h-16 flex items-center justify-center animate-slideInBottom3">
          <div class="w-8 h-8 bg-white/30 rounded"></div>
        </div>
      </div>

      <!-- Decorative elements -->
      <div class="absolute -top-2 -right-2 w-4 h-4 bg-secondary/30 rounded-full blur-sm"></div>
      <div class="absolute -bottom-1 -left-1 w-3 h-3 bg-secondary/40 rounded-full blur-sm"></div>
    </div>

    <!-- Outer glow -->
    <div class="absolute inset-0 bg-gradient-to-br from-secondary/10 via-transparent to-secondary/5 rounded-2xl blur-xl -z-10 opacity-70"></div>
    
    <!-- Floating component indicators -->
    <div class="absolute -top-3 left-8 w-2 h-2 bg-secondary rounded-full animate-pulse"></div>
    <div class="absolute -right-3 top-1/3 w-2 h-2 bg-secondary rounded-full animate-pulse delay-300"></div>
    <div class="absolute -left-3 bottom-1/3 w-2 h-2 bg-secondary rounded-full animate-pulse delay-700"></div>
  </div>
</template>

<script setup>
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>

<style scoped>
.animate-slideInTop {
  animation: slideInTop 8s ease-in-out infinite;
}

.animate-slideInLeft {
  animation: slideInLeft 8s ease-in-out 2s infinite;
}

.animate-slideInRight {
  animation: slideInRight 8s ease-in-out 4s infinite;
}

.animate-slideInBottom1 {
  animation: slideInBottom 8s ease-in-out 6s infinite;
}

.animate-slideInBottom2 {
  animation: slideInBottom 8s ease-in-out 8s infinite;
}

.animate-slideInBottom3 {
  animation: slideInBottom 8s ease-in-out 10s infinite;
}

@keyframes slideInTop {
  0%, 80%, 100% {
    opacity: 1;
    transform: translateY(0);
  }
  10%, 20% {
    opacity: 0.3;
    transform: translateY(-30px);
  }
}

@keyframes slideInLeft {
  0%, 80%, 100% {
    opacity: 1;
    transform: translateX(0);
  }
  10%, 20% {
    opacity: 0.3;
    transform: translateX(-40px);
  }
}

@keyframes slideInRight {
  0%, 80%, 100% {
    opacity: 1;
    transform: translateX(0);
  }
  10%, 20% {
    opacity: 0.3;
    transform: translateX(40px);
  }
}

@keyframes slideInBottom {
  0%, 80%, 100% {
    opacity: 1;
    transform: translateY(0);
  }
  10%, 20% {
    opacity: 0.3;
    transform: translateY(30px);
  }
}
</style>