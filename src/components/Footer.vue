<script setup>
import { Laptop } from 'lucide-vue-next'
</script>

<template>
  <footer class="py-12 border-t border-slate-100 bg-slate-50 text-left">
    <div class="max-w-7xl mx-auto px-5 flex flex-col md:flex-row justify-between items-center gap-6">
      <div class="flex items-center gap-2">
        <div class="w-7 h-7 bg-blue-600 rounded flex items-center justify-center">
          <Laptop class="text-white" :size="14" />
        </div>
        <span class="text-lg font-black italic tracking-tighter uppercase">EDUFIXID.</span>
      </div>
      <p class="text-[10px] font-bold text-slate-400 uppercase tracking-[0.3em]">© 2026 Solusi Cerdas Mahasiswa</p>
    </div>
  </footer>
</template>