<script setup>
import { MessageCircle } from 'lucide-vue-next'

const phoneNumber = '6281234567890' // Ganti dengan nomor WA kamu
const message = 'Halo eduFix, mau tanya-tanya soal servis laptop dong...'
const waLink = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`
</script>

<template>
  <div class="fixed bottom-6 right-6 z-[999] flex flex-col items-end gap-3">
    
    <div class="bg-white px-4 py-2 rounded-2xl shadow-2xl border border-slate-100 flex items-center gap-2 animate-bounce-slow">
      <span class="relative flex h-2 w-2">
        <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-blue-400 opacity-75"></span>
        <span class="relative inline-flex rounded-full h-2 w-2 bg-blue-600"></span>
      </span>
      <span class="text-[10px] font-black uppercase tracking-widest text-slate-900 italic">
        Teknisi Online
      </span>
    </div>

    <a 
      :href="waLink"
      target="_blank"
      class="group flex items-center justify-center w-16 h-16 bg-blue-600 text-white rounded-2xl shadow-2xl shadow-blue-600/40 hover:bg-blue-700 hover:scale-110 active:scale-95 transition-all duration-300"
    >
      <MessageCircle :size="32" class="group-hover:rotate-12 transition-transform" />
      
      <span class="absolute right-20 bg-slate-900 text-white text-[10px] font-bold px-3 py-2 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none uppercase tracking-widest whitespace-nowrap">
        Chat Sekarang
      </span>
    </a>
  </div>
</template>

<style scoped>
@keyframes bounce-slow {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-5px); }
}
.animate-bounce-slow {
  animation: bounce-slow 3s ease-in-out infinite;
}
</style>