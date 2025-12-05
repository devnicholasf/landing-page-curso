<template>
  <div>
    <HeroSection />
    <VibeCodingSection />
    <MetodoSection />
    <ComponentizacaoSection />
    <PossibilidadesSection />
  </div>
</template>

<script setup>
import HeroSection from '~/components/sections/HeroSection.vue'
import VibeCodingSection from '~/components/sections/VibeCodingSection.vue'
import MetodoSection from '~/components/sections/MetodoSection.vue'
import ComponentizacaoSection from '~/components/sections/ComponentizacaoSection.vue'
import PossibilidadesSection from '~/components/sections/PossibilidadesSection.vue'

// Page meta
definePageMeta({
  title: 'Home - SaaS com IA'
})
</script>