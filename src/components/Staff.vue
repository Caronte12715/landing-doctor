<template>
  <section id="equipo" class="py-32 bg-white relative">
    <div class="max-w-6xl mx-auto px-6">
      <div class="text-center mb-20 reveal-up">
        <h2 class="text-4xl md:text-5xl font-bold text-med-dark mb-6 font-serif">Nuestra <span class="text-med-primary">Junta Médica</span></h2>
        <div class="w-24 h-1 bg-med-accent mx-auto mb-6"></div>
        <p class="text-gray-500 text-lg font-light">Especialistas de renombre internacional dedicados a la preservación de su salud.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
        <div v-for="(doctor, idx) in staff" :key="idx" :class="`group bg-slate-50 rounded-2xl overflow-hidden border border-gray-100 hover:shadow-2xl hover:shadow-med-primary/20 transition-all duration-500 reveal-up delay-${(idx + 1) * 100}`">
          <div class="aspect-square overflow-hidden relative">
            <div class="absolute inset-0 bg-gradient-to-t from-med-dark/80 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500 z-10 flex items-end p-6">
              <a href="#contacto" class="text-med-accent text-sm font-bold uppercase tracking-widest hover:text-white transition-colors">Solicitar Consulta →</a>
            </div>
            <img :src="doctor.image" :alt="doctor.name" class="w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-700 filter group-hover:contrast-125" />
          </div>
          <div class="p-8 text-center relative bg-white transform group-hover:-translate-y-6 transition-transform duration-500 mx-4 -mt-10 rounded-xl shadow-lg border-t-4 border-med-accent z-20">
            <h3 class="text-2xl font-bold text-med-dark mb-2 font-serif">{{ doctor.name }}</h3>
            <p class="text-med-primary font-bold text-sm mb-4 uppercase tracking-wide">{{ doctor.spec }}</p>
            <p class="text-gray-500 text-sm font-light border-t border-gray-100 pt-4">{{ doctor.edu }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const staff = [
  { name: 'Dr. Alejandro Silva', spec: 'Cardiólogo Clínico', edu: 'Universidad Nacional • 15 años de experiencia', image: 'https://images.unsplash.com/photo-1612349317150-e413f6a5b16d?auto=format&fit=crop&q=80&w=400' },
  { name: 'Dra. María Castro', spec: 'Cirujana Pediatra', edu: 'Universidad de Barcelona • 10 años de experiencia', image: 'https://images.unsplash.com/photo-1559839734-2b71ea197ec2?auto=format&fit=crop&q=80&w=400' },
  { name: 'Dr. Roberto Mendoza', spec: 'Odontólogo Especialista', edu: 'Universidad de Chile • 12 años de experiencia', image: 'https://images.unsplash.com/photo-1622253692010-333f2da6031d?auto=format&fit=crop&q=80&w=400' }
];
</script>
