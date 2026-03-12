<script setup>
import { Monitor, Laptop, AppWindow, MousePointer2, CheckCircle2 } from 'lucide-vue-next'

const services = [
  { title: 'Instal Ulang', icon: Monitor, desc: 'Laptop lemot? Kita instal OS baru biar ngebut lagi.', features: ['Driver Lengkap', 'Optimasi Startup'] },
  { title: 'Reparasi Laptop', icon: Laptop, desc: 'Layar pecah atau mati total? Teknisi kita jagonya.', features: ['Part Grade A', 'Ganti Thermal Paste'] },
  { title: 'Install Aplikasi', icon: AppWindow, desc: 'Butuh Adobe atau Office? Kita bantu instalin.', features: ['Bebas Virus', 'Langsung Pake'] },
  { title: 'Reparasi Aksesori', icon: MousePointer2, desc: 'Keyboard atau mouse rusak? Bawa sini aja.', features: ['Keyboard Laptop', 'Mouse Gaming'] }
]
</script>

<template>
  <section id="layanan" class="py-20 px-5 bg-slate-50">
    <div class="max-w-7xl mx-auto text-left">
      <h2 class="text-3xl md:text-5xl font-black mb-12 tracking-tighter uppercase italic underline decoration-blue-600 decoration-4">Layanan Kita.</h2>
      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-4">
        <div v-for="s in services" :key="s.title" class="p-8 bg-white border border-slate-100 rounded-[2rem] hover:shadow-xl transition-all group">
          <div class="w-12 h-12 bg-blue-50 text-blue-600 rounded-xl flex items-center justify-center mb-6 group-hover:bg-blue-600 group-hover:text-white transition-all">
            <component :is="s.icon" :size="24" />
          </div>
          <h3 class="text-lg font-black mb-3 tracking-tight uppercase leading-tight italic">{{ s.title }}</h3>
          <p class="text-xs text-slate-500 mb-6 font-medium leading-relaxed">{{ s.desc }}</p>
          <div class="space-y-2 border-t border-slate-50 pt-4">
            <div v-for="f in s.features" :key="f" class="flex items-center gap-2 text-[10px] font-bold text-slate-800 uppercase italic">
              <CheckCircle2 class="text-blue-500" :size="12" /> {{ f }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>