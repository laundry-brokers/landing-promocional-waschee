<template>
  <div>
    <!-- Scroll to Top Button (Left Side) -->
    <button 
      @click="scrollToTop" 
      :class="['scroll-to-top-btn', { 'is-visible': showScrollTop }]"
      aria-label="Ir arriba"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="18 15 12 9 6 15"></polyline>
      </svg>
    </button>

    <!-- Floating WhatsApp Button (Right Side) -->
    <a 
      :href="whatsappUrl" 
      target="_blank" 
      rel="noopener noreferrer" 
      class="whatsapp-float-btn"
      aria-label="Contactar por WhatsApp"
    >
      <i class="fa-brands fa-whatsapp"></i>
    </a>
  </div>
</template>

<script>
import { ref, onMounted, onBeforeUnmount } from 'vue';

export default {
  name: 'FloatingWidgets',
  setup() {
    const showScrollTop = ref(false);
    // WhatsApp number configuration: (55) 5059-0039 -> Mexico code 52 -> 525550590039
    const phoneNumber = '525550590039'; 
    const defaultMessage = 'Hola, me interesa obtener información sobre los equipos industriales Wäschee.';
    const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(defaultMessage)}`;

    const handleScroll = () => {
      showScrollTop.value = window.scrollY > 300;
    };

    const scrollToTop = () => {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    };

    onMounted(() => {
      window.addEventListener('scroll', handleScroll);
    });

    onBeforeUnmount(() => {
      window.removeEventListener('scroll', handleScroll);
    });

    return {
      showScrollTop,
      whatsappUrl,
      scrollToTop
    };
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap');

/* Botón Ir Arriba (Costado Izquierdo) */
.scroll-to-top-btn {
  position: fixed;
  bottom: 30px;
  left: 30px;
  width: 55px;
  height: 55px;
  border-radius: 50%;
  background-color: #000c1a;
  color: #e5a93c;
  border: 2px solid #e5a93c;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  z-index: 999;
  box-shadow: 0 4px 15px rgba(229, 169, 60, 0.3);
  font-family: 'Inter', sans-serif;
  
  /* Animación CSS pura */
  opacity: 0;
  visibility: hidden;
  transform: translateY(15px) scale(0.8);
  transition: opacity 0.3s ease, transform 0.3s ease, background-color 0.3s ease, color 0.3s ease, box-shadow 0.3s ease;
}

.scroll-to-top-btn.is-visible {
  opacity: 1;
  visibility: visible;
  transform: translateY(0) scale(1);
}

.scroll-to-top-btn:hover {
  background-color: #e5a93c;
  color: #000c1a;
  transform: translateY(-5px) scale(1);
  box-shadow: 0 6px 20px rgba(229, 169, 60, 0.5);
}

/* Botón Flotante de WhatsApp (Costado Derecho) */
.whatsapp-float-btn {
  position: fixed;
  bottom: 30px;
  right: 30px;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: #25D366;
  color: #ffffff;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  z-index: 999;
  box-shadow: 0 4px 15px rgba(37, 211, 102, 0.4);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  text-decoration: none;
}

.whatsapp-float-btn:hover {
  background-color: #20ba5a;
  transform: translateY(-5px) scale(1.05);
  box-shadow: 0 6px 22px rgba(37, 211, 102, 0.6);
  color: #ffffff;
}

.whatsapp-float-btn i {
  font-size: 34px;
  line-height: 1;
  transition: transform 0.3s ease;
}

.whatsapp-float-btn:hover i {
  transform: scale(1.1);
}

/* Adaptación para pantallas móviles */
@media (max-width: 767.98px) {
  .scroll-to-top-btn {
    bottom: 20px;
    left: 20px;
    width: 48px;
    height: 48px;
  }
  
  .whatsapp-float-btn {
    bottom: 20px;
    right: 20px;
    width: 52px;
    height: 52px;
  }
  
  .whatsapp-float-btn i {
    font-size: 28px;
  }
}
</style>
