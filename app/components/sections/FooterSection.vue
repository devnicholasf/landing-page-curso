<template>
  <footer class="bg-gradient-to-br from-primary-950 via-primary-900 to-primary-800 border-t border-primary-700/30 py-4">
    <!-- Main content -->
    <div class="container mx-auto px-6">
      <div class="text-center">
        <!-- Copyright -->
        <p class="text-neutral-400 text-sm leading-relaxed">
          Copyright © 2025 <span class="text-white font-medium">NF AICoding LTDA</span>. 
          <span class="text-neutral-500">CNPJ:</span> 
          <span class="text-neutral-300"> 27.159.855/0001-16</span> • 
          <span class="text-neutral-300">Fortaleza - Brasil</span>
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>