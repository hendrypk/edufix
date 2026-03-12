<script setup>
import { MessageCircle, Search, Zap, Sparkles } from 'lucide-vue-next'

const steps = [
  { title: 'Chat WA', icon: MessageCircle },
  { title: 'Diagnosis', icon: Search },
  { title: 'Eksekusi', icon: Zap },
  { title: 'Siap Nugas', icon: Sparkles }
]
</script>

<template>
  <section id="proses" class="py-20 px-5 bg-white text-left">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-5xl font-black mb-12 tracking-tighter uppercase italic">Cuma 4 Langkah.</h2>
      <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
        <div v-for="(step, i) in steps" :key="i" class="flex flex-col items-start gap-4 p-6 bg-slate-50 rounded-3xl">
          <div class="w-10 h-10 bg-blue-600 text-white rounded-xl flex items-center justify-center font-bold">
            {{ i + 1 }}
          </div>
          <p class="font-black italic uppercase text-sm tracking-tight">{{ step.title }}</p>
        </div>
      </div>
    </div>
  </section>
</template>