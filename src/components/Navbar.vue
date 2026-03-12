<script setup>
import { ref, onMounted } from 'vue'
import { Laptop, Menu, X } from 'lucide-vue-next'

const isScrolled = ref(false)
const navOpen = ref(false)

onMounted(() => {
  window.addEventListener('scroll', () => {
    isScrolled.value = window.scrollY > 20
  })
})
</script>

<template>
  <nav :class="['fixed top-0 w-full z-[100] transition-all duration-300 border-b', isScrolled ? 'bg-white/90 backdrop-blur-md border-slate-200 py-3 shadow-sm' : 'bg-white border-transparent py-4']">
    <div class="max-w-7xl mx-auto px-5 flex justify-between items-center">
      <div class="flex items-center gap-2 cursor-pointer">
        <div class="w-8 h-8 bg-blue-600 rounded-lg flex items-center justify-center">
          <Laptop class="text-white" :size="18" />
        </div>
        <span class="text-lg font-black italic tracking-tighter">eduFix<span class="text-blue-600 not-italic">.</span></span>
      </div>

      <div class="hidden md:flex items-center gap-8 text-xs font-bold uppercase tracking-widest text-slate-500">
        <a href="#layanan" class="hover:text-blue-600 transition">Layanan</a>
        <a href="#proses" class="hover:text-blue-600 transition">Alur</a>
        <a href="https://wa.me/..." class="bg-blue-600 text-white px-5 py-2 rounded-full hover:bg-blue-700 transition">Tanya Dulu</a>
      </div>

      <button @click="navOpen = !navOpen" class="md:hidden text-slate-900">
        <component :is="navOpen ? X : Menu" :size="24" />
      </button>
    </div>

    <transition enter-active-class="duration-200 ease-out" enter-from-class="opacity-0 -translate-y-4" enter-to-class="opacity-100 translate-y-0">
      <div v-if="navOpen" class="md:hidden bg-white border-b border-slate-200 p-6 flex flex-col gap-4 text-center">
        <a href="#layanan" @click="navOpen = false" class="font-bold">Layanan</a>
        <a href="#proses" @click="navOpen = false" class="font-bold">Cara Kerja</a>
        <a href="https://wa.me/..." class="bg-blue-600 text-white py-3 rounded-xl font-bold">Chat WhatsApp</a>
      </div>
    </transition>
  </nav>
</template>