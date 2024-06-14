<template>
    <section id="more-services" class="more-services">
      <div class="container">
        <div class="section-title aos-init" data-aos="fade-up">
          <h2>Our Process</h2>
          <p>
            Over the years we’ve evolved a tested method for attaining
            achievement for each one of our clients.
          </p>
        </div>
  
        <div class="row">
          <div
            class="col-md-6 d-flex align-items-stretch"
            v-for="(service, index) in services"
            :key="index"
          >
            <div
              class="card aos-init"
              :style="{ backgroundImage: `url(${service.image})` }"
              :data-aos="service.aos"
              :data-aos-delay="service.delay"
            >
              <div class="card-body">
                <h5 class="card-title"><a :href="service.link" style="text-decoration: none;">{{ service.title }}</a></h5>
                <p class="card-text">{{ service.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'more-services',
    data() {
      return {
        services: [
          {
            title: 'Planning',
            image: 'assets/img/more-services-1.jpg',
            description: 'We help you turn all of your ideas into a digital product that meets all of your requirements. We begin each project by determining its scope and needs. This is done by collaborating closely with you to ensure that we\'re all on the same page.',
            link: '#',
            aos: 'fade-up',
            delay: 100
          },
          {
            title: 'Design',
            image: 'assets/img/more-services-2.jpg',
            description: 'We build our websites carefully through a series of workshops, wire-framing, and user experience (UX) sessions, resulting in a site that reinforces trust, conveys important brand messaging, and provides a return on innovation.',
            link: '#',
            aos: 'fade-up',
            delay: 200
          },
          {
            title: 'Development',
            image: 'assets/img/more-services-3.jpg',
            description: 'We provide extensive front-end and back-end development that allows your idea to stand alone. Our in-house developers work side-by-side with the artistic team to seek out natural breakpoints inside the content and order practicality based on acknowledged statistics.',
            link: '#',
            aos: 'fade-up',
            delay: 100
          },
          {
            title: 'Marketing',
            image: 'assets/img/more-services-4.jpg',
            description: 'We come up with ideas and campaigns to help your business prosper online. Our campaigns and virtual approach have a verified tune report of accomplishing brilliant results, gathering new leads and site visitors in your website and assist them convert.',
            link: '#',
            aos: 'fade-up',
            delay: 200
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
 
  </style>
  