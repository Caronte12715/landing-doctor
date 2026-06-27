<script setup>
import { onMounted } from 'vue';

onMounted(() => {
  // Simple EKG animation setup if needed, handled mostly by CSS
});
</script>

<template>
  <section class="relative pt-32 pb-20 lg:pt-48 lg:pb-32 overflow-hidden bg-med-dark">
    <!-- EKG Background Animation -->
    <div class="absolute inset-0 pointer-events-none opacity-20 flex items-center justify-center">
      <svg class="w-full h-64 ekg-line" viewBox="0 0 1000 200" preserveAspectRatio="none">
        <path 
          d="M0 100 H300 L320 100 L340 50 L360 150 L380 20 L400 180 L420 100 L440 100 L460 70 L480 130 L500 100 H1000" 
          fill="none" 
          stroke="var(--color-med-accent)" 
          stroke-width="3" 
          stroke-linecap="round" 
          stroke-linejoin="round"
          class="path-animation"
        />
      </svg>
    </div>

    <!-- Soft Ambient Lights -->
    <div class="absolute top-0 left-0 w-96 h-96 bg-med-primary rounded-full mix-blend-screen filter blur-[100px] opacity-40 animate-pulse-slow"></div>
    <div class="absolute bottom-0 right-0 w-96 h-96 bg-med-accent rounded-full mix-blend-screen filter blur-[120px] opacity-10 animate-pulse-slower"></div>

    <div class="max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-12 items-center relative z-10">
      
      <!-- Text Content -->
      <div class="relative z-10 animate-fade-in">
        <div class="inline-flex items-center gap-2 bg-white/5 border border-white/10 backdrop-blur-md text-med-accent font-medium px-5 py-2 rounded-full text-sm mb-8">
          <span class="w-2 h-2 rounded-full bg-med-accent animate-ping"></span>
          Atención Médica de Élite
        </div>
        
        <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white leading-tight mb-6 font-serif">
          Tu salud, nuestra <br/>
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-med-accent to-yellow-200">obra maestra.</span>
        </h1>
        
        <p class="text-gray-300 text-lg md:text-xl mb-10 max-w-lg leading-relaxed font-light">
          Redefinimos la excelencia médica combinando especialistas de prestigio con tecnología de vanguardia en un entorno exclusivo.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4">
          <a href="#citas" class="text-center bg-med-accent hover:bg-yellow-500 text-med-dark px-8 py-4 rounded-full font-bold transition-all shadow-[0_0_20px_rgba(212,175,55,0.4)] hover:shadow-[0_0_30px_rgba(212,175,55,0.6)] hover:-translate-y-1">
            Agendar Consulta Privada
          </a>
          <a href="#servicios" class="text-center bg-white/5 border border-white/20 hover:border-med-accent hover:bg-white/10 text-white px-8 py-4 rounded-full font-medium transition-all backdrop-blur-md">
            Conocer Especialidades
          </a>
        </div>

        <div class="mt-12 flex items-center gap-8 text-sm text-gray-400 font-medium">
          <div class="flex items-center gap-3">
            <div class="w-10 h-10 rounded-full bg-white/5 flex items-center justify-center border border-white/10">
              <svg class="w-5 h-5 text-med-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
            </div>
            Junta Médica Certificada
          </div>
          <div class="flex items-center gap-3">
            <div class="w-10 h-10 rounded-full bg-white/5 flex items-center justify-center border border-white/10">
              <svg class="w-5 h-5 text-med-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"></path></svg>
            </div>
            Instalaciones Premium
          </div>
        </div>
      </div>

      <!-- Image / Glassmorphism visual -->
      <div class="relative animate-slide-in hidden lg:block">
        <div class="absolute inset-0 bg-gradient-to-tr from-med-primary to-med-accent rounded-[2rem] transform rotate-6 scale-105 opacity-20 blur-xl"></div>
        <div class="relative rounded-[2rem] overflow-hidden shadow-2xl border border-white/10 bg-med-dark/50 backdrop-blur-sm aspect-[4/5] flex items-center justify-center">
          <!-- We can use a stylized premium photo here, for now a placeholder aesthetic -->
          <img src="https://images.unsplash.com/photo-1638202993928-7267aad84c31?q=80&w=800&auto=format&fit=crop" alt="Doctor Profesional" class="w-full h-full object-cover opacity-90 mix-blend-luminosity" />
          <div class="absolute inset-0 bg-gradient-to-t from-med-dark via-transparent to-transparent opacity-80"></div>
        </div>
        
        <!-- Floating Badge -->
        <div class="absolute bottom-10 -left-10 bg-white/10 backdrop-blur-xl p-5 rounded-2xl shadow-[0_10px_40px_rgba(0,0,0,0.5)] border border-white/20 flex items-center gap-4 animate-float">
          <div class="w-14 h-14 bg-med-accent text-med-dark rounded-full flex items-center justify-center text-xl font-bold font-serif">
            4.9
          </div>
          <div>
            <div class="font-bold text-white text-lg">Excelencia</div>
            <div class="text-sm text-gray-300">Basado en +1000 pacientes</div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes slideIn {
  from { opacity: 0; transform: translateX(50px); }
  to { opacity: 1; transform: translateX(0); }
}
@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-15px); }
  100% { transform: translateY(0px); }
}
@keyframes pulseSlow {
  0%, 100% { opacity: 0.4; transform: scale(1); }
  50% { opacity: 0.2; transform: scale(1.1); }
}

.animate-fade-in { animation: fadeIn 1.2s cubic-bezier(0.16, 1, 0.3, 1) forwards; }
.animate-slide-in { animation: slideIn 1.2s cubic-bezier(0.16, 1, 0.3, 1) 0.3s forwards; opacity: 0; }
.animate-float { animation: float 6s ease-in-out infinite; }
.animate-pulse-slow { animation: pulseSlow 8s ease-in-out infinite; }
.animate-pulse-slower { animation: pulseSlow 12s ease-in-out infinite; animation-delay: 2s; }

/* SVG Line Animation */
.path-animation {
  stroke-dasharray: 2000;
  stroke-dashoffset: 2000;
  animation: drawLine 8s linear infinite;
}

@keyframes drawLine {
  0% { stroke-dashoffset: 2000; opacity: 0; }
  10% { opacity: 1; }
  80% { stroke-dashoffset: 0; opacity: 1; }
  100% { stroke-dashoffset: 0; opacity: 0; }
}

.font-serif {
  font-family: var(--font-serif);
}
</style>
