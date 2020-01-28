<template>
  <Layout>

    <Hero/>
      <div class="container-image">
    
        <g-image src="~/assets/images/background-section.svg" alt="logo medico amigo"  class="back-section"/>
        <g-image src="~/assets/images/background-section-mobile.svg" alt="logo medico amigo"  class="back-section-mobile"/>
        
        <div class="section">
        
          <div class="section-container">
            <div class="section-content">
              <h2 class="title-home">¿ Que es Médico Amigo ?</h2>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas optio impedit, vel quis laborum culpa! Quos non minus consequatur labore culpa dolores itaque, alias quia harum esse explicabo, illum debitis.
              Exercitationem qui numquam, quo quaerat dolore quasi facere illum maiores voluptatem cumque libero saepe perferendis possimus. Quae ducimus voluptates in, voluptate nesciunt quia fuga distinctio, nihil fugit et voluptas praesentium.
              </p>
            </div>
          </div>

          <!-- <div class="section-container">
            <div class="section-content">
              <h2 class="title-home">¿ Porque utilizar Médico Amigo ?</h2>
              <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Unde ut ducimus maiores et consectetur facere harum labore modi repudiandae. Exercitationem deserunt ipsam velit esse laboriosam ducimus adipisci soluta tenetur quam.Enim expedita veritatis tempora tempore ut nisi soluta cumque repudiandae sit laboriosam, possimus odio assumenda minima debitis, eum modi ea dolor a quod! Libero voluptatibus similique, provident laudantium laboriosam dolore?</p>
            </div>
          </div> -->

        </div>

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
<style lang="scss" >
@import '@/assets/style/index';
.title-home {
  text-align: center;
  color: $c-default;
  font-size: 1.2rem;
  @include respond-to(mini) {
    font-size: 1.5rem;
  }
  @include respond-to(little) {
    font-size: 2rem;
  }
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
  @include respond-to(small) {
    margin: 2rem 0;
  }
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
    @include respond-to(big) {
      // width: 90%;
    }
  }
}
</style>
