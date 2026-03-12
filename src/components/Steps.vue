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
  <section id="proses" class="py-16 md:py-24 px-5 bg-white overflow-hidden">
    <div class="max-w-7xl mx-auto">
      <div class="mb-16 text-left border-l-4 border-blue-600 pl-6">
        <h2 class="text-3xl md:text-5xl font-black tracking-tighter uppercase italic leading-none mb-4 text-slate-900">
          Alur <span class="text-blue-600">Simpel.</span>
        </h2>
        <p class="text-sm md:text-base text-slate-500 font-medium max-w-md uppercase tracking-wide">
          Gak pake ribet, laptop sembuh dalam 4 tahap.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-4 gap-4 md:gap-6 relative">
        <div class="hidden md:block absolute top-1/2 left-0 w-full h-px bg-slate-100 -z-10"></div>

        <div v-for="(step, i) in steps" :key="i" 
             class="group relative p-8 bg-slate-50 rounded-[2.5rem] border border-transparent hover:border-blue-200 hover:bg-white hover:shadow-2xl hover:shadow-blue-900/5 transition-all duration-500 flex flex-col items-start text-left">
          
          <div class="absolute top-6 right-8 text-4xl font-black text-slate-100 group-hover:text-blue-50 transition-colors italic">
            0{{ i + 1 }}
          </div>

          <div class="w-12 h-12 bg-white rounded-2xl flex items-center justify-center text-blue-600 shadow-sm border border-slate-100 group-hover:bg-blue-600 group-hover:text-white transition-all mb-8">
            <component :is="step.icon" :size="24" />
          </div>

          <h3 class="text-lg font-black uppercase italic tracking-tight text-slate-900 mb-3 leading-none">
            {{ step.title }}
          </h3>
          <p class="text-xs md:text-sm text-slate-500 font-medium leading-relaxed">
            {{ step.desc }}
          </p>

          <div class="mt-6 md:hidden">
            <ArrowRight v-if="i < 3" class="text-slate-300 rotate-90" :size="20" />
          </div>
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