<script setup>
import { XCircle, CheckCircle2, AlertCircle, Sparkles } from 'lucide-vue-next'

const problems = [
  'Laptop lemot, buka Word aja ditinggal mandi dulu.',
  'Lagi asik nugas tiba-tiba Blue Screen.',
  'Baterai drop, kudu nempel colokan terus.',
  'WiFi sering hilang pas mau submit tugas.'
]

const solutions = [
  'Laptop sat-set, nugas jadi makin semangat.',
  'Sistem stabil, bebas drama crash pas deadline.',
  'Baterai sehat, nugas di kafe nggak perlu ribet.',
  'Koneksi gacor, submit tugas nggak pake delay.'
]
</script>

<template>
  <section class="py-16 px-5 bg-white overflow-hidden">
    <div class="max-w-7xl mx-auto">
      <div class="mb-12 text-left md:text-center max-w-2xl mx-auto">
        <h2 class="text-3xl md:text-5xl font-black tracking-tighter uppercase italic mb-5 leading-tight">
          Capek Sama <br class="md:hidden" /> <span class="text-red-500">Drama Laptop?</span>
        </h2>
        <p class="text-sm md:text-base text-slate-500 font-medium">
          Bedanya jauh banget antara nugas pake laptop "sakit" sama laptop yang udah di-tuning eduFix. Cek perbandingannya:
        </p>
      </div>

      <div class="grid md:grid-cols-2 gap-4 lg:gap-8 relative">
        <div class="hidden md:block absolute left-1/2 top-0 bottom-0 w-px bg-slate-100 -translate-x-1/2"></div>

        <div class="p-8 rounded-[2.5rem] bg-red-50/30 border border-red-100/50">
          <div class="flex items-center gap-3 mb-8">
            <div class="w-10 h-10 bg-red-100 text-red-600 rounded-xl flex items-center justify-center">
              <AlertCircle :size="20" />
            </div>
            <h3 class="text-lg font-black uppercase italic text-red-950 tracking-tight">Kondisi Sekarang</h3>
          </div>
          
          <ul class="space-y-6">
            <li v-for="p in problems" :key="p" class="flex items-start gap-4">
              <XCircle class="text-red-400 shrink-0 mt-1" :size="18" />
              <p class="text-xs md:text-sm text-red-900 font-medium leading-relaxed">{{ p }}</p>
            </li>
          </ul>
        </div>

        <div class="p-8 rounded-[2.5rem] bg-blue-50/50 border border-blue-100/50 relative overflow-hidden group">
          <Sparkles class="absolute -top-4 -right-4 text-blue-200 opacity-50 group-hover:rotate-12 transition-transform" :size="100" />
          
          <div class="flex items-center gap-3 mb-8 relative z-10">
            <div class="w-10 h-10 bg-blue-600 text-white rounded-xl flex items-center justify-center shadow-lg shadow-blue-200">
              <Sparkles :size="20" />
            </div>
            <h3 class="text-lg font-black uppercase italic text-blue-950 tracking-tight">Setelah EduFix</h3>
          </div>

          <ul class="space-y-6 relative z-10">
            <li v-for="s in solutions" :key="s" class="flex items-start gap-4">
              <CheckCircle2 class="text-blue-600 shrink-0 mt-1" :size="18" />
              <p class="text-xs md:text-sm text-blue-900 font-bold leading-relaxed">{{ s }}</p>
            </li>
          </ul>
        </div>
      </div>

      <div class="mt-12 text-center">
        <p class="text-[10px] font-black uppercase tracking-[0.3em] text-slate-400">
          Udah 2.000+ Mahasiswa Pindah Ke Sisi <span class="text-blue-600">Nyaman.</span>
        </p>
      </div>
    </div>
  </section>
</template>