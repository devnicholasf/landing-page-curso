<template>
  <div>
    <HeroSection />
    <VibeCodingSection />
    <MetodoSection />
    <ComponentizacaoSection />
    <PossibilidadesSection />
    <ConteudoCursoSection />
    <DepoimentosSection />
    <CheckoutSection />
    <FaqSection />
    <FooterSection />
  </div>
</template>

<script setup>
import HeroSection from '~/components/sections/HeroSection.vue'
import VibeCodingSection from '~/components/sections/VibeCodingSection.vue'
import MetodoSection from '~/components/sections/MetodoSection.vue'
import ComponentizacaoSection from '~/components/sections/ComponentizacaoSection.vue'
import PossibilidadesSection from '~/components/sections/PossibilidadesSection.vue'
import ConteudoCursoSection from '~/components/sections/ConteudoCursoSection.vue'
import DepoimentosSection from '~/components/sections/DepoimentosSection.vue'
import CheckoutSection from '~/components/sections/CheckoutSection.vue'
import FaqSection from '~/components/sections/FaqSection.vue'
import FooterSection from '~/components/sections/FooterSection.vue'

// Page meta
definePageMeta({
  title: 'Home - SaaS com IA'
})
</script>