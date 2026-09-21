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
                <h4 class="benefit-title m-0">Respaldo y Garantía Waschee</h4>
                <p class="benefit-desc m-0">Equipos de grado industrial protegidos por hasta 8 años.</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Right Column: Bitrix24 Form Container -->
        <div class="col-lg-6">
          <div class="form-container-box p-3 p-sm-4 p-md-5">
            <!-- Form Title -->
            <h3 class="form-box-title text-center text-uppercase mb-4">Solicitar Cotización</h3>
            
            <div ref="b24Container" class="b24-wrapper w-100">
              <!-- Bitrix24 Script is dynamically injected here -->
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
  mounted() {
    if (this.$refs.b24Container) {
      // Prevent duplicate script execution
      const existingScript = this.$refs.b24Container.querySelector('script[data-b24-form="inline/22/ofcvp8"]');
      if (!existingScript) {
        const script = document.createElement('script');
        script.setAttribute('data-b24-form', 'inline/22/ofcvp8');
        script.setAttribute('data-skip-moving', 'true');
        script.innerHTML = `(function(w,d,u){var s=d.createElement('script');s.async=true;s.src=u+'?'+(Date.now()/180000|0);var h=d.getElementsByTagName('script')[0];h.parentNode.insertBefore(s,h);})(window,document,'https://cdn.bitrix24.mx/b36033689/crm/form/loader_22.js');`;
        this.$refs.b24Container.appendChild(script);
      }

      // Continuous DOM reinforcement to ensure 100% width on every Bitrix container
      const enforceFullWidth = () => {
        if (!this.$refs.b24Container) return;
        const allElements = this.$refs.b24Container.querySelectorAll('div, form, fieldset, [class*="b24-"]');
        allElements.forEach((el) => {
          if (!el.classList.contains('b24-form-btn-text') && !el.classList.contains('b24-form-sign')) {
            el.style.setProperty('width', '100%', 'important');
            el.style.setProperty('max-width', '100%', 'important');
            el.style.setProperty('min-width', '100%', 'important');
            el.style.setProperty('box-sizing', 'border-box', 'important');
          }
        });
      };

      const observer = new MutationObserver(enforceFullWidth);
      observer.observe(this.$refs.b24Container, { childList: true, subtree: true, attributes: true });

      const intervalId = setInterval(enforceFullWidth, 250);
      setTimeout(() => clearInterval(intervalId), 15000);
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap');

.contact-section {
  background-color: #000c1a;
  color: #ffffff;
  padding: 70px 0;
  font-family: 'Inter', sans-serif;
  position: relative;
  overflow: hidden;
}

/* Subtle background radial glow */
.contact-section::before {
  content: "";
  position: absolute;
  top: 50%;
  right: -10%;
  width: 500px;
  height: 500px;
  background: radial-gradient(circle, rgba(229, 169, 60, 0.04) 0%, rgba(0, 12, 26, 0) 70%);
  transform: translateY(-50%);
  pointer-events: none;
}

/* Badge accent */
.badge-accent {
  display: inline-block;
  background-color: rgba(229, 169, 60, 0.12);
  color: #e5a93c;
  font-weight: 800;
  font-size: 13px;
  letter-spacing: 0.1em;
  padding: 6px 14px;
  border-radius: 6px;
  border-left: 3px solid #e5a93c;
  text-transform: uppercase;
}

.section-title {
  font-size: clamp(26px, 3.2vw, 42px);
  font-weight: 900;
  letter-spacing: -0.01em;
  line-height: 1.15;
  color: #ffffff;
}

.highlight-yellow {
  color: #e5a93c;
}

.section-description {
  font-size: clamp(14px, 1.2vw, 16px);
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
  -webkit-backdrop-filter: blur(16px);
  border-radius: 20px;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.25);
  min-height: 490px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;
  width: 100%;
}

.form-box-title {
  font-size: 22px;
  font-weight: 900;
  color: #ffffff;
  letter-spacing: 0.02em;
}

/* Responsive media queries */
@media (max-width: 991.98px) {
  .contact-section {
    padding: 50px 0;
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

@media (max-width: 575.98px) {
  .contact-section {
    padding: 35px 0;
  }

  .form-container-box {
    border-radius: 16px;
    padding: 20px 14px !important;
    min-height: auto;
  }
}
</style>

<!-- Pixel-Perfect 100% Full Width Bitrix24 Form Overrides -->
<style>
/* 1. Force 100% Width on all containers, rows, columns */
.form-container-box div,
.form-container-box form,
.form-container-box fieldset,
.form-container-box .b24-wrapper,
.form-container-box .b24-form,
.form-container-box .b24-form-wrapper,
.form-container-box .b24-form-fields,
.form-container-box .b24-form-row,
.form-container-box .b24-form-col,
.form-container-box [class*="b24-form-col"],
.form-container-box [class*="b24-form-row"],
.form-container-box .b24-form-field,
.form-container-box [class*="b24-form-field"],
.form-container-box .b24-form-control-container,
.form-container-box .b24-form-control-wrapper,
.form-container-box .b24-form-control,
.form-container-box [class*="b24-form-control"] {
  width: 100% !important;
  max-width: 100% !important;
  min-width: 100% !important;
  flex: 1 1 100% !important;
  box-sizing: border-box !important;
}

.form-container-box .b24-form,
.form-container-box .b24-form-wrapper {
  background: transparent !important;
  color: #ffffff !important;
  font-family: 'Inter', sans-serif !important;
  padding: 0 !important;
  margin: 0 !important;
  border: none !important;
  box-shadow: none !important;
}

.form-container-box .b24-form-row,
.form-container-box .b24-form-col,
.form-container-box [class*="b24-form-col"],
.form-container-box [class*="b24-form-row"] {
  display: block !important;
  margin: 0 !important;
  padding: 0 !important;
}

/* 2. Hide unwanted language selector ("la"), translate widgets, and floating overlays */
.form-container-box select,
.form-container-box .b24-form-control-select,
.form-container-box .b24-form-field-select,
.form-container-box [class*="language"],
.form-container-box [class*="lang-select"],
.form-container-box [class*="goog-"],
.form-container-box img[src*="google"],
.form-container-box .VIpgJd-ZVi9od-ORHb-OEVmcd,
.form-container-box .b24-form-fields .b24-form-sign,
.form-container-box .b24-form-field [class*="abuse"],
.form-container-box .b24-form-fields [class*="abuse"] {
  display: none !important;
  visibility: hidden !important;
  height: 0 !important;
  width: 0 !important;
  margin: 0 !important;
  padding: 0 !important;
  opacity: 0 !important;
  pointer-events: none !important;
}

/* 3. Field Row: 100% Width */
.form-container-box .b24-form-field {
  background: transparent !important;
  border: none !important;
  box-shadow: none !important;
  margin-bottom: 14px !important;
  padding: 0 !important;
  width: 100% !important;
  max-width: 100% !important;
  min-width: 100% !important;
  box-sizing: border-box !important;
  position: relative !important;
  display: block !important;
}

/* 4. Unified Input Box with Labels INSIDE at the top: 100% Width */
.form-container-box .b24-form-control-container,
.form-container-box .b24-form-control-wrapper {
  display: flex !important;
  flex-direction: column !important;
  justify-content: center !important;
  position: relative !important;
  background-color: rgba(255, 255, 255, 0.06) !important;
  border: 1px solid rgba(255, 255, 255, 0.18) !important;
  border-radius: 10px !important;
  padding: 8px 16px 7px 16px !important;
  min-height: 58px !important;
  width: 100% !important;
  max-width: 100% !important;
  min-width: 100% !important;
  box-sizing: border-box !important;
  transition: all 0.25s ease !important;
  box-shadow: none !important;
}

/* Focused Box */
.form-container-box .b24-form-control-container:focus-within,
.form-container-box .b24-form-control-wrapper:focus-within {
  background-color: rgba(255, 255, 255, 0.1) !important;
  border-color: #e5a93c !important;
  box-shadow: 0 0 12px rgba(229, 169, 60, 0.25) !important;
}

/* Mensaje Textarea Box */
.form-container-box .b24-form-field:has(textarea) .b24-form-control-container,
.form-container-box .b24-form-control-container:has(textarea) {
  min-height: 96px !important;
  justify-content: flex-start !important;
  padding-top: 10px !important;
}

/* 5. Labels INSIDE the input box */
.form-container-box .b24-form-control-label,
.form-container-box .b24-form-field-label,
.form-container-box label {
  order: 1 !important;
  color: rgba(255, 255, 255, 0.75) !important;
  font-size: 11px !important;
  font-weight: 700 !important;
  letter-spacing: 0.05em !important;
  text-transform: uppercase !important;
  margin: 0 0 3px 0 !important;
  padding: 0 !important;
  display: flex !important;
  align-items: center !important;
  gap: 4px !important;
  position: static !important;
  transform: none !important;
  background: transparent !important;
  border: none !important;
  box-shadow: none !important;
  opacity: 1 !important;
  pointer-events: none !important;
  line-height: 1.1 !important;
  width: 100% !important;
}

/* Required Asterisk */
.form-container-box .b24-form-field-label-required,
.form-container-box label span,
.form-container-box label span[style*="color"] {
  color: #e5a93c !important;
  font-weight: 900 !important;
  display: inline !important;
}

/* 6. Inner Input Area */
.form-container-box .b24-form-control,
.form-container-box .b24-form-control-string,
.form-container-box .b24-form-control-phone,
.form-container-box .b24-form-control-email,
.form-container-box .b24-form-control-text {
  order: 2 !important;
  background: transparent !important;
  border: none !important;
  box-shadow: none !important;
  padding: 0 !important;
  margin: 0 !important;
  height: auto !important;
  min-height: auto !important;
  display: flex !important;
  align-items: center !important;
  width: 100% !important;
  max-width: 100% !important;
}

/* Raw Inputs / Textareas */
.form-container-box input,
.form-container-box textarea,
.form-container-box .b24-form-control input,
.form-container-box .b24-form-control textarea {
  background: transparent !important;
  border: none !important;
  outline: none !important;
  box-shadow: none !important;
  color: #ffffff !important;
  font-size: 14.5px !important;
  font-weight: 500 !important;
  padding: 0 !important;
  margin: 0 !important;
  width: 100% !important;
  max-width: 100% !important;
  box-sizing: border-box !important;
  font-family: inherit !important;
  line-height: 1.3 !important;
}

.form-container-box textarea,
.form-container-box .b24-form-control textarea {
  min-height: 50px !important;
  resize: vertical !important;
}

.form-container-box input::placeholder,
.form-container-box textarea::placeholder {
  color: rgba(255, 255, 255, 0.35) !important;
  font-size: 13.5px !important;
}

/* 7. Phone Prefix / Code (+52) */
.form-container-box .b24-form-control-phone {
  display: flex !important;
  align-items: center !important;
  gap: 8px !important;
  width: 100% !important;
}

.form-container-box .b24-form-control-phone span,
.form-container-box [class*="phone"] span {
  color: #ffffff !important;
  font-weight: 600 !important;
  font-size: 14.5px !important;
}

/* 8. Subtitle / Hint ("Código del país + número a 10 dígitos") - High contrast visible */
.form-container-box .b24-form-field-description,
.form-container-box .b24-form-field-hint,
.form-container-box .b24-form-control-comment,
.form-container-box [class*="description"],
.form-container-box [class*="hint"],
.form-container-box [class*="comment"],
.form-container-box .b24-form-field small {
  color: #e2e8f0 !important;
  font-size: 12px !important;
  font-weight: 500 !important;
  margin-top: 6px !important;
  margin-left: 2px !important;
  padding: 0 !important;
  display: block !important;
  background: transparent !important;
  border: none !important;
  opacity: 0.95 !important;
}

/* 9. Errors & Alerts */
.form-container-box .b24-form-field-alert {
  color: #f87171 !important;
  font-size: 11.5px !important;
  margin-top: 5px !important;
  margin-left: 2px !important;
  font-weight: 500 !important;
  background: transparent !important;
  border: none !important;
}

/* 10. Button (100% Width, Solid, Centered text) */
.form-container-box .b24-form-btn-container,
.form-container-box .b24-form-btn-block {
  width: 100% !important;
  max-width: 100% !important;
  min-width: 100% !important;
  display: block !important;
  margin-top: 20px !important;
  padding: 0 !important;
  background: transparent !important;
  border: none !important;
}

.form-container-box button.b24-form-btn,
.form-container-box button[type="submit"] {
  background-color: #e5a93c !important;
  color: #000c1a !important;
  font-weight: 900 !important;
  font-size: 15px !important;
  letter-spacing: 0.06em !important;
  text-transform: uppercase !important;
  border-radius: 10px !important;
  padding: 14px 20px !important;
  height: 48px !important;
  min-height: 48px !important;
  width: 100% !important;
  max-width: 100% !important;
  min-width: 100% !important;
  border: none !important;
  box-shadow: 0 4px 15px rgba(229, 169, 60, 0.25) !important;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1) !important;
  cursor: pointer !important;
  display: flex !important;
  align-items: center !important;
  justify-content: center !important;
  text-align: center !important;
  white-space: nowrap !important;
  box-sizing: border-box !important;
}

.form-container-box button.b24-form-btn:hover,
.form-container-box button[type="submit"]:hover {
  background-color: #f0b84c !important;
  transform: translateY(-2px) !important;
  box-shadow: 0 8px 25px rgba(229, 169, 60, 0.4) !important;
  color: #000c1a !important;
}

.form-container-box button.b24-form-btn *,
.form-container-box button[type="submit"] * {
  background: transparent !important;
  border: none !important;
  box-shadow: none !important;
  padding: 0 !important;
  margin: 0 !important;
  color: #000c1a !important;
  font-weight: 900 !important;
  font-size: 15px !important;
  letter-spacing: 0.06em !important;
  text-transform: uppercase !important;
  white-space: nowrap !important;
  display: inline-block !important;
  width: 100% !important;
  text-align: center !important;
  line-height: 1 !important;
}

/* 11. High-Contrast Abuse Link ("Reportar un abuso") at the very bottom */
.form-container-box .b24-wrapper > .b24-form-sign,
.form-container-box .b24-form-wrapper > .b24-form-sign,
.form-container-box .b24-form-wrapper > a[href*="abuse"],
.form-container-box .b24-form-sign,
.form-container-box a[href*="abuse"] {
  color: #9cb1c9 !important;
  font-size: 12px !important;
  font-weight: 500 !important;
  text-align: center !important;
  display: flex !important;
  align-items: center !important;
  justify-content: center !important;
  gap: 6px !important;
  margin-top: 14px !important;
  text-decoration: none !important;
  background: transparent !important;
  border: none !important;
  opacity: 0.85 !important;
  transition: all 0.3s ease !important;
}

.form-container-box a[href*="abuse"]:hover,
.form-container-box .b24-form-sign:hover {
  color: #e5a93c !important;
  opacity: 1 !important;
}
</style>
