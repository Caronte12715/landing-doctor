<template>
  <section id="testimonios" class="py-32 bg-med-dark relative overflow-hidden">
    <!-- Ambient Background -->
    <div class="absolute top-1/2 left-0 w-1/2 h-full bg-med-primary/10 rounded-full mix-blend-screen filter blur-[150px] transform -translate-y-1/2 pointer-events-none"></div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="text-center mb-20 reveal-up">
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-6 font-serif">Testimonios de <span class="text-med-accent">Excelencia</span></h2>
        <div class="w-24 h-1 bg-med-accent mx-auto mb-6 opacity-50"></div>
        <p class="text-gray-400 font-light text-lg">La salud y satisfacción de nuestros pacientes más exigentes hablan por nosotros.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
        <div v-for="(review, idx) in reviews" :key="idx" :class="`bg-white/5 p-10 rounded-3xl border border-white/10 relative backdrop-blur-md hover:bg-white/10 transition-colors duration-500 reveal-up delay-${(idx + 1) * 100}`">
          <div class="absolute top-6 right-8 text-med-accent/20 text-8xl font-serif leading-none">"</div>
          <p class="text-gray-300 mb-8 relative z-10 leading-relaxed font-light italic">"{{ review.text }}"</p>
          <div class="flex items-center gap-5 border-t border-white/10 pt-6">
            <div class="w-14 h-14 rounded-full bg-gradient-to-tr from-med-accent to-yellow-200 flex items-center justify-center text-med-dark font-bold text-xl shadow-lg">
              {{ review.initial }}
            </div>
            <div>
              <h4 class="text-white font-bold font-serif">{{ review.name }}</h4>
              <span class="text-med-primary text-sm uppercase tracking-wider font-semibold">{{ review.treatment }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const reviews = [
  { initial: 'C', name: 'Carmen Rojas', treatment: 'Cirugía Cardiovascular', text: 'El equipo médico de Medicare salvó mi vida. La atención fue impecable desde el primer diagnóstico hasta mi recuperación total. Estaré eternamente agradecida con el Dr. Silva y todo su equipo.' },
  { initial: 'M', name: 'Miguel Ángel T.', treatment: 'Odontología Integral', text: 'Perdí el miedo al dentista gracias a esta clínica. Las instalaciones son modernas, no sientes ningún dolor y los resultados de mi tratamiento de ortodoncia han sido increíbles.' },
  { initial: 'L', name: 'Laura Vargas', treatment: 'Atención Pediátrica', text: 'Llevar a mis hijos al pediatra ya no es un problema. La Dra. Castro tiene una paciencia y carisma únicos para tratar a los niños. Recomiendo la clínica a todas las madres.' },
  { initial: 'J', name: 'Javier P.', treatment: 'Rehabilitación Física', text: 'Tras mi accidente deportivo, pensé que no volvería a correr. Las sesiones de fisioterapia con tecnología de punta me ayudaron a recuperarme en tiempo récord.' }
];
</script>
