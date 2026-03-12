<script setup>
import { Laptop, Instagram, MessageCircle, MapPin, ArrowUpRight } from 'lucide-vue-next'

const links = {
  layanan: [
    { name: 'Instal Ulang', href: '#layanan' },
    { name: 'Reparasi Hardware', href: '#layanan' },
    { name: 'Install Aplikasi', href: '#layanan' },
    { name: 'Servis Aksesoris', href: '#layanan' }
  ],
  perusahaan: [
    { name: 'Kenapa Kita?', href: '#kenapa' },
    { name: 'Cara Kerja', href: '#proses' },
    { name: 'Tanya Jawab', href: '#faq' },
    { name: 'Hubungi Kami', href: '#kontak' }
  ]
}
</script>

<template>
  <footer class="bg-white border-t border-slate-100 pt-20 pb-10 px-6">
    <div class="max-w-7xl mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-12 gap-12 mb-20">
        
        <div class="md:col-span-5 flex flex-col items-start">
          <div class="flex items-center gap-3 mb-8">
            <div class="w-10 h-10 bg-blue-600 rounded-2xl flex items-center justify-center shadow-xl shadow-blue-200">
              <Laptop class="text-white" :size="20" />
            </div>
            <span class="text-2xl font-black italic tracking-tighter uppercase text-slate-950">
              eduFix<span class="text-blue-600 not-italic">.</span>
            </span>
          </div>
          <p class="text-base text-slate-500 font-medium leading-relaxed max-w-sm mb-8">
            Partner terpercaya mahasiswa untuk urusan kesehatan laptop. Jujur, cepat, dan bergaransi.
          </p>
          <div class="flex gap-3">
            <a href="#" class="group flex items-center gap-2 px-4 py-2 bg-slate-50 border border-slate-100 rounded-xl hover:border-blue-200 transition-all">
              <Instagram :size="16" class="text-slate-400 group-hover:text-blue-600" />
              <span class="text-[10px] font-black uppercase tracking-widest text-slate-500 group-hover:text-slate-950">Instagram</span>
            </a>
            <a href="#" class="group flex items-center gap-2 px-4 py-2 bg-slate-50 border border-slate-100 rounded-xl hover:border-blue-200 transition-all">
              <MessageCircle :size="16" class="text-slate-400 group-hover:text-blue-600" />
              <span class="text-[10px] font-black uppercase tracking-widest text-slate-500 group-hover:text-slate-950">WhatsApp</span>
            </a>
          </div>
        </div>

        <div class="md:col-span-2 text-left">
          <div class="border-l-2 border-blue-600 pl-4 mb-6">
            <h4 class="text-[10px] font-black uppercase tracking-[0.3em] text-slate-400">Layanan</h4>
          </div>
          <ul class="space-y-4">
            <li v-for="item in links.layanan" :key="item.name">
              <a :href="item.href" class="text-sm font-bold text-slate-900 uppercase italic tracking-tight hover:text-blue-600 flex items-center gap-1 group">
                {{ item.name }}
                <ArrowUpRight :size="12" class="opacity-0 group-hover:opacity-100 transition-opacity" />
              </a>
            </li>
          </ul>
        </div>

        <div class="md:col-span-2 text-left">
          <div class="border-l-2 border-blue-600 pl-4 mb-6">
            <h4 class="text-[10px] font-black uppercase tracking-[0.3em] text-slate-400">Navigasi</h4>
          </div>
          <ul class="space-y-4">
            <li v-for="item in links.perusahaan" :key="item.name">
              <a :href="item.href" class="text-sm font-bold text-slate-900 uppercase italic tracking-tight hover:text-blue-600 flex items-center gap-1 group">
                {{ item.name }}
                <ArrowUpRight :size="12" class="opacity-0 group-hover:opacity-100 transition-opacity" />
              </a>
            </li>
          </ul>
        </div>

        <div class="md:col-span-3 text-left">
          <div class="border-l-2 border-blue-600 pl-4 mb-6">
            <h4 class="text-[10px] font-black uppercase tracking-[0.3em] text-slate-400">Kontak</h4>
          </div>
          <div class="flex items-start gap-3 mb-6">
            <MapPin class="text-blue-600 shrink-0 mt-1" :size="18" />
            <p class="text-xs font-bold text-slate-600 leading-relaxed uppercase italic">
              Jl. Kampus Merdeka No. 88, <br/> Dekat Gerbang Belakang.
            </p>
          </div>
          <p class="text-[10px] font-black text-slate-400 uppercase tracking-widest">Tersedia: 09:00 - 20:00 WIB</p>
        </div>
      </div>

      <div class="pt-10 border-t border-slate-100 flex flex-col md:flex-row justify-between items-center gap-6">
        <p class="text-[10px] font-black text-slate-400 uppercase tracking-[0.4em]">
          © 2026 eduFix Indonesia <span class="mx-2 text-slate-200">|</span> <span class="text-slate-900">Solusi Cerdas Mahasiswa</span>
        </p>
        <div class="flex items-center gap-6 text-[9px] font-black uppercase tracking-widest text-slate-400 italic">
          <a href="#" class="hover:text-slate-950">Privacy</a>
          <a href="#" class="hover:text-slate-950">Terms</a>
          <a href="#" class="hover:text-slate-950">Cookies</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
h4, a, p, span {
  font-feature-settings: "salt" on, "ss01" on;
}
</style>