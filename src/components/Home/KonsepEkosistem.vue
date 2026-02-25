<script setup>
// Tidak ada import icon yang dibutuhkan untuk komponen ini
</script>

<template>
  <section
    class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col items-center justify-center p-4 md:p-8 border-b border-white/5 overflow-hidden py-12 md:py-20"
  >
    <!-- Wrapper Diagram Ekosistem -->
    <div
      class="relative w-[280px] h-[280px] md:w-[500px] md:h-[500px] lg:w-[600px] lg:h-[600px] flex items-center justify-center scale-50 sm:scale-75 md:scale-100 animate-fade-in-up"
    >
      <!-- Lingkaran Animasi Latar -->
      <div
        class="absolute inset-0 border border-emerald-500/20 rounded-full animate-[spin_10s_linear_infinite]"
      ></div>
      <div
        class="absolute inset-8 md:inset-12 border border-emerald-500/30 rounded-full animate-[spin_15s_linear_infinite_reverse] border-dashed"
      ></div>
      <div class="absolute inset-16 md:inset-24 border border-emerald-500/40 rounded-full"></div>

      <!-- Inti (Core) -->
      <div
        class="absolute w-24 h-24 md:w-36 md:h-36 lg:w-48 lg:h-48 bg-emerald-600 rounded-full flex items-center justify-center shadow-[0_0_50px_rgba(16,185,129,0.5)] z-20"
      >
        <div class="text-center text-white">
          <h2 class="text-2xl md:text-3xl lg:text-4xl font-black">HmI</h2>
          <p class="text-[8px] md:text-[10px] lg:text-xs font-mono tracking-widest mt-1">
            ECOSYSTEM 4.0
          </p>
        </div>
      </div>

      <!-- Node / Satelit -->
      <div
        class="absolute top-0 left-1/2 -translate-x-1/2 -translate-y-4 md:-translate-y-6 bg-slate-900 border border-emerald-400 text-emerald-400 px-3 md:px-6 py-1.5 md:py-3 rounded-full font-bold shadow-lg z-20 whitespace-nowrap text-xs md:text-sm"
      >
        NEXT GEN (System)
      </div>
      <div
        class="absolute bottom-6 md:bottom-10 right-0 translate-x-1/4 md:translate-x-0 bg-slate-900 border border-emerald-400 text-emerald-400 px-3 md:px-6 py-1.5 md:py-3 rounded-full font-bold shadow-lg z-20 whitespace-nowrap text-xs md:text-sm"
      >
        ACTION (Movement)
      </div>
      <div
        class="absolute bottom-6 md:bottom-10 left-0 -translate-x-1/4 md:translate-x-0 bg-slate-900 border border-emerald-400 text-emerald-400 px-3 md:px-6 py-1.5 md:py-3 rounded-full font-bold shadow-lg z-20 whitespace-nowrap text-xs md:text-sm"
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
    <p class="mt-6 md:mt-8 text-slate-400 font-mono text-center max-w-xl text-sm md:text-base px-4 animate-fade-in-up delay-200">
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