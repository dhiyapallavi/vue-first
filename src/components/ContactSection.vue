<template>
    <section id="contact" class="contact">
      <div class="container">
        <div class="section-title aos-init" data-aos="fade-up">
          <h2>Contact Us</h2>
        </div>
  
        <div class="row">
          <div class="col-lg-4 col-md-6 aos-init" data-aos="fade-up" data-aos-delay="100">
            <div class="contact-about">
              <h3>Akeshya</h3>
              <p>Designers, developers & marketeers capable of delivering solutions according to your needs,</p>
            </div>
          </div>
  
          <div class="col-lg-3 col-md-6 mt-4 mt-md-0 aos-init" data-aos="fade-up" data-aos-delay="200">
            <div class="info">
              <div>
                <i class="ri-map-pin-line"></i>
                <p>26-2-789, 7th street, Jyothi Nagar, Nellore, Andhra Pradesh 524004</p>
              </div>
  
              <div>
                <i class="ri-mail-send-line"></i>
                <p>info@akeshya.com</p>
              </div>
  
              <div>
                <i class="ri-phone-line"></i>
                <p>+91 94942 40922</p>
              </div>
            </div>
          </div>
  
          <!-- FORM -->
          <div class="col-lg-5 col-md-12 aos-init" data-aos="fade-up" data-aos-delay="300">
            <form @submit.prevent="submitForm" class="php-email-form">
              <div class="form-group">
                <input v-model="formData.name" type="text" class="form-control" id="name" placeholder="Your Name" required />
              </div>
              <div class="form-group">
                <input v-model="formData.email" type="email" class="form-control" id="email" placeholder="Your Email" required />
              </div>
              <div class="form-group">
                <input v-model="formData.subject" type="text" class="form-control" id="subject" placeholder="Subject" required />
              </div>
              <div class="form-group">
                <textarea v-model="formData.message" class="form-control" rows="5" placeholder="Message" required></textarea>
              </div>
              <div class="my-3">
                <div class="loading" v-if="loading">Loading</div>
                <div class="error-message" v-if="errorMessage">{{ errorMessage }}</div>
                <div class="sent-message" v-if="successMessage">{{ successMessage }}</div>
              </div>
              <div class="text-center">
                <button type="submit">Send Message</button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        formData: {
          name: '',
          email: '',
          subject: '',
          message: ''
        },
        loading: false,
        errorMessage: '',
        successMessage: ''
      };
    },
    methods: {
      submitForm() {
        // You can add your form submission logic here
        // For example, you can use Axios to send the form data to your backend
        this.loading = true;
        setTimeout(() => {
          // Simulating form submission
          // Replace this with your actual form submission logic
          this.loading = false;
          if (this.formData.message.length > 50) {
            this.successMessage = 'Your message has been sent. Thank you!';
          } else {
            this.errorMessage = 'Please enter a message with at least 50 characters.';
          }
        }, 2000); 
      }
    }
  };
  </script>
  
  <style scoped>
  
  </style>
  