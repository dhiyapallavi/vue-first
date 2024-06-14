<template>
  <section id="clients" class="clients clients">
    <div class="container">
      <div class="row">
        <div
          v-for="(client, index) in clients"
          :key="client.id"
          class="col-lg-2 col-md-4 col-6"
        >
          <img
            :src="client.src"
            class="img-fluid aos-init aos-animate"
            alt=""
            data-aos="zoom-in"
            :data-aos-delay="index * 100"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      clients: [
        { id: 1, src: 'assets/img/clients/client-1.png' },
        { id: 2, src: 'assets/img/clients/client-2.png' },
        { id: 3, src: 'assets/img/clients/client-3.png' },
        { id: 4, src: 'assets/img/clients/client-4.png' },
        { id: 5, src: 'assets/img/clients/client-5.png' },
        { id: 6, src: 'assets/img/clients/client-6.png' },
      ],
    };
  },
  mounted() {
    // AOS initialization code can be added here if required
    // AOS.init();
  },
};
</script>

<style scoped>
/* Add your component-specific styles here */
</style>
