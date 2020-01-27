<template>
  <Layout>

    <Hero/>
    
    <div class="my-container">
      <p>Medicina integral a tu casa en cualquier momento, con los mejores tratamientos y atención médica</p>
    </div>

  </Layout>
</template>

<script>
import Hero from '~/components/Hero.vue'
export default {
  components: { Hero },
  metaInfo: {
    title: 'Inicio'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
