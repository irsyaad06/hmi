<script setup>
import { Target, Hexagon } from 'lucide-vue-next'
</script>

<template>
  <section
    class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col md:flex-row items-center justify-center p-6 md:p-12 border-b border-white/5 py-12 md:py-20"
  >
    <!-- Bagian Kiri: Ikon Target -->
    <div class="w-full md:w-1/2 mb-12 md:mb-0 pr-0 md:pr-12 animate-slide-right flex justify-center md:justify-start">
      <div class="justify-start">
        <div class="absolute -inset-4 bg-emerald-500/20 blur-xl rounded-full"></div>
        <Target
          class="text-emerald-400 relative z-10 w-40 h-40 md:w-56 md:h-56 lg:w-64 lg:h-64"
          :strokeWidth="0.5"
        />
      </div>
    </div>

    <!-- Bagian Kanan: Teks Visi -->
    <div class="w-full md:w-1/2 text-center md:text-left animate-slide-left">
      <h3 class="text-emerald-400 font-mono text-lg md:text-xl font-bold mb-4 flex items-center justify-center md:justify-start gap-2">
        <Hexagon :size="20" fill="currentColor" /> VISI
      </h3>
      <p class="text-2xl md:text-3xl lg:text-5xl font-black text-white leading-tight">
        Mewujudkan HMI cabang Bandung sebagai organisasi
        <span class="text-emerald-400 underline decoration-emerald-500/30 underline-offset-8"
          >modern</span
        >
        yang <span class="text-emerald-400">adaptif</span>,
        <span class="text-emerald-400">progresif</span> dalam pergerakan dan melahirkan kader
        <span class="text-emerald-400">profesional</span>.
      </p>
    </div>
  </section>
</template>

<style scoped>
/* Animasi Khusus untuk Visi */
@keyframes slide-right {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slide-left {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.animate-slide-right {
  animation: slide-right 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

.animate-slide-left {
  animation: slide-left 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}
</style>