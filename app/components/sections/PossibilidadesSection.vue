<template>
  <section class="relative py-20 bg-gradient-to-br from-primary-900 via-primary-800 to-primary-700 overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0">
      <div class="absolute top-20 right-20 w-64 h-64 bg-secondary/5 rounded-full blur-3xl"></div>
      <div class="absolute bottom-20 left-20 w-80 h-80 bg-primary-600/10 rounded-full blur-3xl"></div>
    </div>

    <!-- Main content -->
    <div class="relative z-10 container mx-auto px-6">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <!-- Badge -->
        <div class="flex justify-center mb-8">
          <Badge text="Possibilidades Infinitas" />
        </div>

        <!-- Title -->
        <h2 class="font-primary text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-black mb-6 leading-tight">
          <span class="text-white">Qualquer </span>
          <span class="bg-gradient-to-r from-secondary via-secondary-400 to-secondary-600 bg-clip-text text-transparent">
            Aplicação
          </span>
          <span class="text-white"> que Imaginar</span>
        </h2>

        <!-- Description -->
        <p class="font-body text-lg sm:text-xl text-neutral-300 max-w-3xl mx-auto leading-relaxed">
          Com a metodologia de <span class="text-secondary">Componentização Extrema</span>, você pode criar qualquer tipo de aplicação. 
          <span class="text-white">Desde sistemas complexos de gestão até apps inovadores</span>, 
          nossa abordagem estruturada garante código limpo e escalável para qualquer projeto.
        </p>
      </div>

      <!-- Apps Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
        <!-- Gestão Empresarial -->
        <AppTypeCard
          title="Gestão Empresarial"
          description="Sistemas completos de ERP, CRM, controle de estoque, relatórios financeiros e dashboards analíticos."
          icon="dashboard"
        />

        <!-- E-commerce -->
        <AppTypeCard
          title="E-commerce & Marketplace"
          description="Lojas virtuais completas, marketplaces, sistemas de pagamento e gestão de produtos."
          icon="shopping"
        />

        <!-- Saúde & Medicina -->
        <AppTypeCard
          title="Saúde & Medicina"
          description="Prontuários eletrônicos, agendamentos médicos, telemedicina e sistemas hospitalares."
          icon="health"
        />

        <!-- Redes Sociais -->
        <AppTypeCard
          title="Redes Sociais"
          description="Plataformas sociais, comunidades, chats em tempo real e sistemas de conteúdo."
          icon="social"
        />

        <!-- Delivery -->
        <AppTypeCard
          title="Delivery & Logística"
          description="Apps de entrega, rastreamento em tempo real, gestão de frota e otimização de rotas."
          icon="mobile"
        />

        <!-- Membros -->
        <AppTypeCard
          title="Área de Membros"
          description="Plataformas de cursos, assinaturas, comunidades exclusivas e conteúdo protegido."
          icon="users"
        />

        <!-- Landing Pages -->
        <AppTypeCard
          title="Landing Pages"
          description="Sites institucionais, portfólios, blogs e páginas de conversão otimizadas."
          icon="document"
        />

        <!-- Dashboards -->
        <AppTypeCard
          title="Dashboards & BI"
          description="Painéis analíticos, visualização de dados, relatórios interativos e business intelligence."
          icon="chart"
        />
      </div>
    </div>

    <!-- Bottom gradient fade -->
    <div class="absolute bottom-0 left-0 right-0 h-20 bg-gradient-fade"></div>
  </section>
</template>

<script setup>
import Badge from '~/components/ui/Badge.vue'
import AppTypeCard from '~/components/ui/AppTypeCard.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>