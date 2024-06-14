<template>
    <section id="features" class="features">
      <div class="container">
        <div class="section-title aos-init" data-aos="fade-up">
          <h2>Our Core Features</h2>
          <p>
            Akeshya is a forward-thinking and intelligent design firm that is
            technically and creatively capable of transforming your brand into
            its best digital self. Our approach to design and development
            results in compelling, engaging branding and immersive digital
            experiences that provide a value for money.
          </p>
        </div>
  
        <div class="row aos-init" data-aos="fade-up" data-aos-delay="300">
          <div
            class="col-lg-3 col-md-4"
            v-for="(feature, index) in coreFeatures"
            :key="index"
          >
            <div class="icon-box">
              <i :class="feature.icon" :style="{ color: feature.color }"></i>
              <h3><a :href="feature.link" style="text-decoration: none;">{{ feature.title }}</a></h3>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'feature-section',
    data() {
      return {
        coreFeatures: [
          { title: 'Web design', icon: 'ri-window-line', color: '#ffbb2c', link: '#' },
          { title: 'Development', icon: 'ri-code-box-line', color: '#5578ff', link: '#' },
          { title: 'Branding', icon: 'ri-creative-commons-by-line', color: '#e80368', link: '#' },
          { title: 'Media buying', icon: 'ri-play-circle-line', color: '#e361ff', link: '#' },
          { title: 'Search engine', icon: 'ri-search-eye-line', color: '#47aeff', link: '#' },
          { title: 'Brand strategy', icon: 'ri-todo-line', color: '#ffa76e', link: '#' },
          { title: 'Local search marketing', icon: 'ri-map-pin-line', color: '#dbce11', link: '#' },
          { title: 'Lead Tracking & Management', icon: 'ri-bar-chart-grouped-line', color: '#4233ff', link: '#' },
          { title: 'Contact management', icon: 'ri-contacts-book-line', color: '#b2904f', link: '#' },
          { title: 'Media management', icon: 'ri-disc-line', color: '#b20969', link: '#' },
          { title: 'Social scheduling', icon: 'ri-calendar-event-line', color: '#ff5828', link: '#' },
          { title: 'Ad retargeting', icon: 'ri-advertisement-fill', color: '#29cc61', link: '#' },
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  </style>
  