<script>

const logo = "../public/logoblanco.png"
export default {
    name: 'Header_contact',
    
}
</script>

<template>
    <div class="container-xl">
    <header class="d-flex flex-wrap align-items-center justify-content-center justify-content-md-between py-3 mb-4">
        <div>
            <img src="/logoblanco.png" alt="Acceso Correcto" width="100" height="100" />
        </div>
        <ul class="nav col-12 col-md-auto mb-2 justify-content-center mb-md-0">
            <li><a href="/" class="text-decoration-none font-weight-bold nav-link text-white">Inicio</a></li>
            <li><a href="#/services" class="text-decoration-none font-weight-bold nav-link text-white">Servicios</a></li>
            <li><a href="#/contact" class="text-decoration-none font-weight-bold nav-link text-white">Contacto</a></li>
        </ul>
        <div>
            <v-btn block rounded="xl" size="x-large"
                class="v-btn v-btn--elevated v-theme--light bg-light-blue-lighten-1 text-white v-btn--density-default v-btn--size-default v-btn--variant-elevated"
                style="color: white;">Agendar reunión</v-btn>
        </div>
    </header>
</div>
</template>

<style>



</style>


