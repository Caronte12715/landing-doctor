<template>
  <section id="citas" class="py-32 bg-slate-50 relative overflow-hidden">
    <div class="absolute right-0 top-0 w-1/3 h-full bg-med-primary/5 z-0 hidden lg:block rounded-l-[150px]"></div>
    
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="flex flex-col lg:flex-row gap-20 items-center">
        <div class="w-full lg:w-1/2 reveal-left">
          <div class="inline-flex items-center gap-2 px-5 py-2 bg-med-primary/10 text-med-primary font-bold rounded-full text-sm mb-8 uppercase tracking-widest">
            <span class="w-2 h-2 rounded-full bg-med-primary animate-pulse"></span>
            Atención Inmediata
          </div>
          <h2 class="text-4xl md:text-5xl font-bold text-med-dark mb-6 leading-tight font-serif">Reserve su <br/><span class="text-med-primary">Consulta Privada</span></h2>
          <div class="w-20 h-1 bg-med-accent mb-8"></div>
          <p class="text-gray-500 mb-10 leading-relaxed font-light text-lg">
            Le brindamos un proceso de agendamiento exclusivo, sin esperas, para asegurarnos de que reciba la atención premium que usted y su familia merecen.
          </p>
          <div class="space-y-6">
            <div class="flex items-center gap-6 bg-white p-6 rounded-2xl border border-gray-100 shadow-sm hover:shadow-lg transition-shadow">
              <div class="w-14 h-14 bg-med-dark text-med-accent rounded-full flex items-center justify-center text-2xl shadow-inner">📞</div>
              <div>
                <p class="text-sm text-gray-500 font-bold uppercase tracking-widest mb-1">Línea VIP 24/7</p>
                <p class="font-serif font-bold text-2xl text-med-dark">800-123-4567</p>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full lg:w-1/2 reveal-right delay-200">
          <div class="bg-white p-10 md:p-12 rounded-[2rem] shadow-2xl shadow-med-primary/10 border border-gray-100">
            <h3 class="text-3xl font-bold text-med-dark mb-8 font-serif">Solicitud de Cita</h3>
            <form class="space-y-6">
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                <div>
                  <label class="block text-xs font-bold text-gray-500 uppercase tracking-widest mb-2">Nombre Completo</label>
                  <input type="text" class="w-full border-b-2 border-gray-200 bg-gray-50/50 rounded-t-lg px-4 py-3 focus:outline-none focus:border-med-primary focus:bg-white transition-all font-light" placeholder="Ej. Juan Pérez" />
                </div>
                <div>
                  <label class="block text-xs font-bold text-gray-500 uppercase tracking-widest mb-2">Teléfono</label>
                  <input type="tel" class="w-full border-b-2 border-gray-200 bg-gray-50/50 rounded-t-lg px-4 py-3 focus:outline-none focus:border-med-primary focus:bg-white transition-all font-light" placeholder="Su número de contacto" />
                </div>
              </div>
              <div>
                <label class="block text-xs font-bold text-gray-500 uppercase tracking-widest mb-2">Especialidad Requerida</label>
                <select class="w-full border-b-2 border-gray-200 bg-gray-50/50 rounded-t-lg px-4 py-3 focus:outline-none focus:border-med-primary focus:bg-white transition-all font-light appearance-none">
                  <option value="">Seleccione una especialidad...</option>
                  <option>Cardiología Avanzada</option>
                  <option>Odontología Estética</option>
                  <option>Pediatría Especializada</option>
                  <option>Medicina General VIP</option>
                </select>
              </div>
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                <div>
                  <label class="block text-xs font-bold text-gray-500 uppercase tracking-widest mb-2">Fecha Preferida</label>
                  <input type="date" class="w-full border-b-2 border-gray-200 bg-gray-50/50 rounded-t-lg px-4 py-3 focus:outline-none focus:border-med-primary focus:bg-white transition-all font-light text-gray-600" />
                </div>
                <div>
                  <label class="block text-xs font-bold text-gray-500 uppercase tracking-widest mb-2">Preferencia de Horario</label>
                  <select class="w-full border-b-2 border-gray-200 bg-gray-50/50 rounded-t-lg px-4 py-3 focus:outline-none focus:border-med-primary focus:bg-white transition-all font-light text-gray-600 appearance-none">
                    <option>Mañana (8am - 12pm)</option>
                    <option>Tarde (1pm - 6pm)</option>
                  </select>
                </div>
              </div>
              <button type="button" class="w-full bg-med-primary hover:bg-med-primary-dark text-white font-bold tracking-wider py-4 rounded-xl mt-6 transition-all duration-300 shadow-[0_10px_30px_rgba(15,118,110,0.3)] hover:shadow-[0_15px_40px_rgba(15,118,110,0.4)] hover:-translate-y-1">
                Confirmar Solicitud
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
