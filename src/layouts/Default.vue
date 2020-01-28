<template>
  <div class="layout">

    <header class="header">
      <div class="header-menu my-container">
        <strong>
          <g-link to="/" class="nav-link">
            <div class="flex">
              <g-image src="~/assets/images/logo.svg" alt="logo medico amigo" class="logo"/>
              <div class="header-title">
                <p class="logo-text">{{ $static.metadata.siteName }}</p>
                <p class="slogan-text">Comprometidos con su salud</p>
              </div>
            </div>
          </g-link>
        </strong>

        <nav class="nav view-desktop">
          <g-link class="nav-link" to="/">Inicio</g-link>
          <g-link class="nav-link" to="/servicios/">Servicios</g-link>
          <g-link class="nav-link" to="/preguntas/">Blog</g-link>
          <g-link class="nav-link" to="/preguntas/">Preguntas Frecuentes</g-link>
        </nav>
        
        <button @click.prevent="drawer = true" class="btn-reset view-mobile">
            <i class="fas fa-bars btn-bar"></i>
            <!-- <g-image src="~/assets/images/bars.svg" alt="barras de menu" class="btn-bars"/> -->
        </button>
      </div>
    </header>
    <!-- Drawer de Navegación -->
    <el-drawer 
      :visible.sync="drawer"
      :direction="direction"
      custom-class="drawer-mobile"
      size="46%">

      <el-menu background-color="#f1f1f1" class="menu-mobile">
        <el-menu-item index="1">
          <g-link to="/">Inicio</g-link>
        </el-menu-item>
        <el-menu-item index="2">
          <g-link to="/servicios/">Servicios</g-link>
        </el-menu-item>
        <el-menu-item index="3">
          <g-link to="/servicios/">Blog</g-link>
        </el-menu-item>
        <el-menu-item index="4">
          <g-link to="/preguntas/">Preguntas Frecuentes</g-link>
        </el-menu-item>
      </el-menu>
      
    </el-drawer>
    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  metaInfo: {
    link : [
      {
        rel: 'stylesheet',
        href: 'https://use.fontawesome.com/releases/v5.0.13/css/all.css',
      }
    ]
  },
  data() {
    return {
      drawer: false,
      direction: 'ttb',
    }
  },
}
</script>

<style lang="scss">
@import '@/assets/style/index';
.header {
  background: $c-default;
  &-menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    height: 80px;
  }
}
.nav-link {
  margin-left: 20px;
  color: $c-dark;
    &:hover {
      color: $c-dark-hover;
      border-color: $c-dark-hover;
      }
  }
  .active--exact {
    border-bottom: 2px solid $c-dark;
  }
  .logo {
    padding-right: 0.5rem;
    width: 2.6rem;
    transition: all .1s ease-out;
    &:hover {
      width: 3rem;
    }
    @include respond-to(small) {
      width: 2.8rem;
    }
  }
  .logo-text {
    margin: 0;
    font-family: $font-nice;
    font-size: 1.4rem;
    font-weight: 600;
    // text-align: center;
    color: $c-dark;
    display: block;
    @include respond-to(small) {
      font-size: 1.6rem;
    }
  }
  .slogan-text {
    margin: 0;
    margin-top: -.4rem;
    font-size: 0.7rem;
    padding: 0;
    color: $c-dark;
  }
</style>
