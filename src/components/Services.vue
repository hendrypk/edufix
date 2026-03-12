<script setup>
import { 
  Monitor, Laptop, AppWindow, MousePointer2, 
  Check, ArrowUpRight 
} from 'lucide-vue-next'

const services = [
  { 
    id: '01',
    title: 'Instal Ulang Windows', 
    icon: Monitor, 
    desc: 'Laptop lemot bikin emosi? Kita instal ulang pake OS terbaru biar sat-set lagi nugas.',
    price: 'Mulai 50rb',
    tags: ['Windows 10/11', 'Drivers', 'Optimasi']
  },
  { 
    id: '02',
    title: 'Reparasi Laptop', 
    icon: Laptop, 
    desc: 'Layar pecah atau mati total? Tenang, teknisi kita jagonya bedah hardware sampe sembuh.',
    price: 'Cek Dulu Gratis',
    tags: ['LCD', 'Engsel', 'Motherboard']
  },
  { 
    id: '03',
    title: 'Install Aplikasi', 
    icon: AppWindow, 
    desc: 'Butuh Adobe atau Office buat praktikum? Kita bantu instalin tanpa drama & anti-virus.',
    price: 'Hemat & Cepat',
    tags: ['Office', 'Adobe', 'Design']
  },
  { 
    id: '04',
    title: 'Reparasi Aksesoris', 
    icon: MousePointer2, 
    desc: 'Keyboard macet atau mouse error? Jangan dibuang, sini kita reparasi biar hemat jajan.',
    price: 'Bisa Ditunggu',
    tags: ['Keyboard', 'Mouse', 'Charger']
  }
]
</script>

<template>
  <section id="layanan" class="py-16 md:py-24 px-6 bg-white">
    <div class="max-w-7xl mx-auto">
      
      <div class="mb-16 md:mb-20 text-left border-l-4 border-blue-600 pl-6">
        <p class="text-[10px] font-black uppercase tracking-[0.4em] text-blue-600 mb-2">Our Expertise</p>
        <h2 class="text-3xl md:text-5xl font-black tracking-tighter uppercase italic leading-none text-slate-950">
          Solusi IT <br/> <span class="text-blue-600">No Tipu-Tipu.</span>
        </h2>
        <p class="mt-4 text-sm md:text-base text-slate-500 font-medium max-w-md leading-relaxed">
          Pilih layanan yang kamu butuhin. Semua pengerjaan transparan, harga jujur, dan bergaransi.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4 md:gap-6">
        <div v-for="s in services" :key="s.title" 
             class="group p-8 md:p-10 bg-slate-50 rounded-[2.5rem] border border-transparent hover:border-blue-100 hover:bg-white hover:shadow-2xl hover:shadow-blue-900/5 transition-all duration-500 flex flex-col h-full relative overflow-hidden">
          
          <span class="absolute top-8 right-10 text-5xl font-black text-slate-200/50 group-hover:text-blue-50 transition-colors italic tracking-tighter">
            {{ s.id }}
          </span>

          <div class="flex flex-col items-start mb-10 relative z-10">
            <div class="w-14 h-14 bg-white rounded-2xl flex items-center justify-center text-blue-600 shadow-sm border border-slate-100 group-hover:bg-blue-600 group-hover:text-white transition-all duration-300 mb-6">
              <component :is="s.icon" :size="28" />
            </div>
            <span class="text-[9px] font-black uppercase tracking-widest text-blue-600 bg-blue-50 px-3 py-1 rounded-full border border-blue-100">
              {{ s.price }}
            </span>
          </div>

          <div class="text-left flex-grow relative z-10">
            <h3 class="text-xl font-black mb-4 tracking-tight uppercase italic text-slate-900 leading-tight">
              {{ s.title }}
            </h3>
            <p class="text-xs md:text-sm text-slate-500 mb-10 font-medium leading-relaxed">
              {{ s.desc }}
            </p>
          </div>

          <div class="flex flex-wrap gap-2 pt-8 border-t border-slate-200/50 relative z-10">
            <div v-for="tag in s.tags" :key="tag" class="flex items-center gap-1.5 px-3 py-1 bg-white border border-slate-100 rounded-lg">
              <Check class="text-blue-600" :size="10" stroke-width="4" />
              <span class="text-[9px] font-bold text-slate-700 uppercase tracking-tight">{{ tag }}</span>
            </div>
          </div>

          <div class="mt-8 flex items-center gap-2 text-blue-600 opacity-0 group-hover:opacity-100 transition-opacity">
            <span class="text-[10px] font-black uppercase tracking-widest">Detail</span>
            <ArrowUpRight :size="14" />
          </div>
        </div>
      </div>

      <div class="mt-16 py-8 border-t border-slate-100 flex flex-col md:flex-row justify-between items-center gap-4">
        <p class="text-[10px] font-bold text-slate-400 uppercase tracking-[0.4em]">
          Semua servis sudah termasuk <span class="text-slate-900 italic underline decoration-blue-600">Garansi 30 Hari.</span>
        </p>
        <a href="https://wa.me/6287736763720" class="text-blue-600 font-black text-[10px] uppercase tracking-widest hover:underline">
          Butuh Layanan Lain? Tanya Sini →
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
h2, h3 {
  font-feature-settings: "salt" on, "ss01" on;
}
</style>