<script setup>
import { TrendingUp } from 'lucide-vue-next'
</script>

<template>
  <section
    class="pb-16 md:pb-24 px-4 md:px-8 lg:px-12 flex flex-col justify-center items-center text-center bg-gradient-to-t from-emerald-950/50 to-transparent py-12 md:py-20"
  >
    <!-- Menambahkan w-full, mx-auto, flex, flex-col, dan items-center agar seluruh isi dipaksa rata tengah -->
    <div class="relative z-10 w-full max-w-4xl mx-auto flex flex-col items-center animate-fade-in-up">
      
      <!-- Lingkaran Ikon -->
      <div class="mb-8 w-24 h-24 bg-emerald-500/10 rounded-full flex items-center justify-center border border-emerald-500/30">
        <TrendingUp :size="48" class="text-emerald-400" />
      </div>
      
      <!-- Teks Kutipan -->
      <h2 class="text-xl md:text-3xl lg:text-5xl font-bold text-white mb-6 md:mb-8 leading-normal md:leading-relaxed">
        "Masa depan tidak dimenangkan oleh mereka yang menolak perubahan, tapi oleh mereka yang
        <span class="text-emerald-400 bg-emerald-900/30 px-2 py-1 rounded-sm">menciptakan perubahan</span>
        dengan integritas."
      </h2>
      
    </div>
  </section>
</template>

<style scoped>
/* Animasi Khusus untuk Penutup */
@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  animation: fade-in-up 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  opacity: 0; /* Menyembunyikan elemen sebelum animasi dimulai */
}
</style>