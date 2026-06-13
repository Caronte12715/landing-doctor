<script setup>
</script>

<template>
  <section class="relative pt-32 pb-20 lg:pt-48 lg:pb-32 overflow-hidden bg-white">
    <div class="max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-12 items-center">
      
      <!-- Text Content -->
      <div class="relative z-10 animate-fade-in">
        <div class="inline-block bg-med-secondary text-med-primary font-semibold px-4 py-1.5 rounded-full text-sm mb-6">
          🩺 Atención Médica de Excelencia
        </div>
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-med-dark leading-tight mb-6">
          Tu salud en las <br/>
          <span class="text-med-primary">mejores manos.</span>
        </h1>
        <p class="text-gray-500 text-lg mb-8 max-w-lg leading-relaxed">
          Ofrecemos atención médica integral con tecnología de vanguardia y un equipo de especialistas comprometidos con tu bienestar.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4">
          <a href="#citas" class="text-center bg-med-primary hover:bg-blue-700 text-white px-8 py-3.5 rounded-full font-semibold transition-all shadow-lg shadow-blue-500/30 hover:shadow-blue-500/50 hover:-translate-y-1">
            Agendar Cita
          </a>
          <a href="#contacto" class="text-center bg-white border-2 border-gray-200 hover:border-med-primary hover:text-med-primary text-gray-600 px-8 py-3.5 rounded-full font-semibold transition-all">
            Llamar por Urgencia
          </a>
        </div>

        <div class="mt-10 flex items-center gap-6 text-sm text-gray-500 font-medium">
          <div class="flex items-center gap-2">
            <svg class="w-5 h-5 text-med-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
            Doctores Certificados
          </div>
          <div class="flex items-center gap-2">
            <svg class="w-5 h-5 text-med-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
            Equipos Modernos
          </div>
        </div>
      </div>

      <!-- Image -->
      <div class="relative animate-slide-in">
        <div class="absolute inset-0 bg-med-primary rounded-3xl transform rotate-3 scale-105 opacity-10"></div>
        <div class="relative rounded-3xl overflow-hidden shadow-2xl border border-gray-100">
          <img src="/images/hero.png" alt="Doctor Profesional" class="w-full h-auto object-cover" />
        </div>
        
        <!-- Floating Badge -->
        <div class="absolute -bottom-6 -left-6 bg-white p-4 rounded-2xl shadow-xl border border-gray-100 flex items-center gap-4">
          <div class="w-12 h-12 bg-green-100 text-green-600 rounded-full flex items-center justify-center text-xl font-bold">
            4.9
          </div>
          <div>
            <div class="font-bold text-med-dark">Calificación</div>
            <div class="text-xs text-gray-500">Basado en +500 pacientes</div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes slideIn {
  from { opacity: 0; transform: translateX(30px); }
  to { opacity: 1; transform: translateX(0); }
}
.animate-fade-in { animation: fadeIn 1s ease-out forwards; }
.animate-slide-in { animation: slideIn 1s ease-out 0.2s forwards; opacity: 0; }
</style>
