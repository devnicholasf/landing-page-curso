<template>
  <div>
    <HeroSection />
    <MetodoSection />
  </div>
</template>

<script setup>
import HeroSection from '~/components/sections/HeroSection.vue'
import MetodoSection from '~/components/sections/MetodoSection.vue'

// Page meta
definePageMeta({
  title: 'Home - SaaS com IA'
})
</script>