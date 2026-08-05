<template>
  <section class="investment-section">
    <div class="container">
      <div class="investment-wrapper d-flex flex-column flex-xl-row align-items-center justify-content-between gap-4 gap-xl-0">
        
        <!-- Left Side: Tu Inversión Trabaja Para Ti -->
        <div class="investment-left-block d-flex align-items-start gap-3">
          <!-- Big Inline Chart SVG with Trend Line and Nodes -->
          <div class="investment-chart-icon-wrapper flex-shrink-0">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" class="inversion-svg-icon">
              <!-- Horizontal Base Line -->
              <line x1="6" y1="52" x2="58" y2="52" />
              <!-- Vertical Base Line -->
              <line x1="6" y1="12" x2="6" y2="52" />
              <!-- 4 bars -->
              <line x1="16" y1="52" x2="16" y2="38" />
              <line x1="26" y1="52" x2="26" y2="28" />
              <line x1="36" y1="52" x2="36" y2="22" />
              <line x1="46" y1="52" x2="46" y2="14" />
              <!-- Trend Line -->
              <path d="M10 46 L21 34 L31 38 L48 10" />
              <!-- Trend Arrow -->
              <polyline points="40 10 48 10 48 18" />
              <!-- Nodes -->
              <circle cx="10" cy="46" r="2.5" fill="currentColor" stroke="none" />
              <circle cx="21" cy="34" r="2.5" fill="currentColor" stroke="none" />
              <circle cx="31" cy="38" r="2.5" fill="currentColor" stroke="none" />
              <circle cx="48" cy="10" r="2.5" fill="currentColor" stroke="none" />
            </svg>
          </div>
          <div class="investment-left-text">
            <h3 class="investment-left-title m-0 text-uppercase">
              TU INVERSIÓN<br />
              <span class="text-yellow">TRABAJA PARA TI</span>
            </h3>
            <p class="investment-left-desc m-0 mt-1">
              Equipos que aumentan tu productividad, reducen costos operativos y elevan el nivel nivel de tu negocio.
            </p>
          </div>
        </div>
        
        <!-- Vertical Divider (hidden on mobile/tablet) -->
        <div class="vertical-divider d-none d-xl-block"></div>
        
        <!-- Right Side: Haz Crecer Tu Negocio + Items -->
        <div class="investment-right-block d-flex flex-column flex-md-row align-items-center justify-content-between gap-4 gap-xl-4 flex-fill w-100 ps-xl-4">
          <!-- Text and CTA Button -->
          <div class="cta-cta-container d-flex flex-column align-items-center align-items-md-start text-center text-md-start gap-2">
            <h4 class="investment-right-title m-0 text-uppercase">
              HAZ CRECER TU NEGOCIO CON EQUIPOS<br />
              <span class="text-yellow">PREPARADOS PARA DURAR.</span>
            </h4>
            <a href="#cotizar" class="btn btn-investment-cta d-flex align-items-center gap-2 justify-content-center mt-1">
              COTIZAR AHORA
              <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" fill="currentColor" class="bi bi-chevron-right" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z"/>
              </svg>
            </a>
          </div>
          
          <!-- Small Items Row -->
          <div class="cta-benefits-row d-flex align-items-start justify-content-center justify-content-md-end gap-3 gap-lg-4 flex-wrap flex-md-nowrap">
            <!-- Item 1: Mayor Productividad -->
            <div class="cta-benefit-item d-flex flex-column align-items-center text-center">
              <div class="cta-benefit-icon-wrapper mb-2">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" class="inversion-svg-icon-small">
                  <line x1="6" y1="52" x2="58" y2="52" />
                  <line x1="6" y1="12" x2="6" y2="52" />
                  <line x1="16" y1="52" x2="16" y2="38" />
                  <line x1="26" y1="52" x2="26" y2="28" />
                  <line x1="36" y1="52" x2="36" y2="22" />
                  <line x1="46" y1="52" x2="46" y2="14" />
                  <path d="M10 46 L21 34 L31 38 L48 10" />
                  <polyline points="40 10 48 10 48 18" />
                  <circle cx="10" cy="46" r="2.5" fill="currentColor" stroke="none" />
                  <circle cx="21" cy="34" r="2.5" fill="currentColor" stroke="none" />
                  <circle cx="31" cy="38" r="2.5" fill="currentColor" stroke="none" />
                  <circle cx="48" cy="10" r="2.5" fill="currentColor" stroke="none" />
                </svg>
              </div>
              <span class="cta-benefit-text">MAYOR<br />PRODUCTIVIDAD</span>
            </div>
            
            <!-- Item 2: Menor Costo Operativo -->
            <div class="cta-benefit-item d-flex flex-column align-items-center text-center">
              <div class="cta-benefit-icon-wrapper mb-2">
                <img src="/points/maxima_eficiencia_aschee.webp" alt="Menor Costo" class="cta-benefit-img" />
              </div>
              <span class="cta-benefit-text">MENOR COSTO<br />OPERATIVO</span>
            </div>
            
            <!-- Item 3: Hasta 8 Años de Garantía -->
            <div class="cta-benefit-item d-flex flex-column align-items-center text-center">
              <div class="cta-benefit-icon-wrapper mb-2">
                <img src="/points/ocho_anios_garantia_aschee.webp" alt="8 Años Garantía" class="cta-benefit-img" />
              </div>
              <span class="cta-benefit-text">HASTA 8 AÑOS<br />DE GARANTÍA</span>
            </div>
            
            <!-- Item 4: Soporte y Respaldo Confiable -->
            <div class="cta-benefit-item d-flex flex-column align-items-center text-center">
              <div class="cta-benefit-icon-wrapper mb-2">
                <img src="/points/soporte_nacional.webp" alt="Soporte y Respaldo" class="cta-benefit-img" />
              </div>
              <span class="cta-benefit-text">SOPORTE Y RESPALDO<br />CONFIABLE</span>
            </div>
          </div>
          
        </div>
        
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'InvestmentComponent'
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800;900&display=swap');

.investment-section {
  background-color: #000c1a; /* Navy dark background matching features and navbar */
  color: #ffffff;
  padding: 30px 0;
  font-family: 'Inter', sans-serif;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

/* Left block */
.investment-left-block {
  max-width: 380px;
}

.investment-chart-icon-wrapper {
  color: #ffffff;
  width: 48px;
  height: 48px;
}

.inversion-svg-icon {
  width: 100%;
  height: 100%;
  object-fit: contain;
  opacity: 0.9;
}

.investment-left-title {
  font-size: 15px;
  font-weight: 900;
  line-height: 1.2;
  color: #ffffff;
  letter-spacing: 0.02em;
}

.text-yellow {
  color: #e5a93c; /* Golden yellow */
}

.investment-left-desc {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.7);
  line-height: 1.4;
  font-weight: 400;
}

/* Vertical Divider */
.vertical-divider {
  width: 1px;
  height: 75px;
  background-color: rgba(255, 255, 255, 0.15);
  margin: 0 15px;
  align-self: center;
  flex-shrink: 0;
}

/* Right block */
.investment-right-block {
  display: flex;
}

.cta-cta-container {
  max-width: 310px;
}

.investment-right-title {
  font-size: 14.5px;
  font-weight: 800;
  line-height: 1.25;
  color: #ffffff;
  letter-spacing: 0.02em;
}

/* CTA Button */
.btn-investment-cta {
  background-color: #e5a93c; /* Yellow */
  color: #000c1a;
  font-weight: 800;
  font-size: 13px;
  letter-spacing: 0.05em;
  border-radius: 8px;
  padding: 10px 24px;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  border: none;
  width: auto;
}

.btn-investment-cta:hover {
  background-color: #f0b84c;
  transform: translateY(-2px);
  box-shadow: 0 6px 18px rgba(229, 169, 60, 0.3);
}

.btn-investment-cta:active {
  transform: translateY(0);
}

/* Benefits list */
.cta-benefits-row {
  flex-shrink: 0;
}

.cta-benefit-item {
  width: 90px;
  flex-shrink: 0;
}

.cta-benefit-icon-wrapper {
  height: 38px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.inversion-svg-icon-small {
  width: auto;
  height: 32px;
  color: #ffffff;
  opacity: 0.9;
}

.cta-benefit-img {
  height: 34px;
  width: auto;
  object-fit: contain;
}

.cta-benefit-text {
  font-size: 8.5px;
  font-weight: 700;
  color: #ffffff;
  letter-spacing: 0.05em;
  line-height: 1.3;
}

/* Responsive adjustments */
@media (max-width: 1199.98px) {
  .investment-left-block {
    max-width: 100%;
    text-align: center;
    justify-content: center;
  }
  
  .investment-left-text {
    text-align: left;
  }
  
  .cta-benefits-row {
    width: 100%;
    justify-content: space-around !important;
  }
}

@media (max-width: 767.98px) {
  .investment-section {
    padding: 35px 0;
  }
  
  .investment-left-block {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  
  .investment-left-text {
    text-align: center;
  }
  
  .investment-right-block {
    flex-direction: column !important;
    gap: 25px !important;
  }
  
  .cta-cta-container {
    max-width: 100%;
  }
  
  .btn-investment-cta {
    width: 100%;
    max-width: 260px;
  }
  
  .cta-benefits-row {
    gap: 15px !important;
    flex-wrap: wrap !important;
  }
  
  .cta-benefit-item {
    width: 42%;
    margin-bottom: 10px;
  }
}
</style>
