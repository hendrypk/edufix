<script setup>
import { ChevronRight, Coffee, Star } from 'lucide-vue-next'
</script>

<template>
  <section class="pt-28 pb-16 md:pt-48 md:pb-32 px-5 bg-slate-50 relative overflow-hidden">
    <div class="max-w-7xl mx-auto grid lg:grid-cols-2 gap-10 items-center relative z-10">
        <div class="text-left max-w-2xl">
            <div class="inline-flex items-center gap-2 bg-slate-100 px-3 py-1.5 rounded-full mb-6 border border-slate-200">
            <Sparkles class="text-blue-600" :size="12" />
            <span class="text-[10px] font-black uppercase tracking-[0.1em] text-slate-600">Solusi Deadline Mahasiswa</span>
            </div>
            
            <h1 class="text-4xl md:text-6xl font-extrabold text-slate-950 leading-[1.1] tracking-tight mb-6 uppercase">
            Laptop Nge-lag? <br />
            <span class="text-blue-600">Bikin Ngebut Lagi.</span>
            </h1>
            
            <p class="text-sm md:text-lg text-slate-500 mb-10 leading-relaxed font-medium">
            Nggak perlu emosi gara-gara laptop rewel pas bimbingan. Di eduFix, laptop kamu kita bikin sehat lagi dengan harga yang nggak bikin jatah makan sebulan ludes.
            </p>
            
            <div class="flex flex-wrap gap-4">
            <a href="#kontak" class="px-8 py-4 bg-blue-600 text-white font-bold rounded-2xl hover:bg-blue-700 transition shadow-xl shadow-blue-100 flex items-center gap-2 text-sm uppercase italic">
                Chat Teknisi Sekarang <MessageCircle :size="18" />
            </a>
            <a href="#layanan" class="px-8 py-4 bg-white text-slate-700 border border-slate-200 font-bold rounded-2xl hover:bg-slate-50 transition text-sm uppercase tracking-widest">
                Cek Layanan
            </a>
            </div>
        </div>
      <div class="hidden lg:block relative">
        <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?q=80&w=1000&auto=format&fit=crop" class="rounded-[2.5rem] shadow-2xl border-8 border-white" alt="Student Tech" />
      </div>
    </div>
  </section>
</template>