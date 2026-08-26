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
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" class="svg-benefit" fill="none">
                <!-- Shield shape with gold border -->
                <path d="M24 5L9 11v13c0 9.8 6.4 19 15 21.5 8.6-2.5 15-11.7 15-21.5V11L24 5z" fill="rgba(229, 169, 60, 0.12)" stroke="#e5a93c" stroke-width="2.2" stroke-linejoin="round"/>
                <!-- Central medal / badge with 8 -->
                <circle cx="24" cy="22" r="8" stroke="#ffffff" stroke-width="1.8" fill="rgba(0, 12, 26, 0.8)"/>
                <text x="24" y="26.5" font-family="'Inter', sans-serif" font-weight="900" font-size="12.5" fill="#e5a93c" text-anchor="middle">8</text>
                <!-- Ribbon -->
                <path d="M20.5 32l3.5-2 3.5 2v-4h-7v4z" fill="#e5a93c"/>
              </svg>
            </div>
            <h5 class="benefit-title-text text-uppercase mb-1 mb-md-2">HASTA 8 AÑOS DE GARANTÍA</h5>
            <p class="benefit-desc-text m-0">Compromiso real con la calidad de los equipos</p>
          </div>

          <!-- Benefit 2: Bajo Mantenimiento -->
          <div class="benefit-card text-center">
            <div class="benefit-icon mb-2 mb-md-3">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" class="svg-benefit" fill="none">
                <!-- Gear base -->
                <circle cx="24" cy="24" r="19" fill="rgba(229, 169, 60, 0.1)" stroke="rgba(229, 169, 60, 0.3)" stroke-width="1.5"/>
                <!-- Cog teeth indicators -->
                <path d="M24 8v3m0 26v3m16-16h-3M11 24H8m22.6-8.6l-2.1 2.1m-15 15l-2.1 2.1m0-19.2l2.1 2.1m15 15l2.1 2.1" stroke="rgba(255, 255, 255, 0.4)" stroke-width="2" stroke-linecap="round"/>
                <!-- Precision Wrench -->
                <path d="M16 32l9-9m3-3l3.5-3.5a4 4 0 0 1 5.7 5.7L33.7 25.7a4 4 0 0 1-5.7 0l-1-1" stroke="#e5a93c" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"/>
                <circle cx="16" cy="32" r="2.5" fill="#ffffff"/>
              </svg>
            </div>
            <h5 class="benefit-title-text text-uppercase mb-1 mb-md-2">BAJO MANTENIMIENTO</h5>
            <p class="benefit-desc-text m-0">Diseñados para reducir tiempos muertos y costos de operación</p>
          </div>

          <!-- Benefit 3: Soporte Nacional -->
          <div class="benefit-card text-center">
            <div class="benefit-icon mb-2 mb-md-3">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" class="svg-benefit" fill="none">
                <!-- Outer subtle glow circle -->
                <circle cx="24" cy="24" r="19" fill="rgba(229, 169, 60, 0.1)" stroke="rgba(229, 169, 60, 0.3)" stroke-width="1.5"/>
                <!-- Professional Headset -->
                <path d="M14 24c0-5.5 4.5-10 10-10s10 4.5 10 10v4a3 3 0 0 1-3 3h-1.5v-7h2.5v-1c0-4.4-3.6-7-8-7s-8 2.6-8 7v1h2.5v7H17a3 3 0 0 1-3-3v-4z" fill="rgba(229, 169, 60, 0.15)" stroke="#e5a93c" stroke-width="2.2" stroke-linejoin="round"/>
                <!-- Mic stem -->
                <path d="M29 33v2a3.5 3.5 0 0 1-3.5 3.5h-3.5" stroke="#ffffff" stroke-width="2" stroke-linecap="round"/>
                <circle cx="21" cy="38.5" r="2" fill="#e5a93c"/>
                <!-- Broadcast / signal arc -->
                <path d="M36 18a14 14 0 0 1 0 12" stroke="#ffffff" stroke-width="1.8" stroke-linecap="round" opacity="0.6"/>
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
  width: 52px;
  height: 52px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(229, 169, 60, 0.08);
  border: 1px solid rgba(229, 169, 60, 0.2);
  border-radius: 14px;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
}

.benefit-card:hover .benefit-icon {
  background: rgba(229, 169, 60, 0.15);
  border-color: rgba(229, 169, 60, 0.45);
  transform: translateY(-3px);
  box-shadow: 0 6px 18px rgba(229, 169, 60, 0.25);
}

.svg-benefit {
  width: 34px;
  height: 34px;
  transition: transform 0.3s ease;
}

.benefit-card:hover .svg-benefit {
  transform: scale(1.08);
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
