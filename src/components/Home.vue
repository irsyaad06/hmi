<script setup>
import { onMounted } from 'vue'
import {
  Target,
  Cpu,
  Globe,
  Users,
  Zap,
  Layers,
  Activity,
  Share2,
  TrendingUp,
  Hexagon,
  ChevronRight,
  Shield,
  BookOpen,
} from 'lucide-vue-next'

// --- FIX: Memaksa halaman selalu mulai dari atas saat di-load ---
onMounted(() => {
  window.scrollTo({
    top: 0,
    behavior: 'instant', // Gunakan 'instant' agar tidak terlihat efek gulir saat baru buka
  })
})

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
  <div class="bg-slate-950 text-white font-sans selection:bg-emerald-500 selection:text-white">
    <!-- Fixed Background Component -->
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

    <!-- Scrollable Content Area -->
    <div class="relative z-10 flex flex-col">
      <!-- Section 1: Cover -->
      <section
        class="min-h-screen flex flex-col justify-center items-center p-6 md:p-12 text-center border-b border-white/5 relative"
      >
        <div
          class="inline-block px-4 py-1 mb-6 border border-emerald-500/50 rounded-full bg-emerald-900/20 text-emerald-300 font-mono text-sm tracking-[0.2em] animate-fade-in-up"
        >
          GRAND DESIGN 2025-2026
        </div>
        <h1
          class="text-5xl md:text-6xl lg:text-8xl font-bold text-white mb-2 tracking-tighter leading-tight animate-fade-in-up delay-100"
        >
          HMI
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-green-600"
            >Reformis</span
          >
        </h1>
        <h2
          class="text-xl md:text-2xl lg:text-3xl text-emerald-100 font-light mt-4 tracking-wide animate-fade-in-up delay-200"
        >
          HMI NEXT-Gen
        </h2>
        <div
          class="mt-8 md:mt-12 flex items-center gap-2 text-slate-400 animate-fade-in-up delay-300"
        >
          <span class="h-[1px] w-8 md:w-12 bg-emerald-500/50"></span>
          <span class="font-mono text-xs md:text-sm uppercase">HMI Ecosystem 4.0</span>
          <span class="h-[1px] w-8 md:w-12 bg-emerald-500/50"></span>
        </div>

        <!-- Scroll Indicator (Opsional, agar user tau harus scroll) -->
        <div
          class="absolute bottom-6 md:bottom-10 animate-bounce text-emerald-500/50 flex flex-col items-center"
        >
          <p class="text-xs font-mono mb-2">SCROLL DOWN</p>
          <div class="w-[1px] h-6 md:h-8 bg-emerald-500/50"></div>
        </div>
      </section>

      <!-- Section 2: Profile Kader -->
      <section
        class="mb-16 md:mb-24 px-4 md:px-8 flex flex-col items-center justify-center p-4 md:p-8 border-b border-white/5 py-12 md:py-20"
      >
        <div class="text-center mb-8 md:mb-16 animate-fade-in-up">
          <h3
            class="text-emerald-400 font-mono text-sm md:text-lg tracking-widest mb-2 flex justify-center items-center gap-2"
          >
            <Users :size="18" /> THE FUTURE CADRE
          </h3>
          <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white">
            Profil <span class="text-emerald-500">Calon Ketua</span>
          </h2>
        </div>

        <div
          class="flex flex-col md:flex-row items-center justify-center gap-8 md:gap-12 w-full max-w-6xl"
        >
          <!-- Atribut Kiri (Diaktifkan kembali agar foto tidak sendirian) -->
          <div
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
          </div>

          <!-- Center Image (Disesuaikan untuk foto baru) -->
          <div
            class="relative w-full md:w-1/3 flex justify-center items-center animate-fade-in-up delay-100 py-6 md:py-10"
          >
            <!-- Lingkaran Animasi Belakang -->
            <div
              class="absolute w-[120%] h-[120%] border border-emerald-500/20 rounded-full animate-[spin_10s_linear_infinite]"
            ></div>
            <div
              class="absolute w-[110%] h-[110%] border-2 border-dashed border-emerald-500/30 rounded-full"
            ></div>

            <!-- Frame Foto Utama -->
            <div
              class="relative z-10 rounded-2xl overflow-hidden border-2 border-emerald-500/50 shadow-[0_0_50px_rgba(16,185,129,0.3)] bg-slate-900 h-[350px] w-[260px] md:h-[450px] md:w-[320px]"
            >
              <!-- Pastikan nama file foto yang Anda upload sesuai dengan src di bawah ini -->
              <!-- Misalnya Anda simpan dengan nama kemal.jpg di folder public/img/ -->
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

          <!-- Atribut Kanan -->
          <div
            class="hidden md:flex flex-col gap-8 md:gap-12 w-full md:w-1/4 items-start text-left animate-slide-left delay-200"
          >
            <div class="group">
              <h4
                class="text-lg md:text-xl font-bold text-white flex items-center gap-2 mb-1 group-hover:text-emerald-400 transition-colors"
              >
                <TrendingUp :size="20" class="text-emerald-500" /> PROGRESIF
              </h4>
              <p class="text-slate-400 text-sm">Selalu bergerak maju dan adaptif.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Section 3: Visi -->
      <section
        class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col md:flex-row items-center justify-center p-6 md:p-12 border-b border-white/5 py-12 md:py-20"
      >
        <div class="w-full md:w-1/2 mb-8 md:mb-0 pr-0 md:pr-12 animate-slide-right">
          <div class="relative">
            <div class="absolute -inset-4 bg-emerald-500/20 blur-xl rounded-full"></div>
            <Target
              :size="80"
              class="text-emerald-400 relative z-10 mx-auto md:mx-0 md:w-[200px]"
              :strokeWidth="0.5"
            />
          </div>
        </div>
        <div class="w-full md:w-1/2 text-left animate-slide-left">
          <h3 class="text-emerald-400 font-mono text-lg md:text-xl mb-4 flex items-center gap-2">
            <Hexagon :size="16" fill="currentColor" /> VISI ORGANISASI
          </h3>
          <p class="text-lg md:text-3xl lg:text-5xl font-bold text-white leading-tight">
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

      <!-- Section 4: Misi -->
      <section
        class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col justify-center p-6 md:p-12 border-b border-white/5 bg-emerald-950/10 py-12 md:py-20"
      >
        <div class="container mx-auto">
          <h3
            class="text-emerald-400 font-mono text-lg md:text-xl mb-8 md:mb-12 flex items-center gap-2"
          >
            <Hexagon :size="16" fill="currentColor" /> MISI STRATEGIS
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4 md:gap-6">
            <div
              v-for="(m, idx) in missions"
              :key="idx"
              class="group p-4 md:p-8 border border-emerald-500/20 bg-emerald-950/30 backdrop-blur-sm hover:bg-emerald-900/40 hover:border-emerald-500/60 transition-all duration-300 rounded-xl"
            >
              <div
                class="text-emerald-400 mb-4 transform group-hover:scale-110 transition-transform duration-300 bg-emerald-900/50 p-3 w-fit rounded-lg"
              >
                <component :is="m.icon" :size="24" md:size="32" />
              </div>
              <h4 class="text-lg md:text-xl font-bold text-white mb-2 group-hover:text-emerald-300">
                {{ m.title }}
              </h4>
              <p
                class="text-slate-300 text-sm leading-relaxed border-l-2 border-emerald-500/30 pl-4"
              >
                {{ m.desc }}
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- Section 5: Ecosystem Concept -->
      <section
        class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col items-center justify-center p-4 md:p-8 border-b border-white/5 overflow-hidden py-12 md:py-20"
      >
        <div
          class="relative w-[280px] h-[280px] md:w-[500px] md:h-[500px] lg:w-[600px] lg:h-[600px] flex items-center justify-center scale-50 sm:scale-75 md:scale-100"
        >
          <div
            class="absolute inset-0 border border-emerald-500/20 rounded-full animate-[spin_10s_linear_infinite]"
          ></div>
          <div
            class="absolute inset-8 md:inset-12 border border-emerald-500/30 rounded-full animate-[spin_15s_linear_infinite_reverse] border-dashed"
          ></div>
          <div
            class="absolute inset-16 md:inset-24 border border-emerald-500/40 rounded-full"
          ></div>

          <div
            class="absolute w-24 h-24 md:w-36 md:h-36 lg:w-48 lg:h-48 bg-emerald-600 rounded-full flex items-center justify-center shadow-[0_0_50px_rgba(16,185,129,0.5)] z-20"
          >
            <div class="text-center text-white">
              <h2 class="text-2xl md:text-3xl lg:text-4xl font-black">HMI</h2>
              <p class="text-[8px] md:text-[10px] lg:text-xs font-mono tracking-widest mt-1">
                ECOSYSTEM 4.0
              </p>
            </div>
          </div>

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
        <p
          class="mt-6 md:mt-8 text-slate-400 font-mono text-center max-w-xl text-sm md:text-base px-4"
        >
          Integrasi seamless antara sistem digital, pengembangan kapasitas kader, dan aksi nyata
          yang berdampak.
        </p>
      </section>

      <!-- Section 6: Programs -->
      <section
        class="mb-16 md:mb-24 px-4 md:px-8 lg:px-12 flex flex-col justify-center p-6 md:p-12 border-b border-white/5 py-12 md:py-20"
      >
        <div class="container mx-auto">
          <h3
            class="text-emerald-400 font-mono text-lg md:text-xl mb-8 md:mb-12 flex items-center gap-2"
          >
            <Layers :size="16" fill="currentColor" /> PROGRAM UNGGULAN
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:gap-6">
            <div
              v-for="(prog, idx) in programs"
              :key="idx"
              :class="`relative flex flex-col h-full bg-slate-900/50 backdrop-blur-md rounded-2xl overflow-hidden border-t-4 ${prog.color} hover:bg-slate-800/50 transition-colors`"
            >
              <div class="p-4 md:p-6 bg-gradient-to-b from-white/5 to-transparent">
                <h4 class="text-xl md:text-2xl font-black text-white italic">
                  {{ prog.title }}
                </h4>
                <p class="text-xs text-slate-400 uppercase tracking-widest mt-1">
                  {{ prog.subtitle }}
                </p>
              </div>
              <div class="p-4 md:p-6 pt-0 flex-grow">
                <ul class="space-y-2 md:space-y-4">
                  <div
                    v-for="(item, i) in prog.items"
                    :key="i"
                    class="flex items-start gap-2 md:gap-3 text-slate-300 group"
                  >
                    <ChevronRight
                      :size="16"
                      class="text-emerald-500 mt-0.5 md:mt-1 shrink-0 group-hover:translate-x-1 transition-transform"
                    />
                    <span class="capitalize text-sm md:text-base">{{ item }}</span>
                  </div>
                </ul>
              </div>
              <div
                class="h-1 w-full bg-gradient-to-r from-transparent via-emerald-500/20 to-transparent"
              ></div>
            </div>
          </div>
        </div>
      </section>

      <!-- Section 7: Closing -->
      <section
        class="pb-16 md:pb-24 px-4 md:px-8 lg:px-12 flex flex-col justify-center items-center p-6 md:p-12 text-center bg-gradient-to-t from-emerald-950/50 to-transparent py-12 md:py-20"
      >
        <div class="relative z-10 max-w-4xl">
          <!-- <div class="mb-8 mx-auto w-24 h-24 bg-emerald-500/10 rounded-full flex items-center justify-center border border-emerald-500/30">
            <TrendingUp :size="48" class="text-emerald-400" />
          </div> -->
          <h2
            class="text-lg md:text-3xl lg:text-5xl font-bold text-white mb-6 md:mb-8 leading-normal"
          >
            "Masa depan tidak dimenangkan oleh mereka yang menolak perubahan, tapi oleh mereka yang
            <span class="text-emerald-400 bg-emerald-900/30 px-1 md:px-2"
              >menciptakan perubahan</span
            >
            dengan integritas."
          </h2>

          <!-- <div class="mt-12 p-8 border border-white/10 rounded-2xl bg-white/5 backdrop-blur-sm inline-block">
            <h3 class="text-xl font-bold text-white mb-2">MARI BERKOLABORASI</h3>
            <p class="text-emerald-400 font-mono mb-4">HMI CABANG BANDUNG</p>
            <div class="flex justify-center gap-6 text-slate-400 text-sm">
              <span class="flex items-center gap-2"><Share2 :size="14" /> @hmi_bandung</span>
              <span class="flex items-center gap-2"><Globe :size="14" /> hmibandung.org</span>
            </div>
          </div> -->
        </div>
      </section>
    </div>
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
