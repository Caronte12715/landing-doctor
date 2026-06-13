<template>
  <section id="equipo" class="py-24 bg-white relative">
    <div class="max-w-6xl mx-auto px-6">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold text-[#0F172A] mb-4">Nuestro <span class="text-blue-600">Equipo Médico</span></h2>
        <p class="text-slate-500">Profesionales altamente calificados comprometidos con tu salud y bienestar.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div v-for="(doctor, idx) in staff" :key="idx" class="group bg-slate-50 rounded-2xl overflow-hidden border border-slate-100 hover:shadow-xl transition-all duration-300">
          <div class="aspect-square overflow-hidden relative">
            <div class="absolute inset-0 bg-blue-600/20 mix-blend-multiply opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-10"></div>
            <img :src="doctor.image" :alt="doctor.name" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-700" />
          </div>
          <div class="p-8 text-center relative bg-white transform group-hover:-translate-y-4 transition-transform duration-300 mx-4 -mt-8 rounded-xl shadow-lg border border-slate-100 z-20">
            <h3 class="text-xl font-bold text-slate-800 mb-1">{{ doctor.name }}</h3>
            <p class="text-blue-600 font-semibold text-sm mb-3">{{ doctor.spec }}</p>
            <p class="text-slate-500 text-sm">{{ doctor.edu }}</p>
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
