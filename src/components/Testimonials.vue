<script setup>
import { Star, Quote } from 'lucide-vue-next'

const reviews = [
  {
    name: 'Dika Ardiansyah',
    major: 'Teknik Informatika',
    text: 'Gila sih, instal ulang di sini cuma sejam. Langsung bisa lanjut ngerjain tugas praktikum yang numpuk. Harganya beneran ramah kantong!',
    stars: 5
  },
  {
    name: 'Sarah Amalia',
    major: 'Kedokteran',
    text: 'Layar laptop pecah pas mau bimbingan skripsi itu horor banget. Untung eduFix bisa gercep ganti LCD-nya. Teknisi jujur, part-nya original.',
    stars: 5
  },
  {
    name: 'Kevin Pratama',
    major: 'Manajemen',
    text: 'Awalnya cuma iseng nanya lewat WA, eh responnya cepet banget. Penjelasannya gak pake bahasa teknik yang pusing. Recommended!',
    stars: 5
  }
]
</script>

<template>
  <section class="py-16 md:py-24 px-6 bg-slate-50/50">
    <div class="max-w-7xl mx-auto">
      
      <div class="mb-16 text-left border-l-4 border-blue-600 pl-6">
        <p class="text-[10px] font-black uppercase tracking-[0.4em] text-blue-600 mb-2">Vibe Check</p>
        <h2 class="text-3xl md:text-5xl font-black tracking-tighter uppercase italic leading-none text-slate-950">
          Kata Mereka <br/> <span class="text-blue-600">Tentang eduFix.</span>
        </h2>
        <p class="mt-4 text-sm md:text-base text-slate-500 font-medium max-w-sm">
          Bukan testimoni settingan, beneran pengalaman nyata dari temen-temen mahasiswa.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div v-for="r in reviews" :key="r.name" 
             class="p-8 bg-white border border-slate-100 rounded-[2.5rem] hover:shadow-2xl hover:shadow-blue-900/5 transition-all duration-500 flex flex-col items-start relative overflow-hidden group">
          
          <Quote class="absolute -right-4 -top-4 text-slate-50 opacity-0 group-hover:opacity-100 transition-opacity" :size="120" />

          <div class="flex gap-1 mb-6 relative z-10">
            <Star v-for="i in r.stars" :key="i" class="text-blue-600 fill-blue-600" :size="14" />
          </div>

          <p class="text-sm md:text-base text-slate-700 font-medium leading-relaxed italic mb-8 relative z-10">
            "{{ r.text }}"
          </p>

          <div class="mt-auto flex items-center gap-4 relative z-10">
            <div class="w-10 h-10 bg-blue-50 rounded-full border border-blue-100 flex items-center justify-center font-black text-blue-600 text-xs uppercase italic">
              {{ r.name.charAt(0) }}
            </div>
            <div class="text-left">
              <h4 class="text-sm font-black uppercase italic tracking-tight text-slate-950">{{ r.name }}</h4>
              <p class="text-[10px] font-bold uppercase tracking-widest text-slate-400">{{ r.major }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
h2, h4, p {
  font-feature-settings: "salt" on, "ss01" on;
}
</style>