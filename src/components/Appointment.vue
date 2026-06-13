<template>
  <section id="citas" class="py-24 bg-white relative overflow-hidden">
    <div class="absolute right-0 top-0 w-1/3 h-full bg-blue-50 z-0 hidden lg:block rounded-l-[100px]"></div>
    
    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="flex flex-col lg:flex-row gap-16 items-center">
        <div class="w-full lg:w-1/2">
          <div class="inline-block px-4 py-2 bg-blue-50 text-blue-600 font-semibold rounded-full text-sm mb-6">
            Atención Rápida y Segura
          </div>
          <h2 class="text-4xl md:text-5xl font-bold text-[#0F172A] mb-6 leading-tight">Agenda tu <span class="text-blue-600">Consulta Médica</span> hoy mismo</h2>
          <p class="text-slate-500 mb-8 leading-relaxed">
            No dejes tu salud para mañana. Nuestro sistema de agendamiento es rápido, sencillo y te permite elegir al especialista que necesitas en el horario que mejor se adapte a ti.
          </p>
          <div class="space-y-4">
            <div class="flex items-center gap-4 bg-white p-4 rounded-xl border border-slate-100 shadow-sm">
              <div class="w-12 h-12 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center text-xl">📞</div>
              <div>
                <p class="text-sm text-slate-500">Línea de Emergencias 24/7</p>
                <p class="font-bold text-slate-800">800-123-4567</p>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full lg:w-1/2">
          <div class="bg-white p-8 rounded-2xl shadow-2xl shadow-blue-900/5 border border-slate-100">
            <h3 class="text-2xl font-bold text-slate-800 mb-6">Solicitar Cita</h3>
            <form class="space-y-4">
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                <div>
                  <label class="block text-sm font-medium text-slate-700 mb-1">Nombre</label>
                  <input type="text" class="w-full border border-slate-200 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-blue-600 focus:border-transparent transition-all" placeholder="Juan Pérez" />
                </div>
                <div>
                  <label class="block text-sm font-medium text-slate-700 mb-1">Teléfono</label>
                  <input type="tel" class="w-full border border-slate-200 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-blue-600 focus:border-transparent transition-all" placeholder="Tu número celular" />
                </div>
              </div>
              <div>
                <label class="block text-sm font-medium text-slate-700 mb-1">Especialidad</label>
                <select class="w-full border border-slate-200 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-blue-600 focus:border-transparent transition-all bg-white">
                  <option>Selecciona una especialidad</option>
                  <option>Cardiología</option>
                  <option>Odontología</option>
                  <option>Pediatría</option>
                  <option>Medicina General</option>
                </select>
              </div>
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                <div>
                  <label class="block text-sm font-medium text-slate-700 mb-1">Fecha preferida</label>
                  <input type="date" class="w-full border border-slate-200 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-blue-600 focus:border-transparent transition-all" />
                </div>
                <div>
                  <label class="block text-sm font-medium text-slate-700 mb-1">Horario</label>
                  <select class="w-full border border-slate-200 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-blue-600 focus:border-transparent transition-all bg-white">
                    <option>Mañana (8am - 12pm)</option>
                    <option>Tarde (1pm - 6pm)</option>
                  </select>
                </div>
              </div>
              <button type="button" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-4 rounded-lg mt-4 transition-colors duration-300 shadow-lg shadow-blue-600/30">
                Confirmar Solicitud
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
