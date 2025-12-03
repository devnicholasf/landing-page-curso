<template>
  <div>
    <HeroSection />
    <VibeCodingSection />
    <MetodoSection />
  </div>
</template>

<script setup>
import HeroSection from '~/components/sections/HeroSection.vue'
import VibeCodingSection from '~/components/sections/VibeCodingSection.vue'
import MetodoSection from '~/components/sections/MetodoSection.vue'

// Page meta
definePageMeta({
  title: 'Home - SaaS com IA'
})
</script>