<script setup>
import { MessageCircle, Zap, ShieldCheck, Clock } from 'lucide-vue-next'

const perks = [
  { text: 'Konsul Gratis', icon: Zap },
  { text: 'Garansi 30 Hari', icon: ShieldCheck },
  { text: 'Fast Response', icon: Clock }
]
</script>

<template>
  <section id="kontak" class="py-16 px-5 bg-white">
    <div class="max-w-7xl mx-auto bg-slate-950 rounded-[3rem] p-8 md:p-20 relative overflow-hidden shadow-2xl shadow-blue-900/20">
      
      <div class="absolute -top-24 -right-24 w-96 h-96 bg-blue-600/20 blur-[100px] pointer-events-none"></div>
      <div class="absolute -bottom-24 -left-24 w-96 h-96 bg-indigo-600/10 blur-[100px] pointer-events-none"></div>

      <div class="max-w-7xl mx-auto grid lg:grid-cols-2 gap-12 items-center relative z-10 text-left">
        
        <div>
          <h2 class="text-3xl md:text-6xl font-black text-white tracking-tighter uppercase italic leading-none mb-6">
            Udah Siap <br/> <span class="text-blue-500">Nugas Lagi?</span>
          </h2>
          <p class="text-sm md:text-lg text-slate-400 mb-10 leading-relaxed font-medium">
            Jangan biarin laptop bermasalah ngehambat masa depanmu. Chat eduFix sekarang, kita diagnosis gratis sampe ketemu penyakitnya.
          </p>
          
          <div class="flex flex-wrap gap-4">
            <div v-for="p in perks" :key="p.text" class="flex items-center gap-2 bg-white/5 border border-white/10 px-4 py-2 rounded-full">
              <component :is="p.icon" class="text-blue-500" :size="14" />
              <span class="text-[10px] font-bold text-slate-300 uppercase tracking-widest">{{ p.text }}</span>
            </div>
          </div>
        </div>

        <div class="flex flex-col items-center lg:items-end justify-center">
          <div class="w-full lg:max-w-xs space-y-4">
            <a href="https://wa.me/..." 
               class="flex items-center justify-center gap-3 w-full py-5 bg-blue-600 text-white font-black rounded-2xl hover:bg-blue-700 hover:scale-[1.02] transition-all shadow-xl shadow-blue-600/30 text-lg uppercase italic tracking-tighter">
              <MessageCircle :size="24" />
              Tanya Teknisi
            </a>
            <p class="text-[10px] text-slate-500 text-center font-bold uppercase tracking-[0.2em]">
              Biasanya dibalas dalam <span class="text-slate-300">5 menit</span>
            </p>
          </div>
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