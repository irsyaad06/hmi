<script setup>
// Tidak ada import icon yang dibutuhkan untuk komponen ini
</script>

<template>
  <section
    class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col items-center justify-center p-4 md:p-8 border-b border-white/5 overflow-hidden py-12 md:py-20"
  >
    <!-- Wrapper Diagram Ekosistem -->
    <!-- Menghapus "scale-50" dan menggantinya dengan penyesuaian width & height yang proporsional -->
    <div
      class="relative w-[320px] h-[320px] sm:w-[400px] sm:h-[400px] md:w-[500px] md:h-[500px] lg:w-[600px] lg:h-[600px] flex items-center justify-center animate-fade-in-up mt-4 md:mt-0"
    >
      <!-- Lingkaran Animasi Latar -->
      <div
        class="absolute inset-0 border border-emerald-500/20 rounded-full animate-[spin_10s_linear_infinite]"
      ></div>
      <div
        class="absolute inset-8 sm:inset-10 md:inset-12 border border-emerald-500/30 rounded-full animate-[spin_15s_linear_infinite_reverse] border-dashed"
      ></div>
      <div class="absolute inset-16 sm:inset-20 md:inset-24 border border-emerald-500/40 rounded-full"></div>

      <!-- Inti (Core) -->
      <div
        class="absolute w-28 h-28 sm:w-32 sm:h-32 md:w-36 md:h-36 lg:w-48 lg:h-48 bg-emerald-600 rounded-full flex items-center justify-center shadow-[0_0_50px_rgba(16,185,129,0.5)] z-20"
      >
        <div class="text-center text-white">
          <h2 class="text-3xl sm:text-4xl lg:text-4xl font-black">HmI</h2>
          <p class="text-[10px] md:text-xs font-mono tracking-widest mt-1">
            ECOSYSTEM 4.0
          </p>
        </div>
      </div>

      <!-- Node / Satelit -->
      <!-- Top -->
      <div
        class="absolute top-0 md:top-2 left-1/2 -translate-x-1/2 -translate-y-4 md:-translate-y-6 bg-slate-900 border border-emerald-400 text-emerald-400 px-4 md:px-6 py-2 md:py-3 rounded-full font-bold shadow-lg z-20 whitespace-nowrap text-[10px] sm:text-xs md:text-sm"
      >
        NEXT GEN (System)
      </div>
      
      <!-- Bottom Right -->
      <div
        class="absolute bottom-8 sm:bottom-10 md:bottom-12 right-[-10px] sm:right-0 md:right-2 bg-slate-900 border border-emerald-400 text-emerald-400 px-4 md:px-6 py-2 md:py-3 rounded-full font-bold shadow-lg z-20 whitespace-nowrap text-[10px] sm:text-xs md:text-sm"
      >
        ACTION (Movement)
      </div>
      
      <!-- Bottom Left -->
      <div
        class="absolute bottom-8 sm:bottom-10 md:bottom-12 left-[-10px] sm:left-0 md:left-2 bg-slate-900 border border-emerald-400 text-emerald-400 px-4 md:px-6 py-2 md:py-3 rounded-full font-bold shadow-lg z-20 whitespace-nowrap text-[10px] sm:text-xs md:text-sm"
      >
        PRODIGY (People)
      </div>

      <!-- Garis Koneksi -->
      <div
        class="absolute top-1/2 left-1/2 w-full h-[1px] bg-emerald-500/30 -translate-x-1/2 -translate-y-1/2 rotate-90"
      ></div>
      <div
        class="absolute top-1/2 left-1/2 w-full h-[1px] bg-emerald-500/30 -translate-x-1/2 -translate-y-1/2 rotate-[30deg]"
      ></div>
      <div
        class="absolute top-1/2 left-1/2 w-full h-[1px] bg-emerald-500/30 -translate-x-1/2 -translate-y-1/2 rotate-[-30deg]"
      ></div>
    </div>
    
    <!-- Teks Penjelasan -->
    <p class="mt-10 md:mt-12 text-slate-400 font-mono text-center max-w-xl text-sm md:text-base px-4 animate-fade-in-up delay-200">
      Integrasi seamless antara sistem digital, pengembangan kapasitas kader, dan aksi nyata yang
      berdampak.
    </p>
  </section>
</template>

<style scoped>
/* Menambahkan keyframes animasi untuk konsistensi */
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
  opacity: 0;
}

.delay-200 {
  animation-delay: 200ms;
}
</style>