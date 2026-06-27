<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
  <header 
    :class="[
      'fixed w-full top-0 z-50 transition-all duration-500',
      isScrolled ? 'bg-med-dark/95 backdrop-blur-md shadow-2xl shadow-med-primary-dark/20 py-3 border-b border-white/10' : 'bg-transparent py-6'
    ]"
  >
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center">
      <!-- Logo -->
      <a href="#" class="flex items-center gap-3 text-2xl font-bold text-white tracking-tight font-serif">
        <div class="w-10 h-10 bg-gradient-to-tr from-med-accent to-yellow-200 rounded-xl flex items-center justify-center text-med-dark font-bold text-2xl shadow-lg">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M12 4v16m8-8H4"></path></svg>
        </div>
        Signature<span class="text-med-accent font-light">Clinic</span>
      </a>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-10">
        <a href="#especialidades" class="text-sm font-medium text-gray-300 hover:text-white transition-colors">Especialidades</a>
        <a href="#nosotros" class="text-sm font-medium text-gray-300 hover:text-white transition-colors">Instalaciones</a>
        <a href="#contacto" class="text-sm font-medium text-gray-300 hover:text-white transition-colors">VIP</a>
        <a href="#citas" class="bg-white/10 border border-white/20 hover:border-med-accent hover:bg-med-accent hover:text-med-dark text-white px-7 py-2.5 rounded-full font-bold text-sm transition-all shadow-md backdrop-blur-sm">
          Reservar
        </a>
      </nav>

      <!-- Mobile Toggle -->
      <button 
        @click="isMobileMenuOpen = !isMobileMenuOpen" 
        class="md:hidden text-white p-2"
      >
        <svg v-if="!isMobileMenuOpen" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div 
      v-if="isMobileMenuOpen" 
      class="md:hidden absolute top-full left-0 w-full bg-med-dark shadow-2xl border-t border-white/10 flex flex-col backdrop-blur-xl"
    >
      <a href="#especialidades" class="p-5 border-b border-white/5 text-center font-medium text-gray-300">Especialidades</a>
      <a href="#nosotros" class="p-5 border-b border-white/5 text-center font-medium text-gray-300">Instalaciones</a>
      <a href="#contacto" class="p-5 border-b border-white/5 text-center font-medium text-gray-300">VIP</a>
      <a href="#citas" class="p-5 bg-gradient-to-r from-med-accent to-yellow-400 text-med-dark text-center font-bold">Reservar</a>
    </div>
  </header>
</template>
