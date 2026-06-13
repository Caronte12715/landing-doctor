<template>
  <section id="especialidades" class="py-24 relative overflow-hidden bg-[#F8FAFC]">
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold text-[#0F172A] mb-4">Especialidades <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-cyan-500">Médicas</span></h2>
        <p class="text-slate-500 max-w-2xl mx-auto">Atención integral y especializada para ti y tu familia, con tecnología de punta y el mejor equipo médico.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div v-for="(spec, idx) in specialties" :key="idx" class="bg-white rounded-2xl p-8 border border-slate-100 shadow-sm hover:shadow-xl hover:shadow-blue-500/10 hover:-translate-y-2 transition-all duration-300 group">
          <div class="w-16 h-16 rounded-2xl bg-blue-50 flex items-center justify-center mb-6 group-hover:bg-blue-600 transition-colors duration-300">
            <span class="text-3xl text-blue-600 group-hover:text-white transition-colors duration-300">{{ spec.icon }}</span>
          </div>
          <h3 class="text-xl font-bold text-slate-800 mb-3 group-hover:text-blue-600 transition-colors">{{ spec.title }}</h3>
          <p class="text-slate-500 text-sm leading-relaxed mb-6">{{ spec.desc }}</p>
          <a href="#contacto" class="text-blue-600 font-semibold text-sm inline-flex items-center gap-1 group-hover:gap-2 transition-all">
            Saber más
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path></svg>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const specialties = [
  { icon: '🫀', title: 'Cardiología', desc: 'Diagnóstico y tratamiento de enfermedades del corazón y sistema circulatorio con equipos de última generación.' },
  { icon: '🦷', title: 'Odontología', desc: 'Salud bucal integral, ortodoncia, implantes y estética dental para una sonrisa perfecta y saludable.' },
  { icon: '👶', title: 'Pediatría', desc: 'Cuidado especializado para el desarrollo y salud de los más pequeños en un ambiente amigable.' },
  { icon: '🦴', title: 'Traumatología', desc: 'Tratamiento de lesiones, fracturas y rehabilitación física con especialistas altamente capacitados.' }
];
</script>
