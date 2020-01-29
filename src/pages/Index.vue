<template>
  <Layout>

    <Hero/>

    <div class="container-image">
  
      <g-image src="~/assets/images/background-section.svg" alt="fondo azul claro y oscuro"  class="back-section"/>
      <g-image src="~/assets/images/background-section-mobile.svg" alt="fondo azul claro y oscuro"  class="back-section-mobile"/>

      <div class="section">
      
        <div class="section-container">
          <div class="section-content">
            <h2 class="title-home">¿ Que es Médico Amigo ?</h2>
            <p>
              Somos una empresa de médicos generales y especialistas con amplia trayectoria en el cauca, enfocados en el cuidado del paciente y su familia, logrando un equilibrio fisico y mental
              a través de tratamientos convecionales y alternativos.
            </p>
          </div>
        </div>
        
      </div>
    </div>

    <Services/>

  </Layout>
</template>

<script>
import Hero from '~/components/Hero.vue'
import Services from '~/components/Services.vue'
export default {
  components: { Hero, Services },
  metaInfo: {
    title: 'Inicio'
  }
}
</script>
<style lang="scss" >
@import '@/assets/style/index';
.title-home {
  text-align: center;
  color: $c-default;
  @extend .title;
}
p {
  color: $c-default;
  font-size: 0.7rem;
  @include respond-to(mini) {
    font-size: .8rem;
  }
  @include respond-to(little) {
    font-size: 0.9rem;
  }
  @include respond-to(mid) {
    font-size: 1rem;
  }
}
.container-image {
  position: relative;
  display: inline-block;
  text-align: center;
  width: 100%;
  margin: 1rem 0;
  // @include respond-to(small) {
  //   margin: 1rem 0 1rem 0;
  // }
}
.back-section {
  width: 100%;
  display: none;
  @include respond-to(small) {
    display: block;
  }
}
.back-section-mobile {
  width: 100%;
  display: block;
  @include respond-to(small) {
    display: none;
  }
}
.section {
  position: absolute; 
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  &-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 2rem;    
    @include respond-to(small) {
      margin-bottom: 4rem;
    }
  }
  &-content {
    width: 90%;
    max-width: 1000px;
    @include respond-to(mini) {
      width: 80%;
    }
    @include respond-to(small) {
      width: 65%;
    }
    @include respond-to(semiBig) {
      width: 70%;
    }
  }
}
</style>
