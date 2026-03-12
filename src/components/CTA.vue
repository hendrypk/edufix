<script setup>
import { MessageCircle, ArrowRight, Sparkles } from 'lucide-vue-next'
</script>

<template>
  <section id="kontak" class="py-16 md:py-24 px-6 bg-white overflow-hidden">
    <div class="max-w-7xl mx-auto">
      <div class="flex flex-col md:flex-row items-center md:items-end justify-between gap-10">
        
        <div class="text-left border-l-4 border-blue-600 pl-6 md:pl-8">
          <div class="flex items-center gap-2 mb-4 text-blue-600">
            <Sparkles :size="16" />
            <span class="text-[10px] font-black uppercase tracking-[0.3em]">Solusi Terakhir</span>
          </div>
          
          <h2 class="text-4xl md:text-6xl font-black text-slate-950 tracking-tighter uppercase italic leading-[0.9] mb-6">
            Laptop Beres, <br />
            <span class="text-blue-600">Tugas Sukses.</span>
          </h2>
          
          <p class="text-sm md:text-base text-slate-500 font-medium max-w-sm leading-relaxed">
            Nggak perlu nunggu besok. Chat kita sekarang, konsul gratis, dan laptopmu siap tempur lagi buat ngerjain deadline.
          </p>
        </div>

        <div class="w-full md:w-auto shrink-0">
          <a href="https://wa.me/6287736763720" 
             class="group flex items-center justify-center gap-4 px-10 py-5 bg-blue-600 text-white font-black rounded-2xl hover:bg-blue-700 transition-all shadow-xl shadow-blue-200 uppercase italic tracking-tighter text-lg">
            <MessageCircle :size="24" />
            <span>Chat WhatsApp</span>
            <ArrowRight :size="18" class="group-hover:translate-x-1 transition-transform" />
          </a>
          
          <p class="mt-4 text-[10px] text-slate-400 font-bold uppercase tracking-widest text-center md:text-right">
            Nggak pake antre, <span class="text-blue-600">respon kilat!</span>
          </p>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
h2 {
  font-feature-settings: "salt" on, "ss01" on;
}
</style>