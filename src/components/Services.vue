<template>
    <div class="services">
        <h2 class="services-title">Te ofrecemos los siguientes servicios :</h2>

        <div class="service">
            <div class="service-content">
                <h2 class="service-title">Consulta Médica Domiciliaria</h2>
            </div>
            <div class="service-content">
                <h2 class="service-title">Consulta Médica en IPS</h2>
            </div>
            <div class="service-content">
                <h2 class="service-title">Medicina Alternativa</h2>
            </div>
            <div class="service-content">
                <h2 class="service-title">Especialidades Médicas</h2>
            </div>
            <div class="service-content">
                <h2 class="service-title">Ayudas Diagnosticas</h2>
            </div>
            <div class="service-content">
                <h2 class="service-title">Laboratorio Clinico</h2>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: 'Services'
        }
    },
}
</script>

<style lang="scss">
@import '@/assets/style/index';
.services {
    margin: 0 1rem;
    @include respond-to(small) {
        // margin: 0 2rem 2rem 2rem;

    }
    &-title {
        text-align: center;
        margin-bottom: 4rem;
        @extend .title;
    }
    p {
        color: $c-default;
    }
}
.service {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    text-align: center;
    margin: 0;
    @include respond-to(small) {
        grid-gap: 1rem;
        grid-template-columns: repeat(3, 1fr);
    }
    &-title {
        font-size: 1rem;
        color: $c-default;
        // padding: 2rem 1rem;
        // @extend .title;
    }
    &-content {
        background: url(../assets/images/mod.svg) no-repeat;
        background-size: contain;
        background-position: center;
        padding: 1rem;
        // margin-bottom: 1rem;
    }
}
</style>