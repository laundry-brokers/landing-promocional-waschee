<template>
  <section class="trust-section" id="confianza">
    <div class="container py-3">
      <div class="row align-items-center">
        <!-- Text Content Column -->
        <div class="col-lg-4 text-center text-lg-start d-flex flex-column gap-3 py-lg-4">
          <h2 class="trust-title text-uppercase m-0">
            INGENIERÍA QUE<br />
            <span class="text-dark-blue">INSPIRA CONFIANZA</span>
          </h2>
          <p class="trust-desc m-0">
            Más de tres décadas de experiencia en el desarrollo de equipos profesionales. Combinamos investigación constante, materiales de máxima resistencia y estrictos controles de calidad para entregar equipos que superen las expectativas y permanezcan firmes con el paso del tiempo.
          </p>
        </div>
        
        <!-- Features List Image Column -->
        <div class="col-lg-6 mt-4 mt-lg-0 text-center">
          <img src="/confianza/beneficios_waschee.webp" alt="Beneficios Waschée" class="img-fluid benefits-list-img" />
        </div>
        
        <!-- Empty Spacer Column for background machine on desktop -->
        <div class="col-lg-2 d-none d-lg-block"></div>
        
        <!-- Mobile Machine Image Column (visible on mobile/tablet only) -->
        <div class="col-12 d-block d-lg-none mt-4 text-center">
          <img src="/confianza/fondo_banner1_waschee_1.webp" alt="Ingeniería Waschée" class="img-fluid mobile-machine-img" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TrustComponent'
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800;900&display=swap');

.trust-section {
  position: relative;
  background-image: url('/confianza/fondo_banner1_waschee_1.webp');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-color: #f2f4f7; /* Off-white fallback to match background */
  font-family: 'Inter', sans-serif;
  min-height: 460px;
  display: flex;
  align-items: center;
  padding: 40px 0;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

.trust-title {
  font-size: clamp(26px, 3vw, 36px);
  font-weight: 900;
  line-height: 1.1;
  color: #001229; /* Dark navy blue from mockup */
  letter-spacing: -0.010em;
}

.text-dark-blue {
  color: #001229;
}

.trust-desc {
  font-size: clamp(13px, 1.1vw, 14px);
  color: #556275;
  line-height: 1.55;
  max-width: 380px;
}

.benefits-list-img {
  max-width: 100%;
  height: auto;
  max-height: 220px;
  object-fit: contain;
}

/* Mobile responsive */
@media (max-width: 991.98px) {
  .trust-section {
    background-image: none; /* Hide background image on mobile and use flat background */
    background-color: #f2f4f7;
    padding: 60px 0;
    text-align: center;
  }
  
  .trust-desc {
    max-width: 100%;
    margin-left: auto;
    margin-right: auto;
  }
  
  .benefits-list-img {
    max-height: none;
    margin: 10px 0;
  }
  
  .mobile-machine-img {
    width: 100%;
    height: 240px;
    object-fit: cover;
    object-position: right center; /* Focus on the circular metallic machine door */
    border-radius: 16px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  }
}
</style>
