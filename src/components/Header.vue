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
      'fixed w-full top-0 z-50 transition-all duration-300',
      isScrolled ? 'bg-white shadow-md py-3' : 'bg-white/95 backdrop-blur-sm py-5 border-b border-gray-100'
    ]"
  >
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center">
      <!-- Logo -->
      <a href="#" class="flex items-center gap-2 text-2xl font-bold text-med-dark tracking-tight">
        <div class="w-8 h-8 bg-med-primary rounded-lg flex items-center justify-center text-white font-bold text-xl">+</div>
        MediCare
      </a>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-8">
        <a href="#especialidades" class="text-sm font-medium text-gray-600 hover:text-med-primary transition-colors">Especialidades</a>
        <a href="#nosotros" class="text-sm font-medium text-gray-600 hover:text-med-primary transition-colors">Nosotros</a>
        <a href="#contacto" class="text-sm font-medium text-gray-600 hover:text-med-primary transition-colors">Contacto</a>
        <a href="#citas" class="bg-med-primary hover:bg-blue-700 text-white px-6 py-2.5 rounded-full font-semibold text-sm transition-all shadow-md hover:shadow-lg">
          Agendar Cita
        </a>
      </nav>

      <!-- Mobile Toggle -->
      <button 
        @click="isMobileMenuOpen = !isMobileMenuOpen" 
        class="md:hidden text-med-dark p-2"
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
      class="md:hidden absolute top-full left-0 w-full bg-white shadow-xl border-t border-gray-100 flex flex-col"
    >
      <a href="#especialidades" class="p-4 border-b border-gray-50 text-center font-medium text-gray-600">Especialidades</a>
      <a href="#nosotros" class="p-4 border-b border-gray-50 text-center font-medium text-gray-600">Nosotros</a>
      <a href="#contacto" class="p-4 border-b border-gray-50 text-center font-medium text-gray-600">Contacto</a>
      <a href="#citas" class="p-4 bg-med-primary text-white text-center font-bold">Agendar Cita</a>
    </div>
  </header>
</template>
