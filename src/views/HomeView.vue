<script setup>
import { onMounted } from 'vue'

// Import komponen-komponen section
import Cover from '@/components/Home/Cover.vue'
import ProfileKader from '@/components/Home/ProfileKader.vue'
import Visi from '@/components/Home/Visi.vue'
import Misi from '@/components/Home/Misi.vue'
import KonsepEkosistem from '@/components/Home/KonsepEkosistem.vue'
import Program from '@/components/Home/Program.vue'
import Closing from '@/components/Home/Closing.vue'

// --- FIX: Memaksa halaman selalu mulai dari atas saat di-load ---
onMounted(() => {
  window.scrollTo({
    top: 0,
    behavior: 'instant', // Gunakan 'instant' agar tidak terlihat efek gulir saat baru buka
  })
})
</script>

<template>
  <div
    class="bg-slate-950 text-white font-sans selection:bg-emerald-500 selection:text-white min-h-screen"
  >
    <!-- Fixed Background Component (Global untuk seluruh halaman) -->
    <div class="fixed inset-0 z-0 overflow-hidden bg-slate-950 pointer-events-none">
      <!-- Grid Pattern -->
      <div
        class="absolute inset-0 opacity-20"
        :style="{
          backgroundImage: `linear-gradient(#009639 1px, transparent 1px), linear-gradient(90deg, #009639 1px, transparent 1px)`,
          backgroundSize: '40px 40px',
        }"
      ></div>

      <!-- Glow Effects -->
      <div
        class="absolute top-0 left-0 w-96 h-96 bg-green-900 rounded-full blur-[128px] opacity-40 mix-blend-screen animate-pulse"
      ></div>
      <div
        class="absolute bottom-0 right-0 w-96 h-96 bg-emerald-800 rounded-full blur-[128px] opacity-30 mix-blend-screen"
      ></div>
    </div>

    <!-- Main Content Area -->
    <header></header>
    <main>
      <!-- Wrapper untuk menggabungkan semua section komponen -->
      <div class="relative z-10 flex flex-col px:12 md:px-40">
        <Cover />
        <ProfileKader />
        <Visi />
        <Misi />
        <KonsepEkosistem />
        <Program />
        <Closing />
      </div>
    </main>
  </div>
</template>

<style scoped>
@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

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

.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
}

.animate-slide-right {
  animation: slide-right 0.8s ease-out forwards;
}

.animate-slide-left {
  animation: slide-left 0.8s ease-out forwards;
}

.delay-100 {
  animation-delay: 100ms;
}

.delay-200 {
  animation-delay: 200ms;
}

.delay-300 {
  animation-delay: 300ms;
}
</style>
