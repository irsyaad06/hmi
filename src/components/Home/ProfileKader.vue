<script setup>
import { Users, BookOpen, TrendingUp } from 'lucide-vue-next'
// Note: BookOpen dan TrendingUp tetap di-import untuk berjaga-jaga 
// jika nanti Anda ingin mengaktifkan kembali (uncomment) atribut kiri & kanan.
</script>

<template>
  <section
    class="mb-16 md:mb-24 px-4 md:px-8 flex flex-col items-center justify-center p-4 md:p-8 border-b border-white/5 py-12 md:py-20"
  >
    <div class="text-center mb-8 md:mb-16 animate-fade-in-up">
      <h3
        class="text-emerald-400 font-mono text-sm md:text-lg tracking-widest mb-2 flex justify-center items-center gap-2"
      >
        <Users :size="18" /> Kandidat
      </h3>
      <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white">
        Profil <span class="text-emerald-500">Calon Ketua</span>
      </h2>
    </div>

    <div
      class="flex flex-col md:flex-row items-center justify-center gap-8 md:gap-12 w-full max-w-6xl"
    >
      <!-- Atribut Kiri (Komentar Dipertahankan) -->
      <!-- <div
        class="hidden md:flex flex-col gap-8 md:gap-12 w-full md:w-1/4 items-end text-right animate-slide-right delay-200"
      >
        <div class="group">
          <h4
            class="text-lg md:text-xl font-bold text-white flex items-center justify-end gap-2 mb-1 group-hover:text-emerald-400 transition-colors"
          >
            INTELEKTUAL <BookOpen :size="20" class="text-emerald-500" />
          </h4>
          <p class="text-slate-400 text-sm">Kritis dan visioner dalam pemikiran.</p>
        </div>
      </div> -->

      <!-- Center Image -->
      <div
        class="relative w-full md:w-1/3 flex justify-center items-center animate-fade-in-up delay-100 py-6 md:py-10"
      >
        <!-- Lingkaran Animasi Belakang -->
        <!-- Catatan: animasi spin_10s_linear_infinite adalah bawaan arbitrary values Tailwind -->
        <!-- <div
          class="absolute w-[120%] h-[120%] border border-emerald-500/20 rounded-full animate-[spin_10s_linear_infinite]"
        ></div>
        <div
          class="absolute w-[110%] h-[110%] border-2 border-dashed border-emerald-500/30 rounded-full"
        ></div> -->

        <!-- Frame Foto Utama -->
        <div
          class="relative z-10 rounded-2xl overflow-hidden border-2 border-emerald-500/50 shadow-[0_0_50px_rgba(16,185,129,0.3)] bg-slate-900 h-[350px] w-[260px] md:h-[450px] md:w-[320px]"
        >
          <!-- Gambar -->
          <img
            src="/src/assets/kemal.jpeg"
            alt="Kemal Hadi Permana"
            class="w-full h-full object-cover object-top filter contrast-110"
          />
          <!-- Gradasi Hitam di bawah agar teks terbaca jelas -->
          <div
            class="absolute inset-0 bg-gradient-to-t from-slate-950 via-slate-950/40 to-transparent"
          ></div>

          <!-- Teks Nama & Jabatan -->
          <div class="absolute bottom-4 md:bottom-6 left-0 w-full text-center px-4">
            <p class="text-white font-black text-xl md:text-2xl tracking-wide mb-1">
              Kemal Hadi Permana
            </p>
            <div
              class="inline-block bg-emerald-500/20 border border-emerald-500/30 px-2 md:px-3 py-1 rounded-full backdrop-blur-sm"
            >
              <p class="text-emerald-300 text-xs tracking-widest uppercase">Calon Ketua Umum</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Atribut Kanan (Komentar Dipertahankan) -->
      <!-- <div
        class="hidden md:flex flex-col gap-8 md:gap-12 w-full md:w-1/4 items-start text-left animate-slide-left delay-200"
      >
        <div class="group">
          <h4
            class="text-lg md:text-xl font-bold text-white flex items-center gap-2 mb-1 group-hover:text-emerald-400 transition-colors"
          >
            <TrendingUp :size="20" class="text-emerald-500" /> 
            PROGRESIF
          </h4>
          <p class="text-slate-400 text-sm">Selalu bergerak maju dan adaptif.</p>
        </div>
      </div> -->
    </div>
  </section>
</template>

<style scoped>
/* Menambahkan kembali keyframes animasi yang sebelumnya terhapus */
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
  animation: fade-in-up 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

.animate-slide-right {
  animation: slide-right 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

.animate-slide-left {
  animation: slide-left 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
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