<script setup>
import { Hexagon, Cpu, Activity, Zap, Users } from 'lucide-vue-next'

// Data for Slide Misi
const missions = [
  {
    icon: Cpu,
    title: 'Transformasi Digital',
    desc: 'Mentransformasikan tata kelola organisasi menuju ekosistem digital yang modern.',
  },
  {
    icon: Activity,
    title: 'Adaptif Zaman',
    desc: 'Menyelaraskan langkah organisasi agar senantiasa adaptif terhadap perubahan zaman.',
  },
  {
    icon: Zap,
    title: 'Nalar Kritis',
    desc: 'Merawat nalar kritis dalam gerakan yang progresif dan penuh kebermanfaatan.',
  },
  {
    icon: Users,
    title: 'Kader Profesional',
    desc: 'Membina kapasitas kader demi lahirnya insan profesional yang berintegritas.',
  },
]
</script>

<template>
  <section
    class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col justify-center p-6 md:p-12 border-b border-white/5 bg-emerald-950/10 py-12 md:py-20"
  >
    <!-- MENGGUNAKAN FLEX & GAP DI SINI AGAR JARAKNYA PASTI -->
    <div class="container mx-auto flex flex-col gap-10">
      
      <!-- Judul Bagian (Margin dihapus karena sudah diatur oleh gap di atas) -->
      <h3
        class="text-emerald-400 font-mono text-lg md:text-xl font-bold flex items-center justify-center md:justify-start gap-2 animate-fade-in-up"
      >
        <Hexagon :size="20" fill="currentColor" /> MISI STRATEGIS
      </h3>
      
      <!-- Grid Misi -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
        <div
          v-for="(m, idx) in missions"
          :key="idx"
          class="group p-6 md:p-8 border border-emerald-500/20 bg-emerald-950/30 backdrop-blur-sm hover:bg-emerald-900/40 hover:border-emerald-500/60 transition-all duration-300 rounded-xl animate-fade-in-up"
          :style="{ animationDelay: `${(idx + 1) * 150}ms` }"
        >
          <!-- Ikon Misi -->
          <div
            class="text-emerald-400 mb-4 transform group-hover:scale-110 transition-transform duration-300 bg-emerald-900/50 p-3 w-fit rounded-lg"
          >
            <!-- Menggunakan class tailwind untuk responsive sizing -->
            <component :is="m.icon" class="w-7 h-7 md:w-8 md:h-8" />
          </div>
          
          <!-- Teks Misi -->
          <h4 class="text-xl md:text-2xl font-bold text-white mb-2 group-hover:text-emerald-300 transition-colors">
            {{ m.title }}
          </h4>
          <p class="text-slate-300 text-sm md:text-base leading-relaxed border-l-2 border-emerald-500/30 pl-4">
            {{ m.desc }}
          </p>
        </div>
      </div>
      
    </div>
  </section>
</template>

<style scoped>
/* Animasi Khusus untuk Misi */
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