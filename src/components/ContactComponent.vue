<template>
  <section class="contact-section" id="cotizar">
    <div class="container">
      <div class="row align-items-center g-5">
        
        <!-- Left Column: Contact Text & Benefits -->
        <div class="col-lg-6 text-col">
          <span class="badge-accent mb-3">CONTACTO</span>
          <h2 class="section-title text-uppercase mb-3">
            ¿LISTO PARA DAR EL <br />
            <span class="highlight-yellow">SIGUIENTE PASO?</span>
          </h2>
          <p class="section-description mb-4">
            Completa el formulario y uno de nuestros expertos en lavandería industrial se comunicará contigo para diseñar una cotización a la medida de tu operación.
          </p>
          
          <!-- Key Points / Benefits -->
          <div class="benefits-list d-flex flex-column gap-3">
            <div class="benefit-item d-flex align-items-start gap-3">
              <div class="benefit-icon-wrapper">
                <i class="fa-solid fa-calculator text-yellow"></i>
              </div>
              <div>
                <h4 class="benefit-title m-0">Cotización Personalizada</h4>
                <p class="benefit-desc m-0">Precios adaptados al volumen y necesidades de tu negocio.</p>
              </div>
            </div>

            <div class="benefit-item d-flex align-items-start gap-3">
              <div class="benefit-icon-wrapper">
                <i class="fa-solid fa-truck-ramp-box text-yellow"></i>
              </div>
              <div>
                <h4 class="benefit-title m-0">Asesoría de Puesta en Marcha</h4>
                <p class="benefit-desc m-0">Te guiamos en la preparación técnica e instalación eléctrica/hidráulica.</p>
              </div>
            </div>

            <div class="benefit-item d-flex align-items-start gap-3">
              <div class="benefit-icon-wrapper">
                <i class="fa-solid fa-shield-halved text-yellow"></i>
              </div>
              <div>
                <h4 class="benefit-title m-0">Respaldo y Garantía Waschée</h4>
                <p class="benefit-desc m-0">Equipos de grado industrial protegidos por hasta 8 años.</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Right Column: Interactive Form -->
        <div class="col-lg-6">
          <div class="form-container-box p-4 p-md-5">
            
            <!-- Success Message Box -->
            <div v-if="isSuccess" class="success-message-box py-5 text-center d-flex flex-column align-items-center justify-content-center gap-3">
              <div class="success-checkmark-pulse mb-2">
                <i class="fa-solid fa-circle-check fa-4x text-yellow"></i>
              </div>
              <h3 class="success-title m-0 text-uppercase">¡Envío Exitoso!</h3>
              <p class="success-desc m-0">
                Tu mensaje ha sido recibido de forma correcta.<br />
                Redirigiéndote a la página de agradecimiento...
              </p>
              <!-- Animated Loading Progress Bar -->
              <div class="progress-bar-container mt-3">
                <div class="progress-bar-fill"></div>
              </div>
            </div>

            <!-- Main Form -->
            <div v-else>
              <h3 class="form-box-title text-center text-uppercase mb-4">Solicitar Cotización</h3>
              
              <form @submit.prevent="handleSubmit" class="contact-form d-flex flex-column gap-3" novalidate>
                <!-- Name Input -->
                <div class="form-group">
                  <label for="name" class="form-label">Nombre Completo *</label>
                  <div class="input-wrapper">
                    <span class="input-icon"><i class="fa-solid fa-user"></i></span>
                    <input 
                      type="text" 
                      id="name" 
                      v-model="form.name" 
                      @blur="validateField('name')"
                      @input="clearError('name')"
                      class="form-control-custom" 
                      :class="{ 'is-invalid-custom': errors.name }"
                      placeholder="Ej. Juan Pérez" 
                      required 
                    />
                  </div>
                  <span v-if="errors.name" class="error-message">{{ errors.name }}</span>
                </div>

                <!-- Phone Input -->
                <div class="form-group">
                  <label for="phone" class="form-label">Teléfono de Contacto *</label>
                  <div class="input-wrapper">
                    <span class="input-icon"><i class="fa-solid fa-phone"></i></span>
                    <input 
                      type="tel" 
                      id="phone" 
                      v-model="form.phone" 
                      @blur="validateField('phone')"
                      @input="clearError('phone')"
                      class="form-control-custom" 
                      :class="{ 'is-invalid-custom': errors.phone }"
                      placeholder="Ej. 55 1234 5678" 
                      required 
                    />
                  </div>
                  <span v-if="errors.phone" class="error-message">{{ errors.phone }}</span>
                </div>

                <!-- Email Input -->
                <div class="form-group">
                  <label for="email" class="form-label">Correo Electrónico *</label>
                  <div class="input-wrapper">
                    <span class="input-icon"><i class="fa-solid fa-envelope"></i></span>
                    <input 
                      type="email" 
                      id="email" 
                      v-model="form.email" 
                      @blur="validateField('email')"
                      @input="clearError('email')"
                      class="form-control-custom" 
                      :class="{ 'is-invalid-custom': errors.email }"
                      placeholder="Ej. juan@correo.com" 
                      required 
                    />
                  </div>
                  <span v-if="errors.email" class="error-message">{{ errors.email }}</span>
                </div>

                <!-- Sector Selection -->
                <div class="form-group">
                  <label for="sector" class="form-label">Giro o Sector *</label>
                  <div class="input-wrapper">
                    <span class="input-icon"><i class="fa-solid fa-hotel"></i></span>
                    <select 
                      id="sector" 
                      v-model="form.sector" 
                      @change="validateField('sector')"
                      class="form-control-custom select-custom" 
                      :class="{ 'is-invalid-custom': errors.sector }"
                      required
                    >
                      <option value="" disabled>Selecciona tu sector</option>
                      <option value="hoteleria">Hotelería / Hospedaje</option>
                      <option value="hospitales">Hospitales / Sector Salud</option>
                      <option value="mineria">Minería / Campamentos</option>
                      <option value="industria">Industria / Maquila</option>
                      <option value="lavanderia">Lavandería Comercial / Autoservicio</option>
                      <option value="otro">Otro Giro</option>
                    </select>
                  </div>
                  <span v-if="errors.sector" class="error-message">{{ errors.sector }}</span>
                </div>

                <!-- Comments Input -->
                <div class="form-group">
                  <label for="message" class="form-label">Mensaje o Comentarios (Opcional)</label>
                  <textarea 
                    id="message" 
                    v-model="form.message" 
                    class="form-control-custom textarea-custom" 
                    rows="3" 
                    placeholder="Cuéntanos más sobre las necesidades de tu operación..."
                  ></textarea>
                </div>

                <!-- Submit Button -->
                <button type="submit" class="btn btn-form-submit w-100 d-flex align-items-center justify-content-center gap-2 mt-2">
                  ENVIAR SOLICITUD
                  <i class="fa-solid fa-paper-plane"></i>
                </button>
              </form>
            </div>

          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactComponent',
  data() {
    return {
      form: {
        name: '',
        phone: '',
        email: '',
        sector: '',
        message: ''
      },
      errors: {
        name: '',
        phone: '',
        email: '',
        sector: ''
      },
      isSuccess: false
    };
  },
  methods: {
    validateField(field) {
      if (field === 'name') {
        if (!this.form.name.trim()) {
          this.errors.name = 'El nombre completo es requerido.';
        } else if (this.form.name.trim().length < 3) {
          this.errors.name = 'El nombre debe tener al menos 3 caracteres.';
        } else {
          this.errors.name = '';
        }
      }

      if (field === 'phone') {
        const cleanPhone = this.form.phone.replace(/[^0-9]/g, '');
        if (!this.form.phone) {
          this.errors.phone = 'El teléfono es requerido.';
        } else if (cleanPhone.length !== 10) {
          this.errors.phone = 'Ingresa un número telefónico válido a 10 dígitos.';
        } else {
          this.errors.phone = '';
        }
      }

      if (field === 'email') {
        const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (!this.form.email) {
          this.errors.email = 'El correo electrónico es requerido.';
        } else if (!emailPattern.test(this.form.email)) {
          this.errors.email = 'Ingresa un correo electrónico válido.';
        } else {
          this.errors.email = '';
        }
      }

      if (field === 'sector') {
        if (!this.form.sector) {
          this.errors.sector = 'Selecciona un giro o sector.';
        } else {
          this.errors.sector = '';
        }
      }
    },
    clearError(field) {
      this.errors[field] = '';
    },
    validateForm() {
      this.validateField('name');
      this.validateField('phone');
      this.validateField('email');
      this.validateField('sector');

      return !this.errors.name && !this.errors.phone && !this.errors.email && !this.errors.sector;
    },
    handleSubmit() {
      if (this.validateForm()) {
        this.isSuccess = true;
        // Wait 3 seconds then redirect to /gracias
        setTimeout(() => {
          window.location.href = '/gracias';
        }, 3000);
      }
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap');

.contact-section {
  background-color: #000c1a;
  color: #ffffff;
  padding: 80px 0;
  font-family: 'Inter', sans-serif;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.text-col {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
}

/* Badge and Title */
.badge-accent {
  background-color: rgba(229, 169, 60, 0.1);
  color: #e5a93c;
  font-weight: 800;
  font-size: 13px;
  letter-spacing: 0.1em;
  padding: 6px 16px;
  border-radius: 6px;
  display: inline-block;
  border: 1px solid rgba(229, 169, 60, 0.25);
}

.section-title {
  font-size: clamp(24px, 3.5vw, 38px);
  font-weight: 900;
  line-height: 1.15;
  color: #ffffff;
}

.highlight-yellow {
  color: #e5a93c;
}

.section-description {
  font-size: 15px;
  color: #c9d1d9;
  line-height: 1.5;
  max-width: 500px;
}

/* Benefits list left column */
.benefit-item {
  max-width: 500px;
}

.benefit-icon-wrapper {
  width: 42px;
  height: 42px;
  background-color: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
  flex-shrink: 0;
}

.text-yellow {
  color: #e5a93c;
}

.benefit-title {
  font-size: 15px;
  font-weight: 700;
  color: #ffffff;
  margin-bottom: 2px;
}

.benefit-desc {
  font-size: 13px;
  color: #8b9bb4;
  line-height: 1.4;
}

/* Form Container Box */
.form-container-box {
  background: rgba(3, 20, 42, 0.45);
  border: 1px solid rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(16px);
  border-radius: 20px;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.25);
  min-height: 490px; /* Keep height stable during success state transitions */
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.form-box-title {
  font-size: 20px;
  font-weight: 800;
  color: #ffffff;
  letter-spacing: 0.02em;
}

/* Form inputs & styles */
.form-group {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.form-label {
  font-size: 12px;
  font-weight: 700;
  color: #a5b4fc;
  letter-spacing: 0.02em;
  text-transform: uppercase;
  margin: 0;
}

.input-wrapper {
  position: relative;
  width: 100%;
}

.input-icon {
  position: absolute;
  left: 14px;
  top: 50%;
  transform: translateY(-50%);
  color: rgba(255, 255, 255, 0.35);
  font-size: 14px;
  pointer-events: none;
  display: flex;
  align-items: center;
}

.form-control-custom {
  width: 100%;
  padding: 12px 16px 12px 42px;
  background-color: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  color: #ffffff;
  font-size: 14.5px;
  font-family: inherit;
  transition: all 0.3s ease;
}

.form-control-custom:focus {
  outline: none;
  border-color: #e5a93c;
  background-color: rgba(255, 255, 255, 0.06);
  box-shadow: 0 0 10px rgba(229, 169, 60, 0.15);
}

/* Custom error highlight styles */
.form-control-custom.is-invalid-custom {
  border-color: #ef4444 !important;
  background-color: rgba(239, 68, 68, 0.03);
  box-shadow: 0 0 10px rgba(239, 68, 68, 0.15) !important;
}

.error-message {
  color: #ef4444;
  font-size: 11px;
  font-weight: 600;
  margin-top: 2px;
  letter-spacing: 0.01em;
}

/* Select element customization */
.select-custom {
  appearance: none;
  cursor: pointer;
}

.select-custom option {
  background-color: #03142a;
  color: #ffffff;
}

.textarea-custom {
  padding-left: 16px;
}

/* Submit Button */
.btn-form-submit {
  background-color: #e5a93c;
  color: #000c1a;
  font-weight: 800;
  font-size: 14px;
  letter-spacing: 0.05em;
  border-radius: 10px;
  padding: 14px 0;
  border: none;
  box-shadow: 0 4px 15px rgba(229, 169, 60, 0.2);
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  cursor: pointer;
}

.btn-form-submit:hover {
  background-color: #f0b84c;
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(229, 169, 60, 0.35);
}

.btn-form-submit:active {
  transform: translateY(0);
}

/* Success State Styles */
.success-message-box {
  animation: fadeIn 0.4s ease forwards;
}

.success-checkmark-pulse {
  animation: bounceScale 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
}

.success-title {
  font-size: 24px;
  font-weight: 900;
  color: #ffffff;
}

.success-desc {
  font-size: 14px;
  color: #c9d1d9;
  line-height: 1.5;
}

/* 3-second animated progress bar */
.progress-bar-container {
  width: 100%;
  max-width: 280px;
  height: 4px;
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 2px;
  overflow: hidden;
}

.progress-bar-fill {
  width: 0%;
  height: 100%;
  background-color: #e5a93c;
  animation: loadProgress 3s linear forwards;
}

/* Animations */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes bounceScale {
  0% {
    transform: scale(0.3);
    opacity: 0;
  }
  50% {
    transform: scale(1.1);
  }
  70% {
    transform: scale(0.9);
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}

@keyframes loadProgress {
  0% {
    width: 0%;
  }
  100% {
    width: 100%;
  }
}

/* Responsive media queries */
@media (max-width: 991.98px) {
  .contact-section {
    padding: 60px 0;
  }
  
  .text-col {
    align-items: center;
    text-align: center;
  }
  
  .section-description {
    max-width: 100%;
  }
  
  .benefit-item {
    text-align: left;
  }
}
</style>
