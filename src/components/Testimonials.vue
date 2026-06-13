<template>
  <section id="testimonios" class="py-24 bg-[#0F172A]">
    <div class="max-w-6xl mx-auto px-6 relative">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">Pacientes <span class="text-blue-400">Satisfechos</span></h2>
        <p class="text-slate-400">La salud y el bienestar de nuestros pacientes es nuestra mejor carta de presentación.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div v-for="(review, idx) in reviews" :key="idx" class="bg-slate-800 p-8 rounded-2xl border border-slate-700 relative">
          <div class="absolute top-6 right-8 text-blue-500/20 text-6xl font-serif">"</div>
          <p class="text-slate-300 mb-6 relative z-10 leading-relaxed">{{ review.text }}</p>
          <div class="flex items-center gap-4">
            <div class="w-12 h-12 rounded-full bg-blue-600 flex items-center justify-center text-white font-bold text-lg">
              {{ review.initial }}
            </div>
            <div>
              <h4 class="text-white font-semibold">{{ review.name }}</h4>
              <span class="text-blue-400 text-sm">{{ review.treatment }}</span>
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
