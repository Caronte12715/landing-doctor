<script setup>
const specialities = [
  {
    title: 'Medicina General',
    desc: 'Atención primaria y diagnósticos precisos para un seguimiento integral.',
    icon: '🩺'
  },
  {
    title: 'Cardiología Avanzada',
    desc: 'Prevención y tratamiento con tecnología cardiovascular de última generación.',
    icon: '❤️'
  },
  {
    title: 'Odontología Estética',
    desc: 'Diseño de sonrisa y salud bucal con materiales premium y mínima invasión.',
    icon: '🦷'
  },
  {
    title: 'Pediatría Especializada',
    desc: 'Cuidado experto para el desarrollo óptimo de los más pequeños.',
    icon: '👶'
  },
  {
    title: 'Laboratorio Clínico',
    desc: 'Análisis ultra-precisos procesados in-house para resultados inmediatos.',
    icon: '🔬'
  },
  {
    title: 'Imágenes Diagnósticas',
    desc: 'Ecografías 4D y Rayos X digitales de altísima resolución.',
    icon: '🩻'
  }
];
</script>

<template>
  <section id="servicios" class="py-32 bg-med-gray relative">
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      
      <div class="text-center mb-20 max-w-3xl mx-auto reveal-up">
        <h2 class="text-4xl md:text-5xl font-bold text-med-dark mb-6 font-serif">Nuestras Especialidades</h2>
        <div class="w-24 h-1 bg-med-accent mx-auto mb-6"></div>
        <p class="text-gray-500 text-lg md:text-xl font-light">
          Cubrimos todas tus necesidades médicas con un nivel de exigencia y exclusividad sin precedentes.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
        <div 
          v-for="(spec, index) in specialities" 
          :key="index"
          :class="`bg-white p-10 rounded-2xl shadow-sm border border-gray-100 hover:shadow-2xl hover:shadow-med-accent/10 transition-all duration-500 hover:-translate-y-2 group cursor-pointer reveal-up delay-${(index % 3 + 1) * 100}`"
        >
          <div class="w-16 h-16 bg-slate-50 border border-gray-100 rounded-2xl flex items-center justify-center text-3xl mb-8 group-hover:bg-med-accent group-hover:border-med-accent transition-all duration-500 shadow-sm">
            <span class="group-hover:scale-110 transition-transform duration-500">{{ spec.icon }}</span>
          </div>
          <h3 class="text-2xl font-bold text-med-dark mb-4 font-serif">{{ spec.title }}</h3>
          <p class="text-gray-500 font-light leading-relaxed">{{ spec.desc }}</p>
        </div>
      </div>

    </div>
  </section>
</template>
