<template>
  <header class="hero-section d-flex align-items-center" id="inicio">
    <div class="container py-3 py-lg-4">
      <div class="row align-items-center">
        <!-- Text and Promo Column -->
        <div class="col-lg-5 text-center text-lg-start d-flex flex-column gap-3">
          <!-- Promo Badge -->
          <div>
            <span class="badge-promo">PROMOCIÓN</span>
          </div>
          
          <!-- Heading -->
          <div class="hero-heading-container">
            <h1 class="hero-title m-0">TODO</h1>
            <h1 class="hero-title hero-title-yellow m-0">INCLUIDO</h1>
            <p class="hero-subtitle mt-2 mb-0">
              AL ADQUIRIR TU <br class="d-none d-lg-block" />
              <span class="fw-extrabold">DÚO INDUSTRIAL</span>
            </p>
          </div>
          
          <!-- Benefits Image -->
          <div class="benefits-container d-flex justify-content-center justify-content-lg-start">
            <img :src="benefitsImageSrc" alt="Puesta en marcha y fletes" class="img-fluid benefits-img" />
          </div>
          
          <!-- CTA Button & Disclaimer -->
          <div class="cta-container d-flex flex-column align-items-center align-items-lg-start gap-2 mt-2">
            <a href="#cotizar" class="btn btn-hero-cta d-flex align-items-center gap-2 justify-content-center">
              SOLICITAR ESTA PROMOCIÓN
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-right" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z"/>
              </svg>
            </a>
            <span class="disclaimer-text">*Aplican términos y condiciones.</span>
          </div>
        </div>
        
        <!-- Machines and Warranty Column -->
        <div class="col-lg-7 mt-4 mt-lg-0 text-center">
          <div class="row align-items-center justify-content-center g-3">
            <!-- Machines Display -->
            <div class="col-12 col-md-10 position-relative text-center">
              <!-- Image of Machines -->
              <div class="machines-image-wrapper w-100">
                <img src="/hero/lavadoras_modelos_waschee.webp" alt="Lavadora y Secadora Industrial Waschée" class="img-fluid machines-img" />
              </div>
            </div>
            
            <!-- Warranty Display -->
            <div class="col-12 col-md-2 mt-3 mt-md-0 d-flex flex-column align-items-center justify-content-center">
              <div class="warranty-badge-container d-flex flex-column align-items-center">
                <img src="/hero/ocho_anios_garantia.webp" alt="8 Años de Garantía" class="img-fluid warranty-badge-img mb-2" />
                <p class="warranty-text m-0 text-center">
                  COMPROMISO REAL CON LA CALIDAD DE LOS EQUIPOS
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeroComponent',
  data() {
    return {
      benefitsImageSrc: '/hero/puesta_marcha_mantenimiento_colored.webp'
    };
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800;900&display=swap');

.hero-section {
  position: relative;
  background-image: url('/hero/banner1_todo_incluido_waschee_WLCA.webp');
  background-size: cover;
  background-position: center;
  color: #ffffff;
  min-height: 600px;
  display: flex;
  align-items: center;
  font-family: 'Inter', sans-serif;
  overflow: hidden;
  padding: 60px 0;
}

/* Badge Promo */
.badge-promo {
  background-color: #e5a93c;
  color: #000c1a;
  font-weight: 900;
  font-size: 14px;
  letter-spacing: 0.1em;
  padding: 8px 24px;
  border-radius: 8px;
  display: inline-block;
}

/* Heading styles */
.hero-title {
  font-size: clamp(45px, 5.5vw, 74px);
  font-weight: 900;
  line-height: 0.95;
  letter-spacing: -0.01em;
}

.hero-title-yellow {
  color: #e5a93c;
}

.hero-subtitle {
  font-size: clamp(20px, 2.2vw, 25px);
  font-weight: 700;
  line-height: 1.2;
  letter-spacing: 0.05em;
  color: #ffffff;
  text-transform: uppercase;
}

.fw-extrabold {
  font-weight: 900;
}

/* Benefits styling */
.benefits-container {
  margin-top: 10px;
  margin-bottom: 10px;
}

.benefits-img {
  max-width: 100%;
  height: auto;
  max-height: 90px;
  object-fit: contain;
}

/* CTA Button & Disclaimer */
.btn-hero-cta {
  background-color: #e5a93c;
  color: #000c1a;
  font-weight: 800;
  font-size: 15px;
  letter-spacing: 0.05em;
  border-radius: 12px;
  padding: 16px 40px;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  border: none;
  width: auto;
}

.btn-hero-cta:hover {
  background-color: #f0b84c;
  color: #000c1a;
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(229, 169, 60, 0.4);
}

.btn-hero-cta:active {
  transform: translateY(0);
}

.disclaimer-text {
  font-size: 11px;
  color: rgba(255, 255, 255, 0.4);
  font-style: italic;
  font-weight: 600;
}

/* Machines section */
.machines-image-wrapper {
  position: relative;
  display: inline-block;
}

.machines-img {
  max-height: 480px;
  object-fit: contain;
  transition: transform 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
}

.machines-image-wrapper:hover .machines-img {
  transform: scale(1.02);
}

/* Warranty Styling */
.warranty-badge-container {
  max-width: 160px;
}

.warranty-badge-img {
  max-height: 140px;
  object-fit: contain;
  transition: transform 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
}

.warranty-badge-container:hover .warranty-badge-img {
  transform: rotate(3deg) scale(1.05);
}

.warranty-text {
  font-size: 10px;
  font-weight: 700;
  line-height: 1.4;
  letter-spacing: 0.08em;
  color: rgba(255, 255, 255, 0.85);
}

/* Responsive adjustments */
@media (max-width: 991.98px) {
  .hero-section {
    padding: 35px 0;
    text-align: center;
    min-height: auto;
  }
  
  .hero-title {
    font-size: clamp(38px, 8vw, 56px);
  }

  .hero-subtitle {
    font-size: clamp(16px, 3.5vw, 22px);
  }

  .benefits-img {
    max-height: 75px;
  }

  .btn-hero-cta {
    width: 100%;
    max-width: 360px;
    padding: 14px 28px;
    font-size: 14px;
  }
  
  .machines-img {
    max-height: 320px;
  }
  
  .warranty-badge-container {
    margin-top: 10px;
  }

  .warranty-badge-img {
    max-height: 110px;
  }
}

@media (max-width: 575.98px) {
  .hero-section {
    padding: 25px 0;
  }

  .badge-promo {
    font-size: 12px;
    padding: 6px 18px;
  }

  .hero-title {
    font-size: 36px;
  }
  
  .hero-subtitle {
    font-size: 16px;
  }

  .benefits-img {
    max-height: 60px;
  }
  
  .machines-img {
    max-height: 240px;
  }

  .warranty-badge-img {
    max-height: 95px;
  }
}
</style>
