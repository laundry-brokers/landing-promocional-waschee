<template>
  <section class="features-section" id="equipos">
    <div class="container">
      <div class="features-grid">
        
        <!-- Feature Item 1 -->
        <div class="feature-item reveal-child">
          <div class="icon-wrapper">
            <img src="/points/ocho_anios_garantia_aschee.webp" alt="8 Años de Garantía" class="feature-icon" />
          </div> 
        </div>
        
        <!-- Feature Item 2 -->
        <div class="feature-item reveal-child">
          <div class="icon-wrapper">
            <img src="/points/construccion_industrial.webp" alt="Construcción Industrial" class="feature-icon" />
          </div>
        </div>
        
        <!-- Feature Item 3 -->
        <div class="feature-item reveal-child">
          <div class="icon-wrapper">
            <img src="/points/maxima_eficiencia_aschee.webp" alt="Máxima Eficiencia" class="feature-icon" />
          </div>
        </div>
        
        <!-- Feature Item 4 -->
        <div class="feature-item reveal-child">
          <div class="icon-wrapper">
            <img src="/points/bajo_mantenimiento.webp" alt="Bajo Mantenimiento" class="feature-icon" />
          </div>
        </div>
        
        <!-- Feature Item 5 -->
        <div class="feature-item reveal-child">
          <div class="icon-wrapper">
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
  background-color: #000c1a;
  color: #ffffff;
  padding: 50px 0;
  font-family: 'Inter', sans-serif;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 20px;
  align-items: center;
  width: 100%;
}

.feature-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 10px 8px;
  transition: transform 0.3s ease;
}

.feature-item:hover {
  transform: translateY(-4px);
}

.icon-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}

.feature-icon {
  width: auto;
  max-width: 100%;
  height: auto;
  max-height: 140px;
  object-fit: contain;
  transition: transform 0.3s ease;
}

/* Divider lines between items on desktop */
@media (min-width: 992px) {
  .feature-item:not(:last-child) {
    border-right: 1px solid rgba(255, 255, 255, 0.12);
  }
}

/* Tablet Layout (768px - 991px) */
@media (max-width: 991.98px) and (min-width: 576px) {
  .features-section {
    padding: 40px 0;
  }

  .features-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 24px 16px;
  }

  .feature-item {
    background: rgba(255, 255, 255, 0.02);
    border: 1px solid rgba(255, 255, 255, 0.06);
    border-radius: 12px;
    padding: 16px 12px;
  }

  .feature-icon {
    max-height: 120px;
  }
}

/* Mobile Layout (<576px) */
@media (max-width: 575.98px) {
  .features-section {
    padding: 35px 0;
  }

  .features-grid {
    grid-template-columns: 1fr;
    gap: 16px;
  }

  .feature-item {
    background: rgba(255, 255, 255, 0.02);
    border: 1px solid rgba(255, 255, 255, 0.06);
    border-radius: 12px;
    padding: 16px 10px;
  }

  .feature-icon {
    max-height: 110px;
  }
}
</style>
