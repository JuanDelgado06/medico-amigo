<template>
    <div class="hero">
        <div class="my-container">
            <h2 class="hero-title">Consulta Médica en Casa</h2>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss">
@import '@/assets/style/index';
.hero {
    width: 100%;
    height: 35vh;
    display: flex;
    background: $c-default;
    background-image: url(../assets/images/hero-medico-2.jpg);
    background-size: cover;
    background-position:top;
    background-repeat: no-repeat;
    justify-content: center;
    align-items: center;
    @include respond-to-height(mini) {
        height: 50vh;
    }
    @include respond-to-height(small) {
        height: 35vh;
    }
    @include respond-to-height(mid) {
        height: 28vh;
    }
    @include respond-to(semiBig) {
        // background-image: url(../assets/images/hero-medico.png);
        background-position:right;
        background-image: url(../assets/images/hero-medico-2.jpg);
        height: 87vh;
    }
    
    &-title {
        // margin: 0 0 1.5rem 0;
        width: 70%;
        margin: 0;
        text-transform: uppercase;
        text-align: center;
        color: $c-dark;
        font-size: 1.8rem;
        font-family: $font-nice;
        font-weight: 700;
        @include respond-to(mid) {
            width: 70%;
            font-size: 3rem;
        }
        @include respond-to-height(semiBig) {
            width: 68%;
        }
    }
    &-text {
        text-align: center;
        color: $c-dark;
        font-size: 1.5rem;
        font-weight: 700;
        margin: 0;
    }
}
</style>