<script setup>
import { Layers, ChevronRight } from 'lucide-vue-next'

// Data for Slide Program
const programs = [
  {
    title: 'HMI NEXT GEN',
    subtitle: 'Generasi Baru & Sistem',
    color: 'border-emerald-500',
    items: ['E-leadership reformis', 'Talent mapping dashboard'],
  },
  {
    title: 'HMI PRODIGY',
    subtitle: 'Inkubasi Bakat',
    color: 'border-cyan-500',
    items: ['Leadership lab', 'Research & policy Lab', 'Skill booster careers', 'CadrePreneur'],
  },
  {
    title: 'HMI ACTION',
    subtitle: 'Aksi Nyata',
    color: 'border-green-400',
    items: ['Policy talk', 'Digital campaign', 'HMI community action'],
  },
]
</script>

<template>
  <section
    class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col justify-center p-6 md:p-12 border-b border-white/5 py-12 md:py-20"
  >
    <!-- MENGGUNAKAN FLEX & GAP DI SINI AGAR JARAKNYA PASTI (GAP-10) -->
    <div class="container mx-auto flex flex-col gap-10">
      
      <!-- Judul Section (Margin bawah dihapus) -->
      <h3
        class="text-emerald-400 font-mono text-lg md:text-xl font-bold flex items-center justify-center md:justify-start gap-2 animate-fade-in-up"
      >
        <Layers :size="20" fill="currentColor" /> PROGRAM UNGGULAN
      </h3>
      
      <!-- Grid Program -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:gap-6">
        <div
          v-for="(prog, idx) in programs"
          :key="idx"
          :class="[
            'relative flex flex-col h-full bg-slate-900/50 backdrop-blur-md rounded-2xl overflow-hidden border-t-4 hover:bg-slate-800/50 transition-colors animate-fade-in-up',
            prog.color
          ]"
          :style="{ animationDelay: `${(idx + 1) * 150}ms` }"
        >
          <!-- Header Card -->
          <div class="p-4 md:p-6 bg-gradient-to-b from-white/5 to-transparent">
            <h4 class="text-xl md:text-2xl font-black text-white italic">
              {{ prog.title }}
            </h4>
            <p class="text-xs text-slate-400 uppercase tracking-widest mt-1">
              {{ prog.subtitle }}
            </p>
          </div>
          
          <!-- List Item -->
          <div class="p-4 md:p-6 pt-0 flex-grow">
            <ul class="space-y-2 md:space-y-4">
              <li
                v-for="(item, i) in prog.items"
                :key="i"
                class="flex items-start gap-2 md:gap-3 text-slate-300 group"
              >
                <ChevronRight
                  :size="16"
                  class="text-emerald-500 mt-0.5 md:mt-1 shrink-0 group-hover:translate-x-1 transition-transform"
                />
                <span class="capitalize text-sm md:text-base">{{ item }}</span>
              </li>
            </ul>
          </div>
          
          <!-- Bottom Glow Line -->
          <div
            class="h-1 w-full bg-gradient-to-r from-transparent via-emerald-500/20 to-transparent"
          ></div>
        </div>
      </div>
      
    </div>
  </section>
</template>

<style scoped>
/* Animasi Khusus untuk Program */
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