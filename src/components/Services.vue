<script setup>
import { 
  Monitor, Laptop, AppWindow, MousePointer2, 
  CheckCircle2, ArrowRight 
} from 'lucide-vue-next'

const services = [
  { 
    title: 'Instal Ulang Windows', 
    icon: Monitor, 
    desc: 'Laptop lemot bikin emosi? Kita instal ulang pake OS terbaru biar sat-set lagi nugas.',
    features: ['Drivers Lengkap', 'Optimasi Startup', 'Bebas Bloatware'],
    price: 'Mulai 50rb'
  },
  { 
    title: 'Reparasi Laptop', 
    icon: Laptop, 
    desc: 'Layar pecah atau mati total? Tenang, teknisi kita jagonya bedah hardware sampe sembuh.',
    features: ['Part Grade A', 'Ganti Thermal Paste', 'Cek Fisik Gratis'],
    price: 'Cek Dulu Gratis'
  },
  { 
    title: 'Install Aplikasi', 
    icon: AppWindow, 
    desc: 'Butuh Adobe atau Office buat praktikum? Kita bantu instalin tanpa drama & anti-virus.',
    features: ['Bebas Malware', 'Full Version', 'Langsung Pake'],
    price: 'Hemat & Cepat'
  },
  { 
    title: 'Reparasi Aksesoris', 
    icon: MousePointer2, 
    desc: 'Keyboard macet atau mouse error? Jangan dibuang, sini kita reparasi biar hemat jajan.',
    features: ['Keyboard Laptop', 'Mouse Gaming', 'Kabel Charger'],
    price: 'Harga Kantun'
  }
]
</script>

<template>
  <section id="layanan" class="py-16 md:py-24 px-5 bg-white">
    <div class="max-w-7xl mx-auto">
      <div class="flex flex-col md:flex-row md:items-end justify-between gap-6 mb-16 text-left">
        <div class="max-w-xl">
          <h2 class="text-3xl md:text-5xl font-black tracking-tighter uppercase italic leading-none mb-4">
            Layanan <span class="text-blue-600">Andalan.</span>
          </h2>
          <p class="text-sm md:text-base text-slate-500 font-medium italic uppercase tracking-wider">
            Solusi teknis paling jujur buat kantong mahasiswa.
          </p>
        </div>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <div v-for="s in services" :key="s.title" 
             class="group p-8 bg-slate-50 rounded-[2.5rem] border border-transparent hover:border-blue-200 hover:bg-white hover:shadow-2xl hover:shadow-blue-900/5 transition-all duration-500 flex flex-col h-full">
          
          <div class="flex justify-between items-start mb-8">
            <div class="w-12 h-12 bg-white rounded-2xl flex items-center justify-center text-blue-600 shadow-sm border border-slate-100 group-hover:bg-blue-600 group-hover:text-white transition-all">
              <component :is="s.icon" :size="24" />
            </div>
            <span class="text-[9px] font-black uppercase tracking-widest text-blue-600 bg-blue-50 px-3 py-1 rounded-full border border-blue-100 group-hover:bg-white transition-colors">
              {{ s.price }}
            </span>
          </div>

          <div class="text-left flex-grow">
            <h3 class="text-xl font-black mb-3 tracking-tight uppercase italic text-slate-900 leading-none">
              {{ s.title }}
            </h3>
            <p class="text-xs md:text-sm text-slate-500 mb-8 font-medium leading-relaxed">
              {{ s.desc }}
            </p>
          </div>

          <div class="space-y-3 pt-6 border-t border-slate-200/50">
            <div v-for="f in s.features" :key="f" class="flex items-center gap-2">
              <CheckCircle2 class="text-blue-500 shrink-0" :size="14" />
              <span class="text-[10px] font-bold text-slate-700 uppercase italic tracking-tight">{{ f }}</span>
            </div>
          </div>

          <a href="https://wa.me/..." class="mt-8 flex items-center justify-between group/link">
             <span class="text-[10px] font-black uppercase tracking-widest text-slate-400 group-hover/link:text-blue-600 transition-colors">Booking Now</span>
             <ArrowRight :size="16" class="text-slate-300 group-hover/link:text-blue-600 group-hover/link:translate-x-1 transition-all" />
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