<script setup>
import { X, Check, AlertCircle, Sparkles } from 'lucide-vue-next'

const comparisons = [
  { 
    problem: 'Laptop lemot, buka Word aja nunggunya lama.', 
    solution: 'Laptop sat-set, multitasking tugas nggak pake drama.' 
  },
  { 
    problem: 'Lagi asik ngetik tiba-tiba Blue Screen.', 
    solution: 'Sistem stabil, ngerjain skripsi jadi tenang.' 
  },
  { 
    problem: 'Baterai drop, harus nempel colokan terus.', 
    solution: 'Baterai awet, nugas di kafe makin produktif.' 
  },
  { 
    problem: 'WiFi hilang pas mau submit tugas.', 
    solution: 'Koneksi gacor, submit tugas selalu on-time.' 
  }
]
</script>

<template>
  <section class="py-16 md:py-24 px-5 bg-white">
    <div class="max-w-7xl mx-auto">
      
      <div class="mb-16 text-left border-l-4 border-blue-600 pl-6">
        <h2 class="text-3xl md:text-5xl font-black tracking-tighter uppercase italic leading-none text-slate-950">
          Udah Capek <br/> <span class="text-blue-600">Sama Masalah IT?</span>
        </h2>
        <p class="mt-4 text-sm md:text-base text-slate-500 font-medium max-w-md">
          Bedanya jauh banget antara laptop yang "sakit" sama yang udah di-tuning eduFix. Cek sendiri:
        </p>
      </div>

      <div class="grid lg:grid-cols-2 gap-4 md:gap-8 items-stretch">
        
        <div class="p-8 md:p-12 bg-slate-50 rounded-[2.5rem] border border-slate-100 flex flex-col">
          <div class="flex items-center gap-3 mb-10">
            <div class="w-10 h-10 bg-slate-200 text-slate-500 rounded-xl flex items-center justify-center">
              <AlertCircle :size="20" />
            </div>
            <div>
              <p class="text-[10px] font-black uppercase tracking-widest text-slate-400 leading-none mb-1">Status</p>
              <h3 class="text-lg font-black uppercase italic text-slate-900 tracking-tight">Kondisi Sekarang</h3>
            </div>
          </div>

          <div class="space-y-8">
            <div v-for="item in comparisons" :key="item.problem" class="flex items-start gap-4 group">
              <div class="w-6 h-6 rounded-full bg-slate-200 flex items-center justify-center shrink-0 mt-0.5">
                <X class="text-slate-500" :size="12" stroke-width="4" />
              </div>
              <p class="text-sm text-slate-500 font-medium leading-relaxed italic">{{ item.problem }}</p>
            </div>
          </div>
        </div>

        <div class="p-8 md:p-12 bg-white rounded-[2.5rem] border-2 border-blue-600 shadow-2xl shadow-blue-900/10 flex flex-col relative overflow-hidden group">
          <div class="absolute -top-12 -right-12 w-40 h-40 bg-blue-600/5 rounded-full blur-3xl"></div>
          
          <div class="flex items-center gap-3 mb-10 relative z-10">
            <div class="w-10 h-10 bg-blue-600 text-white rounded-xl flex items-center justify-center shadow-lg shadow-blue-200">
              <Sparkles :size="20" />
            </div>
            <div>
              <p class="text-[10px] font-black uppercase tracking-widest text-blue-600 leading-none mb-1">Upgrade</p>
              <h3 class="text-lg font-black uppercase italic text-slate-900 tracking-tight">Setelah eduFix</h3>
            </div>
          </div>

          <div class="space-y-8 relative z-10">
            <div v-for="item in comparisons" :key="item.solution" class="flex items-start gap-4">
              <div class="w-6 h-6 rounded-full bg-blue-600 flex items-center justify-center shrink-0 mt-0.5 shadow-md shadow-blue-200">
                <Check class="text-white" :size="12" stroke-width="4" />
              </div>
              <p class="text-sm text-slate-900 font-bold leading-relaxed">{{ item.solution }}</p>
            </div>
          </div>

          <div class="mt-auto pt-10">
            <div class="inline-flex items-center gap-2 bg-blue-50 px-4 py-2 rounded-xl">
              <span class="text-[10px] font-black uppercase tracking-widest text-blue-600 italic">Tugas Lancar, Hati Tenang.</span>
            </div>
          </div>
        </div>

      </div>

      <div class="mt-12 text-left md:text-center">
        <p class="text-[10px] font-bold text-slate-400 uppercase tracking-[0.4em]">
          Udah <span class="text-slate-900">2.000+ Mahasiswa</span> Pindah Ke Sisi Nyaman.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
h2, h3 {
  font-feature-settings: "salt" on, "ss01" on;
}
</style>