<script setup>
</script>

<template>
  <footer id="contacto" class="bg-med-dark text-white pt-20 pb-10">
    <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16">
      
      <!-- Brand -->
      <div>
        <a href="#" class="flex items-center gap-2 text-2xl font-bold text-white tracking-tight mb-6">
          <div class="w-8 h-8 bg-med-primary rounded-lg flex items-center justify-center text-white font-bold text-xl">+</div>
          MediCare
        </a>
        <p class="text-gray-400 leading-relaxed mb-6">
          Comprometidos con tu salud y la de tu familia. Atención médica de calidad, humana y accesible.
        </p>
      </div>

      <!-- Links -->
      <div>
        <h4 class="text-lg font-bold mb-6">Enlaces Rápidos</h4>
        <ul class="space-y-3 text-gray-400">
          <li><a href="#" class="hover:text-med-primary transition-colors">Inicio</a></li>
          <li><a href="#especialidades" class="hover:text-med-primary transition-colors">Especialidades</a></li>
          <li><a href="#nosotros" class="hover:text-med-primary transition-colors">Sobre Nosotros</a></li>
          <li><a href="#citas" class="hover:text-med-primary transition-colors">Agendar Cita</a></li>
        </ul>
      </div>

      <!-- Contact -->
      <div>
        <h4 class="text-lg font-bold mb-6">Contacto</h4>
        <ul class="space-y-4 text-gray-400">
          <li class="flex items-start gap-3">
            <span class="text-med-primary">📍</span>
            <span>Av. Salud Integral 789<br/>Edificio Médico, Piso 2</span>
          </li>
          <li class="flex items-center gap-3">
            <span class="text-med-primary">📞</span>
            <span>+1 (555) 123-4567</span>
          </li>
          <li class="flex items-center gap-3">
            <span class="text-med-primary">✉️</span>
            <span>contacto@medicare.com</span>
          </li>
        </ul>
      </div>

      <!-- Hours -->
      <div>
        <h4 class="text-lg font-bold mb-6">Horarios de Atención</h4>
        <ul class="space-y-3 text-gray-400">
          <li class="flex justify-between border-b border-gray-700 pb-2">
            <span>Lun - Vie:</span>
            <span>08:00 - 20:00</span>
          </li>
          <li class="flex justify-between border-b border-gray-700 pb-2">
            <span>Sábados:</span>
            <span>09:00 - 14:00</span>
          </li>
          <li class="flex justify-between pb-2">
            <span>Domingos:</span>
            <span class="text-med-accent font-semibold">Urgencias 24/7</span>
          </li>
        </ul>
      </div>

    </div>

    <!-- Copyright -->
    <div class="max-w-7xl mx-auto px-6 border-t border-gray-800 pt-8 flex flex-col md:flex-row justify-between items-center gap-4 text-sm text-gray-500">
      <p>&copy; 2026 MediCare Clinic. Todos los derechos reservados.</p>
      <div class="flex gap-4">
        <a href="#" class="hover:text-white transition-colors">Privacidad</a>
        <a href="#" class="hover:text-white transition-colors">Términos</a>
      </div>
    </div>
  </footer>
</template>
