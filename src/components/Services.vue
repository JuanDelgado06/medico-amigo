<template>
    <div class="services">
        <h2 class="services-title">Te ofrecemos los siguientes servicios :</h2>

        <div class="service">
            <div class="service-content">
                <h3 class="service-title">Consulta Médica Domiciliaria</h3>
            </div>
            <div class="service-content">
                <h3 class="service-title">Consulta Médica en IPS</h3>
            </div>
            <div class="service-content">
                <h3 class="service-title">Medicina Alternativa</h3>
            </div>
            <div class="service-content">
                <h3 class="service-title">Especialidades Médicas</h3>
            </div>
            <div class="service-content">
                <h3 class="service-title">Ayudas Diagnosticas</h3>
            </div>
            <div class="service-content">
                <h3 class="service-title">Laboratorio Clinico</h3>
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
    margin: 1.2rem;
    @include respond-to(little) {
        margin: 1rem 1.5rem;
    }
    @include respond-to(semiBig) {
        width: 90%;
        max-width: 1200px;
        margin: 1rem auto;
    }
    &-title {
        text-align: center;
        margin-bottom: 2rem;
        @extend .title;
        @include respond-to(small) {
            margin-bottom: 4rem;
        }
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

    grid-gap: 8px;
    @include respond-to(small) {
        grid-template-columns: repeat(3, 1fr);
    }
    &-title {
        display: flex;
        justify-content: center;
        align-content: center;
        width: 80%;
        margin: .4rem auto;
        color: $c-default;
        padding: 0;
        font-size: .8rem;
        @include respond-to(mini) {
            width: 90%;
            font-size: .9rem;
            margin: .6rem auto;
        }
        @include respond-to(little) {
            width: 80%;
            margin: 1rem auto;
        }
        @include respond-to(small) {
            font-size: 1.2rem;
            padding: 1rem 1rem;
        }
        @include respond-to(semiBig) {
            width: 55%;
            padding: 2.2rem 1rem;
            font-size: 1.5rem;
        }
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