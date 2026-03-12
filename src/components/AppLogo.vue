<script setup>
import { computed } from 'vue'
import logoImg from '@/assets/logo.png'

const props = defineProps({
  size: { type: String, default: 'md' }, // sm, md, lg, xl
})

// Ukuran yang jauh lebih berani (Bold Sizing)
const logoSizeClasses = computed(() => {
  switch (props.size) {
    case 'sm': 
      // Tinggi 40px (sebelumnya cuma 24px)
      return 'h-10 md:h-12' 
    case 'lg': 
      // Tinggi 80px - 96px (buat Footer atau Hero)
      return 'h-20 md:h-24'
    case 'xl':
      // Ukuran jumbo 128px
      return 'h-28 md:h-32'
    case 'md':
    default: 
      // Tinggi 56px - 64px (Standar baru untuk Navbar)
      return 'h-14 md:h-16' 
  }
})
</script>

<template>
  <a href="/" class="flex items-center group focus:outline-none shrink-0" title="eduFix Home">
    
    <div :class="[logoSizeClasses, 'aspect-[3/2] flex items-center justify-center']">
      <img 
        v-if="logoImg"
        :src="logoImg" 
        alt="eduFix Logo" 
        class="h-full w-full object-contain transition-transform duration-500 group-hover:scale-105"
      />
      
      <span v-else class="text-xl font-black text-blue-600 uppercase italic tracking-tighter">
        eduFix
      </span>
    </div>

  </a>
</template>

<style scoped>
/* Menjaga kualitas gambar tetap tajam meski ukurannya besar */
img {
  image-rendering: -webkit-optimize-contrast;
  backface-visibility: hidden;
}
</style>