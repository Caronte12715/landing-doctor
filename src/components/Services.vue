<script setup>
const specialities = [
  {
    title: 'Medicina General',
    desc: 'Atención primaria, diagnósticos precisos y seguimiento integral para toda la familia.',
    icon: '🩺'
  },
  {
    title: 'Pediatría',
    desc: 'Cuidado especializado para los más pequeños, desde recién nacidos hasta adolescentes.',
    icon: '👶'
  },
  {
    title: 'Cardiología',
    desc: 'Prevención, diagnóstico y tratamiento de enfermedades cardiovasculares.',
    icon: '❤️'
  },
  {
    title: 'Odontología',
    desc: 'Salud bucal completa: limpiezas, ortodoncia, implantes y estética dental.',
    icon: '🦷'
  },
  {
    title: 'Laboratorio',
    desc: 'Análisis clínicos rápidos y precisos con equipos de última generación.',
    icon: '🔬'
  },
  {
    title: 'Rayos X y Ecografía',
    desc: 'Imágenes diagnósticas de alta resolución para tratamientos exactos.',
    icon: '🩻'
  }
];
</script>

<template>
  <section id="especialidades" class="py-24 bg-med-gray">
    <div class="max-w-7xl mx-auto px-6">
      
      <div class="text-center mb-16 max-w-2xl mx-auto">
        <h2 class="text-3xl md:text-4xl font-bold text-med-dark mb-4">Nuestras Especialidades</h2>
        <p class="text-gray-500 text-lg">
          Cubrimos todas tus necesidades médicas en un solo lugar, con especialistas altamente capacitados.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div 
          v-for="(spec, index) in specialities" 
          :key="index"
          class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 hover:shadow-xl transition-all duration-300 hover:-translate-y-2 group cursor-pointer"
        >
          <div class="w-14 h-14 bg-med-secondary rounded-xl flex items-center justify-center text-3xl mb-6 group-hover:bg-med-primary group-hover:scale-110 transition-all duration-300">
            <span class="group-hover:grayscale-0 transition-all">{{ spec.icon }}</span>
          </div>
          <h3 class="text-xl font-bold text-med-dark mb-3">{{ spec.title }}</h3>
          <p class="text-gray-500 leading-relaxed">{{ spec.desc }}</p>
        </div>
      </div>

    </div>
  </section>
</template>
