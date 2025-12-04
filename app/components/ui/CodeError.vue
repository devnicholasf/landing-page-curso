<template>
  <div class="relative w-full max-w-3xl mx-auto">
    <!-- Code Editor Container -->
    <div class="bg-gradient-to-br from-primary-900 via-primary-800 to-primary-700 rounded-lg shadow-2xl border border-red-500/20 overflow-hidden">
      <!-- Editor Header -->
      <div class="bg-primary-950/80 px-4 py-3 border-b border-red-500/30 flex items-center justify-between">
        <div class="flex items-center space-x-3">
          <div class="w-3 h-3 bg-red-500 rounded-full"></div>
          <div class="w-3 h-3 bg-yellow-500 rounded-full"></div>
          <div class="w-3 h-3 bg-green-500 rounded-full"></div>
        </div>
        <div class="flex items-center space-x-2">
          <span class="font-mono text-white/70 text-sm">{{ fileName }}</span>
          <div class="bg-red-500 text-white text-xs px-2 py-1 rounded">{{ errorCount }} errors</div>
        </div>
      </div>

      <!-- Line Numbers & Code Content -->
        <div class="flex bg-primary-900/60 min-h-[320px]">
        <!-- Line Numbers -->
        <div class="bg-primary-950/40 px-3 py-4 border-r border-white/10 select-none">
          <div class="font-mono text-xs text-white/40 space-y-1">
            <div v-for="line in 22" :key="line" class="leading-5">{{ line.toString().padStart(2, ' ') }}</div>
          </div>
        </div>

        <!-- Code Content -->
        <div class="flex-1 p-4 font-mono text-sm overflow-hidden">
          <!-- Template Section -->
          <div class="space-y-1">
            <div class="text-blue-300">&lt;<span class="text-red-400">template</span>&gt;</div>
            <div class="pl-4 text-white">  &lt;<span class="text-red-400 underline decoration-red-500 decoration-wavy">div class="container"</span>&gt;</div>
            <div class="pl-8 text-white">    &lt;<span class="text-red-400">h1</span>&gt;&#123;&#123; title &#125;&#125;&lt;/<span class="text-red-400">h1</span>&gt;</div>
            <div class="pl-8 text-white">    &lt;<span class="text-red-400 underline decoration-red-500 decoration-wavy">button @click="handleClick()"</span>&gt;Click&lt;/<span class="text-red-400">button</span>&gt;</div>
            <div class="pl-8 text-white">    &lt;<span class="text-red-400">div v-for="item in items"</span>&gt;</div>
            <div class="pl-12 text-white">      &lt;<span class="text-red-400">span</span>&gt;&#123;&#123; item.name &#125;&#125;&lt;/<span class="text-red-400">span</span>&gt;</div>
            <div class="pl-8 text-white">    &lt;/<span class="text-red-400">div</span>&gt;</div>
            <div class="pl-4 text-white">  &lt;/<span class="text-red-400">div</span>&gt;</div>
            <div class="text-blue-300">&lt;/<span class="text-red-400">template</span>&gt;</div>
            <div class="h-4"></div>

            <!-- Script Section with Errors -->
            <div class="text-blue-300">&lt;<span class="text-red-400">script</span>&gt;</div>
            <div class="pl-4 text-purple-300">import { <span class="text-red-400 underline decoration-red-500 decoration-wavy">ref, computed</span> } from 'vue'</div>
            <div class="pl-4 text-purple-300">import <span class="text-red-400 underline decoration-red-500 decoration-wavy">SomeComponent</span> from './Component'</div>
            <div class="h-2"></div>
            <div class="pl-4 text-purple-300">export default {</div>
            <div class="pl-8 text-white">name: '<span class="text-green-400">MyComponent</span>',</div>
            <div class="pl-8 text-white">data() {</div>
            <div class="pl-12 text-white">return {</div>
            <div class="pl-16 text-white">title: '<span class="text-green-400">Hello World</span>',</div>
            <div class="pl-16 text-white">items: <span class="text-red-400 underline decoration-red-500 decoration-wavy">undefined</span>,</div>
            <div class="pl-16 text-white"><span class="text-red-400 underline decoration-red-500 decoration-wavy">loading: true</span></div>
            <div class="pl-12 text-white">}</div>
            <div class="pl-8 text-white">},</div>
            <div class="pl-8 text-white">methods: {</div>
            <div class="pl-12 text-white"><span class="text-red-400 underline decoration-red-500 decoration-wavy">handleClick()</span> {</div>
            <div class="pl-16 text-white">console.<span class="text-yellow-300">log</span>(<span class="text-red-400 underline decoration-red-500 decoration-wavy">this.title</span>)</div>
            <div class="pl-16 text-white"><span class="text-red-400 underline decoration-red-500 decoration-wavy">this.fetchData()</span></div>
            <div class="pl-12 text-white">}</div>
            <div class="pl-8 text-white">}</div>
            <div class="pl-4 text-white">}</div>
            <div class="text-blue-300">&lt;/<span class="text-red-400">script</span>&gt;</div>
          </div>

          <!-- Error Indicators -->
          <div class="absolute right-4 top-20">
            <div class="space-y-2">
              <div class="w-2 h-1 bg-red-500 rounded animate-pulse"></div>
              <div class="w-2 h-1 bg-red-500 rounded animate-pulse delay-100"></div>
              <div class="w-2 h-1 bg-red-500 rounded animate-pulse delay-200"></div>
              <div class="w-2 h-1 bg-red-500 rounded animate-pulse delay-300"></div>
              <div class="w-2 h-1 bg-red-500 rounded animate-pulse delay-500"></div>
            </div>
          </div>
        </div>
      </div>

      <!-- Error Panel -->
      <div class="bg-red-500/10 border-t border-red-500/30 p-4">
        <div class="flex items-center space-x-2 text-red-400 text-sm">
          <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
          </svg>
          <span class="font-mono">{{ errorCount }} problems ({{ errorCount }} errors, 3 warnings)</span>
        </div>
      </div>
    </div>

    <!-- Glow effect -->
    <div class="absolute inset-0 bg-gradient-to-br from-red-500/10 via-transparent to-red-500/5 rounded-lg blur-xl -z-10 opacity-60"></div>
  </div>
</template>

<script setup>
const props = defineProps({
  fileName: {
    type: String,
    default: 'AppComponent.vue'
  },
  errorCount: {
    type: Number,
    default: 12
  }
})
</script>