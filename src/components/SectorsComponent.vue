<template>
  <section class="sectors-section" id="sectores">
    <div class="container">
      <!-- Section Title -->
      <div class="row mb-5">
        <div class="col-12 text-center">
          <h2 class="section-title text-uppercase m-0">
            DISEÑADOS PARA LOS NEGOCIOS QUE NO PUEDEN DETENERSE
          </h2>
        </div>
      </div>
      
      <!-- Sector Cards Grid -->
      <div class="row g-4 justify-content-center">
        <!-- Card 1: Hotelería -->
        <div class="col-sm-12 col-md-6 col-lg-3 reveal-child">
          <div class="card sector-card h-100">
            <img src="/business/hoteleria_card.png" alt="Hotelería" class="card-img-top sector-img" />
            <div class="card-body p-4 d-flex align-items-start gap-3">
              <div class="icon-circle flex-shrink-0">
                <img src="/business/hotelería_waschee.webp" alt="Icono Hotelería" class="sector-icon" />
              </div>
              <div class="card-text-content">
                <h4 class="card-title text-uppercase">HOTELERÍA</h4>
                <p class="card-description m-0">
                  Lavado impecable para brindar la mejor experiencia a cada huésped.
                </p>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Card 2: Hospitales -->
        <div class="col-sm-12 col-md-6 col-lg-3 reveal-child">
          <div class="card sector-card h-100">
            <img src="/business/hospitales_card.png" alt="Hospitales" class="card-img-top sector-img" />
            <div class="card-body p-4 d-flex align-items-start gap-3">
              <div class="icon-circle flex-shrink-0">
                <img src="/business/hospitales_waschee.webp" alt="Icono Hospitales" class="sector-icon" />
              </div>
              <div class="card-text-content">
                <h4 class="card-title text-uppercase">HOSPITALES</h4>
                <p class="card-description m-0">
                  Higiene y desinfección con equipos preparados para trabajo continuo.
                </p>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Card 3: Minería -->
        <div class="col-sm-12 col-md-6 col-lg-3 reveal-child">
          <div class="card sector-card h-100">
            <img src="/business/mineria_card.png" alt="Minería" class="card-img-top sector-img" />
            <div class="card-body p-4 d-flex align-items-start gap-3">
              <div class="icon-circle flex-shrink-0">
                <img src="/business/mineria_aschee_2.webp" alt="Icono Minería" class="sector-icon" />
              </div>
              <div class="card-text-content">
                <h4 class="card-title text-uppercase">MINERÍA</h4>
                <p class="card-description m-0">
                  Equipos diseñados para soportar operaciones de alta exigencia.
                </p>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Card 4: Industria -->
        <div class="col-sm-12 col-md-6 col-lg-3 reveal-child">
          <div class="card sector-card h-100">
            <img src="/business/industria_card_waschee.png" alt="Industria" class="card-img-top sector-img" />
            <div class="card-body p-4 d-flex align-items-start gap-3">
              <div class="icon-circle flex-shrink-0">
                <img src="/business/industria_waschee.webp" alt="Icono Industria" class="sector-icon" />
              </div>
              <div class="card-text-content">
                <h4 class="card-title text-uppercase">INDUSTRIA</h4>
                <p class="card-description m-0">
                  Productividad constante para grandes volúmenes de ropa.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectorsComponent'
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800;900&display=swap');

.sectors-section {
  background-color: #f8f9fa; /* Light background as in mockup */
  padding: 80px 0;
  font-family: 'Inter', sans-serif;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

.section-title {
  font-size: clamp(20px, 2.5vw, 28px);
  font-weight: 900;
  color: #001c3d; /* Dark navy blue from reference image */
  letter-spacing: 0.02em;
}

.sector-card {
  border: 1px solid rgba(0, 0, 0, 0.06);
  border-radius: 16px;
  overflow: hidden;
  background-color: #ffffff;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.015);
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
}

.sector-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.05);
  border-color: rgba(0, 0, 0, 0.1);
}

.sector-img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-bottom: 1px solid rgba(0, 0, 0, 0.03);
}



.icon-circle {
  width: 64px;
  height: 64px;
  background-color: #e8eff5; /* Light gray-blue background from mockup */
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.sector-icon {
  width: 32px;
  height: 32px;
  object-fit: contain;
}

.card-title {
  font-size: 17px;
  font-weight: 800;
  color: #001c3d;
  margin-bottom: 6px;
  letter-spacing: 0.02em;
}

.card-description {
  font-size: 14px;
  color: #556275;
  line-height: 1.45;
  font-weight: 500;
}

@media (max-width: 991.98px) {
  .sectors-section {
    padding: 60px 0;
  }
}
</style>
