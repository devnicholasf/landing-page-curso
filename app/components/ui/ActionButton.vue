<template>
  <button
    @click="scrollToCheckout"
    class="bg-secondary hover:bg-secondary/90 text-primary font-primary font-semibold py-4 px-12 text-lg rounded-xl transition-all duration-200 shadow-lg hover:shadow-xl transform hover:scale-105 active:scale-95"
  >
    {{ texto }}
  </button>
</template>

<script setup>
const props = defineProps({
  texto: {
    type: String,
    required: true
  }
})

// Method to scroll to checkout section
const scrollToCheckout = () => {
  const checkoutElement = document.getElementById('checkout')
  if (checkoutElement) {
    checkoutElement.scrollIntoView({ 
      behavior: 'smooth',
      block: 'start'
    })
  }
}
</script>