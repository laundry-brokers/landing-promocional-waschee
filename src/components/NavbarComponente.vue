<template>
  <nav class="navbar navbar-expand-lg navbar-dark custom-navbar py-3">
    <div class="container-fluid px-lg-5">
      <!-- Logo -->
      <a class="navbar-brand d-flex align-items-center" href="/">
        <img src="/logos/Logo_Laundrybrokers.png" alt="Waschée" class="logo-img" style="width: 300px; height: auto;" />
      </a>
      
      <!-- Hamburger Button (Mobile) -->
      <button 
        class="navbar-toggler border-0" 
        type="button" 
        @click="toggleMenu"
        aria-controls="navbarNav" 
        :aria-expanded="isMenuOpen" 
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      
      <!-- Navbar Links & CTA -->
      <div 
        class="collapse navbar-collapse" 
        :class="{ 'show': isMenuOpen }" 
        id="navbarNav"
      >
        <ul class="navbar-nav mx-auto mb-2 mb-lg-0 text-center gap-1 gap-lg-4">
          <li class="nav-item">
            <a class="nav-link nav-text" href="/" @click="closeMenu">INICIO</a>
          </li>
          <li class="nav-item">
            <a class="nav-link nav-text" href="https://waschee.com/mx/catalogo" target="_blank" @click="closeMenu">EQUIPOS</a>
          </li>
          <li class="nav-item">
            <a class="nav-link nav-text" href="#cotizar" @click="closeMenu">CONTACTO</a>
          </li>
        </ul>
        
        <!-- CTA Button -->
        <div class="d-flex justify-content-center align-items-center">
          <a href="#cotizar" @click="closeMenu" class="btn btn-cta d-flex align-items-center gap-2 justify-content-center">
            COTIZAR AHORA
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-right" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z"/>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavbarComponente',
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu() {
      this.isMenuOpen = false;
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap');

.custom-navbar {
  background-color: #000c1a; /* Navy dark blue matching the reference image */
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  font-family: 'Inter', sans-serif;
  z-index: 1030;
}

.logo-img {
  height: 48px;
  width: auto;
  object-fit: contain;
}

.nav-text {
  color: #e0e5eb !important;
  font-weight: 700;
  font-size: 13px;
  letter-spacing: 0.08em;
  transition: color 0.25s ease;
  padding: 8px 12px;
}

.nav-text:hover,
.nav-text:focus {
  color: #ffffff !important;
}

.btn-cta {
  background-color: #e5a93c; /* Golden yellow matching reference */
  color: #000c1a;
  font-weight: 800;
  font-size: 13px;
  letter-spacing: 0.08em;
  border-radius: 12px;
  padding: 12px 28px;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  border: none;
}

.btn-cta:hover {
  background-color: #f0b84c;
  color: #000c1a;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(229, 169, 60, 0.35);
}

.btn-cta:active {
  transform: translateY(0);
}

/* Custom hamburger menu styling */
.navbar-toggler {
  outline: none;
  box-shadow: none !important;
}

@media (max-width: 991.98px) {
  .navbar-collapse {
    background-color: #000c1a;
    padding: 16px 8px 16px 8px;
    border-radius: 12px;
    margin-top: 10px;
    border: 1px solid rgba(255, 255, 255, 0.05);
  }
  
  .nav-text {
    padding: 10px 0;
    font-size: 13.5px;
    border-bottom: 1px solid rgba(255, 255, 255, 0.04);
  }

  .nav-item:last-child .nav-text {
    border-bottom: none;
  }
  
  .btn-cta {
    margin-top: 14px;
    width: 100%;
    max-width: 320px;
  }
}
</style>
