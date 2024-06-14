<template>
  <header id="header" class="fixed-top d-flex align-items-center">
    <div class="container d-flex align-items-center justify-content-between">
      <div class="logo">
        <h1>
          <a href="/">
            <img src="assets/img/logo.png" alt="Akeshya Logo" class="img-fluid" />
            AKESHYA
          </a>
        </h1>
      </div>
      <nav :class="['navbar', { 'navbar-mobile': isNavbarMobile }]" id="navbar">
        <ul>
          <li><a class="nav-link scrollto active" href="#hero" @click="scrollToSection('#hero')">Home</a></li>
          <li><a class="nav-link scrollto" href="#about" @click="scrollToSection('#about')">About</a></li>
          <li><a class="nav-link scrollto" href="#services" @click="scrollToSection('#services')">Services</a></li>
          <li><a class="getstarted scrollto" href="#contact" @click="scrollToSection('#contact')">Contact us</a></li>
        </ul>
        <i class="bi mobile-nav-toggle" :class="navToggleClass" @click="toggleMobileNav"></i>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      isNavbarMobile: false
    };
  },
  computed: {
    navToggleClass() {
      return this.isNavbarMobile ? 'bi-x' : 'bi-list';
    }
  },
  methods: {
    toggleMobileNav() {
      this.isNavbarMobile = !this.isNavbarMobile;
    },
    scrollToSection(hash) {
      const element = document.querySelector(hash);
      if (element) {
        const header = document.querySelector('#header');
        const offset = header.offsetHeight;
        const elementPos = element.offsetTop;
        window.scrollTo({
          top: elementPos - offset,
          behavior: 'smooth'
        });
        this.isNavbarMobile = false;
      }
    },
    onScroll() {
      const position = window.scrollY + 200;
      const links = document.querySelectorAll('#navbar .scrollto');
      links.forEach(link => {
        const section = document.querySelector(link.hash);
        if (!section) return;
        if (position >= section.offsetTop && position <= (section.offsetTop + section.offsetHeight)) {
          link.classList.add('active');
        } else {
          link.classList.remove('active');
        }
      });
    }
  },
  mounted() {
    window.addEventListener('scroll', this.onScroll);
    this.onScroll(); // Initial check
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.onScroll);
  }
};
</script>

<style scoped>

</style>
