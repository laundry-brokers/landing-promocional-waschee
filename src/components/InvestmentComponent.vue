<template>
  <section class="investment-section" id="soporte">
    <div class="container">
      <div class="row align-items-center justify-content-between g-4 g-lg-5 py-2">
        
        <!-- Left Side: Tu Inversión Trabaja Para Ti -->
        <div class="col-xl-4 col-lg-6 col-md-12 d-flex align-items-start gap-3 gap-sm-4">
          <div class="chart-icon-container">
            <!-- Left Chart SVG exactly as in mockup -->
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 160 80" class="investment-chart-svg">
              <rect x="10" y="25" width="4" height="45" rx="2" fill="white" opacity="0.2"/>
              <rect x="22" y="15" width="4" height="55" rx="2" fill="white" opacity="0.2"/>
              <rect x="34" y="20" width="4" height="50" rx="2" fill="white" opacity="0.2"/>
              <rect x="46" y="10" width="4" height="60" rx="2" fill="white" opacity="0.2"/>
              <rect x="58" y="30" width="4" height="40" rx="2" fill="white" opacity="0.2"/>
              <rect x="70" y="25" width="4" height="45" rx="2" fill="white" opacity="0.2"/>
              <rect x="82" y="15" width="4" height="55" rx="2" fill="white" opacity="0.2"/>
              <rect x="94" y="20" width="4" height="50" rx="2" fill="white" opacity="0.2"/>
              <rect x="106" y="5" width="4" height="65" rx="2" fill="white" opacity="0.2"/>
              <rect x="118" y="25" width="4" height="45" rx="2" fill="white" opacity="0.2"/>
              <rect x="130" y="15" width="4" height="55" rx="2" fill="white" opacity="0.2"/>
              <rect x="142" y="8" width="4" height="62" rx="2" fill="white" opacity="0.2"/>
              <!-- Graph line -->
              <path d="M 12 60 L 48 30 L 72 55 L 108 20 L 132 40 L 144 15" fill="none" stroke="white" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
              <!-- Graph dots -->
              <circle cx="12" cy="60" r="6" fill="white"/>
              <circle cx="48" cy="30" r="6" fill="white"/>
              <circle cx="72" cy="55" r="6" fill="white"/>
              <circle cx="108" cy="20" r="6" fill="white"/>
              <circle cx="132" cy="40" r="6" fill="white"/>
              <circle cx="144" cy="15" r="6" fill="white"/>
            </svg>
          </div>
          <div class="investment-text">
            <h3 class="investment-title m-0 text-uppercase">
              TU INVERSIÓN<br />
              <span class="text-yellow">TRABAJA PARA TI</span>
            </h3>
            <p class="investment-desc m-0 mt-2">
              Equipos que aumentan tu productividad, reducen costos operativos y elevan el nivel de tu negocio.
            </p>
          </div>
        </div>

        <!-- Vertical Divider (desktop only) -->
        <div class="col-auto d-none d-xl-block px-0">
          <div class="vertical-divider"></div>
        </div>

        <!-- Middle Side: Title & Button -->
        <div class="col-xl-3 col-lg-5 col-md-12 d-flex flex-column align-items-center align-items-lg-start text-center text-lg-start gap-3">
          <h4 class="middle-title text-uppercase m-0">
            HAZ CRECER TU NEGOCIO CON EQUIPOS PREPARADOS PARA DURAR
          </h4>
          <a href="#cotizar" class="btn-cotizar-now d-inline-flex align-items-center justify-content-between gap-3">
            COTIZAR AHORA
            <span class="arrow-wrapper">
              <svg xmlns="http://www.w3.org/2000/svg" width="8" height="12" viewBox="0 0 8 12" fill="none">
                <path d="M1.5 11L6.5 6L1.5 1" stroke="white" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </span>
          </a>
        </div>

        <!-- Right Side: 3 Benefits (exactly as in mockup) -->
        <div class="col-xl-4 col-lg-12 d-flex flex-column flex-sm-row justify-content-between gap-3 gap-md-4 mt-3 mt-xl-0 ps-xl-4">
          <!-- Benefit 1: Hasta 8 Años de Garantía -->
          <div class="benefit-card text-center">
            <div class="benefit-icon mb-2 mb-md-3">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64" class="svg-benefit" fill="none" stroke="currentColor" stroke-width="2.5">
                <path d="M32 6 C18 6 12 12 12 28 C12 44 26 54 32 58 C38 54 52 44 52 28 C52 12 46 6 32 6 Z" stroke="white" fill="none" stroke-linejoin="round"/>
                <text x="32" y="38" font-family="'Inter', sans-serif" font-weight="900" font-size="22" fill="white" text-anchor="middle">8</text>
              </svg>
            </div>
            <h5 class="benefit-title-text text-uppercase mb-1 mb-md-2">HASTA 8 AÑOS DE GARANTÍA</h5>
            <p class="benefit-desc-text m-0">Protección total para tu inversión</p>
          </div>

          <!-- Benefit 2: Bajo Mantenimiento -->
          <div class="benefit-card text-center">
            <div class="benefit-icon mb-2 mb-md-3">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="svg-benefit" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/>
              </svg>
            </div>
            <h5 class="benefit-title-text text-uppercase mb-1 mb-md-2">BAJO MANTENIMIENTO</h5>
            <p class="benefit-desc-text m-0">Diseñados para reducir tiempos muertos y costos de operación</p>
          </div>

          <!-- Benefit 3: Soporte Nacional -->
          <div class="benefit-card text-center">
            <div class="benefit-icon mb-2 mb-md-3">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="svg-benefit" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M12 2a5 5 0 0 0-5 5v3a5 5 0 0 0 10 0V7a5 5 0 0 0-5-5z"/>
                <path d="M17 16H7a4 4 0 0 0-4 4v2h18v-2a4 4 0 0 0-4-4z"/>
                <path d="M21 11.5a2.5 2.5 0 0 1-2.5 2.5h-1.5v-5h1.5a2.5 2.5 0 0 1 2.5 2.5z"/>
                <path d="M3 11.5a2.5 2.5 0 0 0 2.5 2.5h1.5v-5H5.5A2.5 2.5 0 0 0 3 11.5z"/>
                <path d="M17.5 14c.5 1 .5 2 0 3h-2.5"/>
              </svg>
            </div>
            <h5 class="benefit-title-text text-uppercase mb-1 mb-md-2">SOPORTE NACIONAL</h5>
            <p class="benefit-desc-text m-0">Asesoría especializada antes, durante y después de tu compra</p>
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
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap');

.investment-section {
  background-color: #030d1c;
  color: #ffffff;
  padding: 60px 0;
  font-family: 'Inter', sans-serif;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.chart-icon-container {
  width: 85px;
  flex-shrink: 0;
}

.investment-chart-svg {
  width: 100%;
  height: auto;
}

.investment-text {
  flex-grow: 1;
}

.investment-title {
  font-size: 19px;
  font-weight: 900;
  line-height: 1.15;
  letter-spacing: -0.010em;
}

.text-yellow {
  color: #e5a93c;
}

.investment-desc {
  font-size: 12.5px;
  color: #c9d1d9;
  line-height: 1.45;
  font-weight: 500;
}

/* Vertical Divider (Thick white line) */
.vertical-divider {
  width: 2px;
  height: 100px;
  background-color: #ffffff;
}

/* Middle Title styling */
.middle-title {
  font-size: 15px;
  font-weight: 900;
  line-height: 1.25;
  letter-spacing: 0.02em;
  color: #ffffff;
}

/* Cotizar Button */
.btn-cotizar-now {
  background-color: #e5a93c;
  color: #000c1a;
  font-weight: 900;
  font-size: 14px;
  letter-spacing: 0.04em;
  border-radius: 8px;
  padding: 12px 24px;
  text-decoration: none;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  border: none;
  width: 100%;
  max-width: 280px;
}

.btn-cotizar-now:hover {
  background-color: #f0b84c;
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(229, 169, 60, 0.4);
  color: #000c1a;
}

.arrow-wrapper {
  display: inline-flex;
  align-items: center;
}

/* Right Benefits */
.benefit-card {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 240px;
}

.benefit-icon {
  width: 44px;
  height: 44px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.svg-benefit {
  width: auto;
  height: 38px;
  color: #ffffff;
}

.benefit-title-text {
  font-size: 11.5px;
  font-weight: 800;
  color: #ffffff;
  letter-spacing: 0.02em;
  line-height: 1.25;
  text-transform: uppercase;
}

.benefit-desc-text {
  font-size: 11px;
  color: #8c9bb4;
  line-height: 1.35;
  font-weight: 500;
}

/* Tablet & Mobile responsive */
@media (max-width: 1199.98px) {
  .vertical-divider {
    display: none;
  }
}

@media (max-width: 991.98px) {
  .investment-section {
    padding: 45px 0;
  }

  .middle-title {
    max-width: 480px;
  }

  .benefit-card {
    max-width: 100%;
  }
}

@media (max-width: 575.98px) {
  .investment-section {
    padding: 35px 0;
  }
  
  .chart-icon-container {
    width: 60px;
  }

  .investment-title {
    font-size: 17px;
  }

  .btn-cotizar-now {
    max-width: 100%;
  }

  .benefit-card {
    background: rgba(255, 255, 255, 0.02);
    border: 1px solid rgba(255, 255, 255, 0.05);
    border-radius: 12px;
    padding: 14px 10px;
  }
}
</style>
