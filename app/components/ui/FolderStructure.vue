<template>
  <div class="bg-gradient-to-br from-primary-950 to-primary-900 border border-neutral-600/50 rounded-2xl shadow-2xl w-full max-w-5xl h-[500px] flex overflow-hidden backdrop-blur-sm">
    <!-- Left Panel - File Explorer -->
    <div class="w-80 bg-gradient-to-b from-primary-950/90 to-primary-900/90 border-r border-neutral-600/30 flex flex-col backdrop-blur-sm">
      <!-- Explorer Header -->
      <div class="flex items-center justify-between p-4 border-b border-neutral-600/30 bg-primary-900/50">
        <div class="flex space-x-1.5">
          <div class="w-3.5 h-3.5 bg-gradient-to-br from-red-400 to-red-600 rounded-full shadow-sm border border-red-300/50"></div>
          <div class="w-3.5 h-3.5 bg-gradient-to-br from-yellow-400 to-yellow-600 rounded-full shadow-sm border border-yellow-300/50"></div>
          <div class="w-3.5 h-3.5 bg-gradient-to-br from-green-400 to-green-600 rounded-full shadow-sm border border-green-300/50"></div>
        </div>
        <div class="flex items-center space-x-2">
          <span class="text-neutral-300 text-sm font-medium tracking-wide">Explorer</span>
          <div class="w-2 h-2 bg-secondary/60 rounded-full animate-pulse"></div>
        </div>
      </div>

      <!-- File Tree -->
      <div class="flex-1 p-5 space-y-2 text-sm font-mono overflow-y-auto">
        <!-- components folder expanded -->
        <div class="flex items-center text-neutral-200 hover:text-white transition-colors group">
          <div class="flex items-center space-x-2">
            <svg class="w-4 h-4 text-secondary group-hover:text-secondary-400 transition-colors" fill="currentColor" viewBox="0 0 24 24">
              <path d="M10 4H4c-1.11 0-2 .89-2 2v12c0 1.11.89 2 2 2h16c1.11 0 2-.89 2-2V8c0-1.11-.89-2-2-2h-8l-2-2z"/>
            </svg>
            <span class="font-medium">components</span>
            <svg class="w-3 h-3 text-neutral-400 group-hover:text-neutral-300 transition-colors" fill="currentColor" viewBox="0 0 24 24">
              <path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z"/>
            </svg>
          </div>
        </div>

        <!-- BaseButton.vue -->
        <div class="flex items-center text-secondary ml-7 hover:bg-secondary/10 px-2 py-1.5 rounded-lg transition-all duration-200 group cursor-pointer">
          <div class="flex items-center space-x-2">
            <div class="w-3 h-3 bg-gradient-to-br from-secondary to-secondary-600 rounded-sm border border-secondary/50"></div>
            <span class="font-medium group-hover:text-secondary-400">BaseButton.vue</span>
          </div>
        </div>

        <!-- BaseInput.vue -->
        <div class="flex items-center text-secondary ml-7 hover:bg-secondary/10 px-2 py-1.5 rounded-lg transition-all duration-200 group cursor-pointer">
          <div class="flex items-center space-x-2">
            <div class="w-3 h-3 bg-gradient-to-br from-secondary to-secondary-600 rounded-sm border border-secondary/50"></div>
            <span class="font-medium group-hover:text-secondary-400">BaseInput.vue</span>
          </div>
        </div>

        <!-- composables folder expanded -->
        <div class="flex items-center text-neutral-200 hover:text-white transition-colors group mt-4">
          <div class="flex items-center space-x-2">
            <svg class="w-4 h-4 text-secondary group-hover:text-secondary-400 transition-colors" fill="currentColor" viewBox="0 0 24 24">
              <path d="M10 4H4c-1.11 0-2 .89-2 2v12c0 1.11.89 2 2 2h16c1.11 0 2-.89 2-2V8c0-1.11-.89-2-2-2h-8l-2-2z"/>
            </svg>
            <span class="font-medium">composables</span>
            <svg class="w-3 h-3 text-neutral-400 group-hover:text-neutral-300 transition-colors" fill="currentColor" viewBox="0 0 24 24">
              <path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z"/>
            </svg>
          </div>
        </div>

        <!-- userCustomer.ts -->
        <div class="flex items-center text-blue-400 ml-7 hover:bg-blue-500/10 px-2 py-1.5 rounded-lg transition-all duration-200 group cursor-pointer">
          <div class="flex items-center space-x-2">
            <div class="w-3 h-3 bg-gradient-to-br from-blue-400 to-blue-600 rounded-sm border border-blue-400/50"></div>
            <span class="font-medium group-hover:text-blue-300">userCustomer.ts</span>
          </div>
        </div>

        <!-- app.vue - Selected -->
        <div class="flex items-center text-secondary bg-gradient-to-r from-secondary/20 to-secondary/10 px-3 py-2 rounded-lg shadow-lg border border-secondary/30 mt-4 backdrop-blur-sm">
          <div class="flex items-center space-x-2">
            <div class="w-3 h-3 bg-gradient-to-br from-secondary to-secondary-600 rounded-sm border border-secondary/50 shadow-sm"></div>
            <span class="font-semibold text-secondary-300">app.vue</span>
            <div class="w-2 h-2 bg-secondary rounded-full animate-pulse ml-auto"></div>
          </div>
        </div>

        <!-- package.json -->
        <div class="flex items-center text-green-400 hover:bg-green-500/10 px-2 py-1.5 rounded-lg transition-all duration-200 group cursor-pointer mt-2">
          <div class="flex items-center space-x-2">
            <div class="w-3 h-3 bg-gradient-to-br from-green-400 to-green-600 rounded-sm border border-green-400/50"></div>
            <span class="font-medium group-hover:text-green-300">package.json</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Right Panel - Code Editor -->
    <div class="flex-1 flex flex-col bg-gradient-to-b from-primary-900/50 to-primary-950/50 backdrop-blur-sm">
      <!-- Simple Header -->
      <div class="flex items-center justify-between p-4 border-b border-neutral-600/30 bg-primary-900/30">
        <div class="text-neutral-300 text-sm font-medium">app.vue</div>
        <div class="flex items-center space-x-2">
          <div class="w-2 h-2 bg-secondary/60 rounded-full animate-pulse"></div>
          <span class="text-neutral-400 text-xs font-mono">modified</span>
        </div>
      </div>

      <!-- Code Content -->
      <div class="flex-1 p-6 font-mono text-sm overflow-auto">
        <div class="space-y-2">
          <div class="text-orange-400 font-medium">&lt;<span class="text-blue-400">script</span> <span class="text-green-400">setup</span>&gt;</div>
          <div class="ml-2 text-blue-400">const <span class="text-white font-medium">message</span> = <span class="text-green-300">ref</span>(<span class="text-red-300">''</span>)</div>
          <div class="ml-2 text-blue-400">const { <span class="text-white font-medium">handleClick</span> } = <span class="text-green-300">userCustomer</span>()</div>
          <div class="text-orange-400 font-medium">&lt;/<span class="text-blue-400">script</span>&gt;</div>
          <div class="mt-6"></div>
          <div class="text-orange-400 font-medium">&lt;<span class="text-blue-400">template</span>&gt;</div>
          <div class="ml-2 text-orange-400">&lt;<span class="text-blue-400">main</span> <span class="text-green-400">class</span>=<span class="text-red-300">"container"</span>&gt;</div>
          <div class="ml-4 text-orange-400">&lt;<span class="text-blue-400">h1</span> <span class="text-green-400">class</span>=<span class="text-red-300">"title"</span>&gt;</div>
          <div class="ml-6 text-white font-medium">App com Componentes Reutilizáveis</div>
          <div class="ml-4 text-orange-400">&lt;/<span class="text-blue-400">h1</span>&gt;</div>
          <div class="ml-4 text-orange-400">&lt;<span class="text-blue-400">form</span> <span class="text-green-400">class</span>=<span class="text-red-300">"form-container"</span>&gt;</div>
          <div class="ml-6 text-orange-400">&lt;<span class="text-blue-400 font-semibold">BaseInput</span> <span class="text-green-400">v-model</span>=<span class="text-red-300">"message"</span> /&gt;</div>
          <div class="ml-6 text-orange-400">&lt;<span class="text-blue-400 font-semibold">BaseButton</span> <span class="text-green-400">@click</span>=<span class="text-red-300">"handleClick"</span>&gt;</div>
          <div class="ml-8 text-white font-medium">Executar Ação Principal</div>
          <div class="ml-6 text-orange-400">&lt;/<span class="text-blue-400 font-semibold">BaseButton</span>&gt;</div>
          <div class="ml-4 text-orange-400">&lt;/<span class="text-blue-400">form</span>&gt;</div>
          <div class="ml-2 text-orange-400">&lt;/<span class="text-blue-400">main</span>&gt;</div>
          <div class="text-orange-400 font-medium">&lt;/<span class="text-blue-400">template</span>&gt;</div>
        </div>
      </div>
    </div>
  </div>
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