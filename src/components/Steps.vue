<script setup>
import { MessageCircle, Search, Wrench, Sparkles, ArrowRight } from 'lucide-vue-next'

const steps = [
  { 
    title: 'Konsul Dulu', 
    desc: 'Chat via WA, ceritain drama laptopmu. Fast response, gak pake bot kaku.',
    icon: MessageCircle 
  },
  { 
    title: 'Diagnosis', 
    desc: 'Bawa ke basecamp atau kita jemput. Kita cek total sampe ketemu penyakitnya.',
    icon: Search 
  },
  { 
    title: 'Eksekusi', 
    desc: 'Setelah deal harga, langsung kita sikat. Transparan, gak ada biaya siluman.',
    icon: Wrench 
  },
  { 
    title: 'Siap Nugas', 
    desc: 'Laptop balik ngebut + garansi aman. Kamu tinggal fokus ngejar deadline.',
    icon: Sparkles 
  }
]
</script>

<template>
  <section id="proses" class="py-16 md:py-24 px-6 bg-white overflow-hidden">
    <div class="max-w-7xl mx-auto">
      
      <div class="mb-16 md:mb-20 text-left border-l-4 border-blue-600 pl-6">
        <p class="text-[10px] font-black uppercase tracking-[0.4em] text-blue-600 mb-2">How We Work</p>
        <h2 class="text-3xl md:text-5xl font-black tracking-tighter uppercase italic leading-none text-slate-950">
          Alur Servis <br/> <span class="text-blue-600">Anti Ribet.</span>
        </h2>
        <p class="mt-4 text-sm md:text-base text-slate-500 font-medium max-w-md leading-relaxed">
          Gak perlu bingung prosedur. Laptop sembuh cuma lewat 4 tahap transparan ini.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4 md:gap-6 relative">
        
        <div class="hidden lg:block absolute top-1/2 left-0 w-full h-px bg-slate-100 -z-10"></div>

        <div v-for="(step, i) in steps" :key="i" 
             class="group relative p-8 md:p-10 bg-slate-50 rounded-[2.5rem] border border-transparent hover:border-blue-100 hover:bg-white hover:shadow-2xl hover:shadow-blue-900/5 transition-all duration-500 flex flex-col items-start">
          
          <div class="absolute top-8 right-10 text-5xl font-black text-slate-200/50 group-hover:text-blue-50 transition-colors italic tracking-tighter">
            0{{ i + 1 }}
          </div>

          <div class="w-14 h-14 bg-white rounded-2xl flex items-center justify-center text-blue-600 shadow-sm border border-slate-100 group-hover:bg-blue-600 group-hover:text-white transition-all duration-300 mb-10">
            <component :is="step.icon" :size="28" />
          </div>

          <div class="text-left relative z-10">
            <h3 class="text-xl font-black uppercase italic tracking-tight text-slate-900 mb-4 leading-none">
              {{ step.title }}
            </h3>
            <p class="text-xs md:text-sm text-slate-500 font-medium leading-relaxed">
              {{ step.desc }}
            </p>
          </div>

          <div class="mt-8 md:hidden">
            <div v-if="i < 3" class="flex flex-col items-center gap-1 opacity-20">
              <div class="w-1 h-1 bg-slate-400 rounded-full"></div>
              <div class="w-1 h-1 bg-slate-400 rounded-full"></div>
              <ArrowRight class="rotate-90 text-slate-400" :size="16" />
            </div>
          </div>
        </div>
      </div>

      <div class="mt-16 text-left md:text-center">
        <div class="inline-flex flex-col md:flex-row items-center gap-4 bg-slate-50 px-6 py-3 rounded-2xl border border-slate-100">
          <span class="text-[10px] font-black uppercase tracking-widest text-slate-400">Punya kendala mendesak?</span>
          <a href="https://wa.me/6287736763720" class="text-[10px] font-black uppercase tracking-widest text-blue-600 hover:underline">
            Gunakan Layanan Prioritas →
          </a>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
h2, h3 {
  font-feature-settings: "salt" on, "ss01" on;
}
</style>