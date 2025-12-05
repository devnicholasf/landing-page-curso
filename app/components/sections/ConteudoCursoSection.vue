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
          <Badge text="Conteúdo do Curso" />
        </div>

        <!-- Title -->
        <h2 class="font-primary text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-black mb-6 leading-tight">
          <span class="text-white">Domine a </span>
          <span class="bg-gradient-to-r from-secondary via-secondary-400 to-secondary-600 bg-clip-text text-transparent">
            Componentização Extrema
          </span>
        </h2>

        <!-- Description -->
        <p class="font-body text-lg sm:text-xl text-neutral-300 max-w-3xl mx-auto leading-relaxed">
          Um curso completo e prático que vai do zero ao deploy. 
          <span class="text-white">Aprenda a criar aplicações robustas</span> 
          com metodologia estruturada e code clean garantido.
        </p>
      </div>

      <!-- Course Sections -->
      <div class="max-w-4xl mx-auto space-y-6">
        <!-- Section 1: Fundamentos Teóricos -->
        <CourseSection
          section-number="1"
          title="Fundamentos Teóricos"
          description="Base empresarial e conceitos essenciais antes de codar"
          :initial-expanded="true"
          :modules="[
            {
              title: 'Comece Por aqui',
              description: 'Apresentação e informações importantes',
              status: 'LIBERADO'
            },
            {
              title: 'Anatomia de Software',
              description: 'Como funcionam os sistemas modernos',
              status: 'LIBERADO'
            }
          ]"
        />

        <!-- Section 2: Componentização Extrema -->
        <CourseSection
          section-number="2"
          title="Componentização Extrema"
          description="O coração do método: criando apps estruturados e escaláveis"
          :modules="[
            {
              title: 'Setup Inicial',
              description: 'Instalando as ferramentas necessárias',
              status: 'LIBERADO'
            },
            {
              title: 'Componentização com Nuxt',
              description: 'Entenda como funciona o método',
              status: 'LIBERADO'
            },
            {
              title: 'O Cofre do seu projeto',
              description: 'Git e Github para manter seu código protegido',
              status: 'LIBERADO'
            },
            {
              title: 'Caixa Rápido com IA',
              description: 'Landing pages para venda imediata',
              status: 'LIBERADO'
            }
          ]"
        />

        <!-- Section 3: Projetos Práticos -->
        <CourseSection
          section-number="3"
          title="Projetos Práticos"
          description="Projetos reais para fixar o conhecimento"
          :modules="[
            {
              title: 'Sistema Cadastro com Auth',
              description: 'Sistema básico de cadastro',
              status: 'LIBERADO'
            },
            {
              title: 'Aplicativo de Agendamento',
              description: 'Crie um sistema de Agendamentos do zero',
              status: 'LIBERADO'
            }
          ]"
        />

        <!-- Section 4: Backend e Assinaturas -->
        <CourseSection
          section-number="4"
          title="Backend e Assinaturas"
          description="Integração com banco de dados e pagamentos"
          :modules="[
            {
              title: 'Supabase Auth',
              description: 'Tudo sobre Autenticação com Supabase',
              status: 'LIBERADO'
            },
            {
              title: 'Supabase - Modelagem e Segurança',
              description: 'Tudo sobre Modelagem de dados e Segurança',
              status: 'LIBERADO'
            },
            {
              title: 'Stripe',
              description: 'O gateway de pagamento mais famoso do mundo',
              status: 'LIBERADO'
            }
          ]"
        />

        <!-- Section 5: Publicação e Manutenção -->
        <CourseSection
          section-number="5"
          title="Publicação e Manutenção"
          description="Publique seu app de forma profissional e segura"
          :modules="[
            {
              title: 'Publicação do Software',
              description: 'Aprenda a publicar na Vercel e VPS com domínio próprio',
              status: 'EM BREVE'
            }
          ]"
        />
      </div>

      <!-- Call to Action -->
      <div class="text-center mt-16">
        <ActionButton texto="Acessar Curso Completo" />
      </div>
    </div>

    <!-- Bottom gradient fade -->
    <div class="absolute bottom-0 left-0 right-0 h-20 bg-gradient-fade"></div>
  </section>
</template>

<script setup>
import Badge from '~/components/ui/Badge.vue'
import CourseSection from '~/components/ui/CourseSection.vue'
import ActionButton from '~/components/ui/ActionButton.vue'

// Component props
const props = defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>