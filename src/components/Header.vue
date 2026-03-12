
<script setup>
import { ref, onMounted } from 'vue'
import { Laptop, Search, Menu } from 'lucide-vue-next'

const isScrolled = ref(false)

onMounted(() => {
  window.addEventListener('scroll', () => {
    isScrolled.value = window.scrollY > 20
  })
})
</script>

<template>
  <header 
    :class="[
      'fixed top-0 w-full z-[100] transition-all duration-500 border-b',
      isScrolled ? 'bg-slate-950/80 backdrop-blur-xl border-white/5 py-3' : 'bg-transparent border-transparent py-6'
    ]"
  >
    <div class="max-w-7xl mx-auto flex justify-between items-center px-6">
      
      <div class="flex items-center gap-3 group cursor-pointer">
        <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-indigo-600 rounded-xl flex items-center justify-center shadow-lg shadow-blue-500/20 group-hover:rotate-12 transition-transform">
          <Laptop class="text-white" :size="20" />
        </div>
        <div class="flex flex-col -space-y-1">
          <span class="text-2xl font-black tracking-tighter text-white leading-none">
            EDUFIX<span class="text-blue-500 italic">ID</span>
          </span>
          <span class="text-[8px] font-bold tracking-[0.3em] text-slate-500 uppercase">Tech Restoration</span>
        </div>
      </div>

      <nav class="hidden md:flex items-center gap-10">
        <a 
          v-for="item in ['Home', 'Services', 'Experience', 'Contact']" 
          :key="item"
          href="#" 
          class="text-[11px] font-black uppercase tracking-[0.2em] text-slate-400 hover:text-blue-500 transition-colors relative group"
        >
          {{ item }}
          <span class="absolute -bottom-1 left-0 w-0 h-0.5 bg-blue-600 transition-all group-hover:w-full"></span>
        </a>
      </nav>

      <div class="flex items-center gap-4">
        <button class="hidden sm:block text-slate-400 hover:text-white transition p-2">
          <Search :size="20" />
        </button>
        <button class="group relative px-6 py-2.5 bg-white text-black text-xs font-black uppercase tracking-widest rounded-full overflow-hidden hover:text-white transition-colors duration-300">
          <span class="relative z-10">Get Started</span>
          <div class="absolute inset-0 bg-blue-600 translate-y-full group-hover:translate-y-0 transition-transform duration-300"></div>
        </button>
        
        <button class="md:hidden text-white">
          <Menu :size="24" />
        </button>
      </div>

    </div>
  </header>
</template>


<style scoped>
/* Tambahkan font Inter atau Montserrat untuk hasil maksimal */
</style>