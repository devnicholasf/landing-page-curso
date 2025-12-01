<template>
  <div class="inline-flex items-center bg-secondary/10 border border-secondary/30 rounded-full px-4 py-2 backdrop-blur-sm">
    <span class="font-primary text-sm font-medium text-secondary">
      {{ text }}
    </span>
  </div>
</template>

<script setup>
const props = defineProps({
  text: {
    type: String,
    required: true
  }
})
</script>