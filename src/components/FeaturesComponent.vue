<template>
  <section class="features-section">
    <div class="container">
      <div class="features-wrapper d-flex flex-column flex-lg-row align-items-stretch justify-content-between">
        
        <!-- Feature Item 1 -->
        <div class="feature-item reveal-child text-center px-lg-3 py-3 d-flex flex-column align-items-center">
          <div class="icon-wrapper mb-3">
            <img src="/points/ocho_anios_garantia_aschee.webp" alt="8 Años de Garantía" class="feature-icon" />
          </div> 
        </div>
        
        <!-- Feature Item 2 -->
        <div class="feature-item reveal-child text-center px-lg-3 py-3 d-flex flex-column align-items-center">
          <div class="icon-wrapper mb-3">
            <img src="/points/construccion_industrial.webp" alt="Construcción Industrial" class="feature-icon" />
          </div>
        </div>
        
        <!-- Feature Item 3 -->
        <div class="feature-item reveal-child text-center px-lg-3 py-3 d-flex flex-column align-items-center">
          <div class="icon-wrapper mb-3">
            <img src="/points/maxima_eficiencia_aschee.webp" alt="Máxima Eficiencia" class="feature-icon" />
          </div>
         
        </div>
        
        <!-- Feature Item 4 -->
        <div class="feature-item reveal-child text-center px-lg-3 py-3 d-flex flex-column align-items-center">
          <div class="icon-wrapper mb-3">
            <img src="/points/bajo_mantenimiento.webp" alt="Bajo Mantenimiento" class="feature-icon" />
          </div>
        </div>
        
        <!-- Feature Item 5 -->
        <div class="feature-item reveal-child text-center px-lg-3 py-3 d-flex flex-column align-items-center">
          <div class="icon-wrapper mb-3">
            <img src="/points/soporte_nacional.webp" alt="Soporte Nacional" class="feature-icon" />
          </div>
        </div>
        
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FeaturesComponent'
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800;900&display=swap');

.features-section {
  background-color: #000c1a; /* Navy dark background matching the navbar and hero */
  color: #ffffff;
  padding: 60px 0;
  font-family: 'Inter', sans-serif;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.features-wrapper {
  width: 100%;
}

.feature-item {
  flex: 1;
  transition: transform 0.3s ease;
}

.feature-item:hover {
  transform: translateY(-4px);
}

.icon-wrapper {
  height: 84px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.feature-icon {
  height: 180px;
  width: auto;
  object-fit: contain;
}

.feature-title {
  color: #e5a93c; /* Golden yellow */
  font-size: 14px;
  font-weight: 800;
  letter-spacing: 0.05em;
  line-height: 1.25;
  margin-bottom: 12px;
  height: 36px; /* Align titles vertically by giving a fixed height for 2 lines */
  display: flex;
  align-items: center;
  justify-content: center;
}

.feature-desc {
  color: #c9d1d9; /* Faded white/gray text */
  font-size: 13px;
  line-height: 1.4;
  font-weight: 400;
  max-width: 210px;
}

/* Divider lines between items on desktop */
@media (min-width: 992px) {
  .feature-item:not(:last-child) {
    border-right: 1px solid rgba(255, 255, 255, 0.15);
  }
}

/* Stack styling for tablet and mobile devices */
@media (max-width: 991.98px) {
  .features-section {
    padding: 50px 0;
  }

  .feature-item {
    padding-top: 20px;
    padding-bottom: 20px;
  }
  
  .feature-item:not(:last-child) {
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }
  
  .feature-title {
    height: auto; /* Let it wrap naturally on mobile */
  }
  
  .feature-desc {
    max-width: 280px;
  }
}
</style>
