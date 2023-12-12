<script>
export default {
  name: 'piedepagina',
}

</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col-6 col-md-2 mb-3">
        <h5>Acceso Correcto</h5>
        <ul class="nav flex-column">
          <li class="nav-item mb-2"><a href="#" class="nav-link p-0 text-body-secondary">Sobre Acceso Correcto</a></li>
          <li class="nav-item mb-2"><a href="#" class="nav-link p-0 text-body-secondary">Bolsa de trabajo</a></li>
        </ul>
      </div>

      <div class="col-6 col-md-2 mb-3">
        <h5>Ayuda</h5>
        <ul class="nav flex-column">
          <li class="nav-item mb-2"><a href="#" class="nav-link p-0 text-body-secondary">Centro de ayuda</a></li>
          <li class="nav-item mb-2"><a href="#" class="nav-link p-0 text-body-secondary">Contacta con nosotros</a></li>
        </ul>
      </div>

      <div class="col-6 col-md-2 mb-3">
        <h5></h5>
        <ul class="nav flex-column">

        </ul>
      </div>

      <div class="col-md-5 offset-md-1 mb-3">
        <form>
          <h5>Registrate aquí </h5>
          <p>Nosotros nos pondremos en contacto contigo</p>
          <div class="d-flex flex-column flex-sm-row w-100 gap-2">
            <label for="newsletter1" class="visually-hidden">Correo electrónico</label>
            <input id="newsletter1" type="text" class="form-control" placeholder="Correo electrónico">
            <div>
              <v-btn elevation="8" rounded="xl" size="large"
                class="v-theme--light bg-light-blue-lighten-1 text-white">Registrarse</v-btn>
            </div>

          </div>
        </form>
      </div>
    </div>

    <div class="d-flex flex-column flex-sm-row justify-content-between py-4 my-4 border-top">
      <p>&copy; 2023 Acceso Correcto. Todos los derechos reservados.</p>
      <ul class="list-unstyled d-flex">
        <li class="ms-3"><a class="link-body-emphasis" href="#"><svg class="bi" width="24" height="24">
              <use xlink:href="#twitter" />
            </svg></a></li>
        <li class="ms-3"><a class="link-body-emphasis" href="#"><svg class="bi" width="24" height="24">
              <use xlink:href="#instagram" />
            </svg></a></li>
        <li class="ms-3"><a class="link-body-emphasis" href="#"><svg class="bi" width="24" height="24">
              <use xlink:href="#facebook" />
            </svg></a></li>
      </ul>
    </div>
  </div>
</template>

<style></style>