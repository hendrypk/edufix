<script setup>
import { MessageCircle } from 'lucide-vue-next'
</script>

<template>
  <section id="kontak" class="py-20 px-5">
    <div class="max-w-5xl mx-auto bg-slate-950 rounded-[2.5rem] p-10 md:p-20 text-center relative overflow-hidden">
      <div class="absolute top-0 right-0 w-64 h-64 bg-blue-600/20 blur-[100px]"></div>
      <div class="relative z-10">
        <h2 class="text-3xl md:text-6xl font-black text-white mb-6 uppercase italic tracking-tighter">Benerin Sekarang Yuk!</h2>
        <p class="text-slate-400 mb-10 text-sm md:text-lg font-medium">Jangan ditunda, ntar makin parah. Konsultasi aja dulu, GRATIS!</p>
        <a href="https://wa.me/..." class="inline-flex items-center gap-3 px-8 py-4 bg-blue-600 text-white font-bold rounded-2xl hover:bg-blue-700 transition shadow-2xl shadow-blue-900/40 text-sm md:text-lg uppercase italic">
          <MessageCircle :size="24" /> Chat WhatsApp
        </a>
      </div>
    </div>
  </section>
</template>