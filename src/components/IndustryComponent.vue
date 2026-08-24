<template>
  <section class="industry-section">
    <div class="container py-4">
      <div class="row align-items-center">
        <!-- Content Column (Left Side) -->
        <div class="col-lg-6 text-center text-lg-start d-flex flex-column gap-4 py-lg-4">
          <!-- Heading -->
          <div class="heading-container">
            <h2 class="section-title m-0">
              LA POTENCIA<br />
              <span class="text-blue">INDUSTRIAL</span><br />
              QUE TU OPERACIÓN<br />
              <span class="text-dark-blue">NECESITA</span>
            </h2>
          </div>
          
          <!-- Description -->
          <p class="section-desc mb-0">
            Equipos de lavandería diseñados para operar todos los días, con máxima eficiencia, menor costo operativo y hasta 8 años de garantía.
          </p>
          
          <!-- CTA Button -->
          <div class="cta-container d-flex justify-content-center justify-content-lg-start">
            <a href="#cotizar" class="btn btn-industry-cta d-flex align-items-center gap-2 justify-content-center">
              SOLICITAR ASESORÍA
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-right" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z"/>
              </svg>
            </a>
          </div>
          
          <!-- Experience Badge -->
          <div class="badge-experience d-flex align-items-center justify-content-center justify-content-lg-start mt-2">
            <img src="/industrial/mas_de_treinta_anios.webp" alt="MÁS DE 30 AÑOS DE EXPERIENCIA RESPALDAN NUESTRA INGENIERÍA" class="badge-img" />
          </div>
        </div>
        
        <!-- Empty Column (Right Side) to let the background machines be visible on desktop -->
        <div class="col-lg-6 d-none d-lg-block spacer-column"></div>
        
        <!-- Mobile Image Column (Only visible on mobile/tablet) -->
        <div class="col-lg-6 d-block d-lg-none mt-4 text-center">
          <img src="/industrial/background_waschee_dos.webp" alt="Equipos Industriales Waschée" class="img-fluid mobile-industry-img" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'IndustryComponent'
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800;900&display=swap');

.industry-section {
  position: relative;
  background-image: url('/industrial/background_waschee_dos.webp');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-color: #f2f4f7; /* Off-white fallback to match background_waschee_dos.webp */
  font-family: 'Inter', sans-serif;
  min-height: 520px;
  display: flex;
  align-items: center;
  padding: 40px 0;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

/* Typography styling */
.section-title {
  font-size: clamp(34px, 4vw, 48px);
  font-weight: 900;
  line-height: 1.05;
  color: #001229;
  letter-spacing: -0.010em;
}

.text-blue {
  color: #2b70b2; /* Royal blue matching the mockup color */
}

.text-dark-blue {
  color: #001229;
}

.section-desc {
  font-size: clamp(15px, 1.2vw, 16px);
  color: #4a5568;
  line-height: 1.5;
  max-width: 480px;
}

/* CTA Button */
.btn-industry-cta {
  background-color: #001229; /* Dark navy matching the brand theme */
  color: #ffffff !important; /* Force text color to stay white */
  font-weight: 800;
  font-size: 14px;
  letter-spacing: 0.05em;
  border-radius: 12px;
  padding: 15px 36px;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  border: none;
  width: auto;
  text-decoration: none;
}

.btn-industry-cta svg {
  transition: transform 0.3s ease;
  fill: #ffffff;
}

.btn-industry-cta:hover {
  background-color: #0c2545;
  color: #ffffff !important; /* Ensure it stays white on hover */
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0, 18, 41, 0.25);
}

.btn-industry-cta:hover svg {
  transform: translateX(4px); /* Micro-animation: slide arrow right */
}

.btn-industry-cta:active {
  transform: translateY(0);
}

/* Experience Badge */
.badge-img {
  height: 52px;
  width: auto;
  object-fit: contain;
}

/* Mobile responsive */
@media (max-width: 991.98px) {
  .industry-section {
    background-image: none;
    background-color: #f2f4f7;
    padding: 45px 0;
    text-align: center;
  }

  .section-title {
    font-size: clamp(26px, 6vw, 38px);
  }
  
  .section-desc {
    max-width: 100%;
    margin-left: auto;
    margin-right: auto;
    font-size: 14.5px;
  }

  .btn-industry-cta {
    width: 100%;
    max-width: 340px;
  }
  
  .mobile-industry-img {
    width: 100%;
    max-width: 600px;
    height: 260px;
    object-fit: cover;
    object-position: 70% center;
    border-radius: 14px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
    margin: 0 auto;
    display: block;
  }
}

@media (max-width: 575.98px) {
  .industry-section {
    padding: 35px 0;
  }

  .mobile-industry-img {
    height: 200px;
    border-radius: 10px;
  }

  .badge-img {
    height: 42px;
  }
}
</style>
