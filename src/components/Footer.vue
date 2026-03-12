<script setup>
import { Laptop, Instagram, MessageCircle, Globe, MapPin } from 'lucide-vue-next'
</script>

<template>
  <footer class="bg-slate-50 border-t border-slate-200 pt-16 pb-8 px-5">
    <div class="max-w-7xl mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16 text-left">
        
        <div class="flex flex-col gap-6">
          <div class="flex items-center gap-2.5">
            <div class="w-8 h-8 bg-blue-600 rounded-lg flex items-center justify-center shadow-lg shadow-blue-600/20">
              <Laptop class="text-white" :size="18" />
            </div>
            <span class="text-xl font-black italic tracking-tighter uppercase">eduFix<span class="text-blue-600 not-italic">.</span></span>
          </div>
          <p class="text-sm text-slate-500 leading-relaxed font-medium">
            Penyelamat laptop mahasiswa pas lagi panik dikejar deadline. Solusi servis paling jujur, sat-set, dan pastinya ramah di dompet.
          </p>
          <div class="flex gap-4">
            <a href="#" class="w-9 h-9 bg-white border border-slate-200 rounded-xl flex items-center justify-center text-slate-400 hover:text-blue-600 hover:border-blue-200 transition-all shadow-sm">
              <Instagram :size="18" />
            </a>
            <a href="#" class="w-9 h-9 bg-white border border-slate-200 rounded-xl flex items-center justify-center text-slate-400 hover:text-blue-600 hover:border-blue-200 transition-all shadow-sm">
              <MessageCircle :size="18" />
            </a>
          </div>
        </div>

        <div>
          <h4 class="text-[10px] font-black uppercase tracking-[0.2em] text-slate-400 mb-6">Layanan Kita</h4>
          <ul class="flex flex-col gap-4 text-sm font-bold text-slate-700 uppercase italic tracking-tight">
            <li><a href="#layanan" class="hover:text-blue-600 transition">Instal Ulang Windows</a></li>
            <li><a href="#layanan" class="hover:text-blue-600 transition">Reparasi Hardware</a></li>
            <li><a href="#layanan" class="hover:text-blue-600 transition">Install Aplikasi</a></li>
            <li><a href="#layanan" class="hover:text-blue-600 transition">Servis Aksesoris</a></li>
          </ul>
        </div>

        <div>
          <h4 class="text-[10px] font-black uppercase tracking-[0.2em] text-slate-400 mb-6">Menu Cepat</h4>
          <ul class="flex flex-col gap-4 text-sm font-bold text-slate-700 uppercase italic tracking-tight">
            <li><a href="#kenapa" class="hover:text-blue-600 transition">Kenapa Kita?</a></li>
            <li><a href="#proses" class="hover:text-blue-600 transition">Cara Kerja</a></li>
            <li><a href="#faq" class="hover:text-blue-600 transition">Tanya Jawab</a></li>
            <li><a href="#kontak" class="hover:text-blue-600 transition">Hubungi Teknisi</a></li>
          </ul>
        </div>

        <div>
          <h4 class="text-[10px] font-black uppercase tracking-[0.2em] text-slate-400 mb-6">Lokasi & Jam</h4>
          <div class="flex flex-col gap-5">
            <div class="flex items-start gap-3">
              <MapPin class="text-blue-600 shrink-0" :size="18" />
              <p class="text-xs font-medium text-slate-600 leading-relaxed">
                Jl. Kampus Merdeka No. 88, <br/> Dekat Gerbang Belakang (Samping Kopsis).
              </p>
            </div>
            <div class="p-4 bg-white border border-slate-200 rounded-2xl shadow-sm">
              <p class="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-1">Jam Operasional</p>
              <p class="text-xs font-bold text-slate-900 uppercase italic tracking-tight">Senin - Sabtu: 09:00 - 20:00</p>
            </div>
          </div>
        </div>
      </div>

      <div class="pt-8 border-t border-slate-200 flex flex-col md:flex-row justify-between items-center gap-4">
        <p class="text-[10px] font-bold text-slate-400 uppercase tracking-[0.3em]">
          © 2026 Solusi Cerdas Mahasiswa • eduFix ID
        </p>
        <div class="flex items-center gap-6 text-[9px] font-black uppercase tracking-widest text-slate-400 italic">
          <a href="#" class="hover:text-slate-900 transition">Privacy Policy</a>
          <a href="#" class="hover:text-slate-900 transition">Terms of Service</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
/* Menjaga konsistensi tipografi */
h4, span, a, p {
  font-feature-settings: "salt" on, "ss01" on;
}
</style>